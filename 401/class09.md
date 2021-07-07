# Read: 09 - WRRC and Java

## [High-level HTTP](https://dev.to/dangolant/things-i-brushed-up-on-this-week-the-http-request-lifecycle-)


### Step 1: Local Processing

1. When you type the domain name in the browser.

2. The browser will extract the IP by looking through its own cache of recently requested URLs, the operating system’s cache of recent queries, your router’s cache, and your DNS cache.

### Step 2: Resolve an IP

1. If the cache lookup fails, your browser fires off a DNS request using UDP3. The DNS request contains the preconfigured IP for your DNS server and your return IP in its header. 
'*UDP is a lightweight protocol, but the tradeoff is that it offers no guarantees in terms of delivery, and there is no acknowledgement other than a response being sent and received.*'

2. Your request will now have to travel many network devices to reach its target DNS server. 

3. Once your request arrives at your configured DNS server, the server looks for the address associated with the requested hostname. If it finds one, it sends a response.
if not it will send it to another DNS server, This happens recursively until the address is found.
 

4. now the request is successful though. If the response makes it back (remember, with UDP there’s no guarantee!), the requesting client now has a target IP. and it can be cached.

### Step 3: Establish a TCP Connection


1. TCP(unlike UDP) ensures delivery and ordered data transmission. and using a sequence number for every byte sent would allow the receiver to re-order received packets back into their original order, and allows the sender to retransmit any packet that does not get acknowledged by the receiver.

2. TCP connections are opened using what’s known as a three-way handshake. 

3. We now have a completed three-way handshake and an established connection. The connection has also established a random, sequential sequence11 for each direction of communication (client->server, server->client), allowing a full duplex communication.

### Step 4: Send an HTTP Request

1. The request is made up of a "request line", request header, and a body. The "request line" is simply a line that indicates the HTTP method, the resource being requested, and the protocol version. 
The header of the request is made up of pairs in the form name:value <CR><LF>, that indicate the end of the header section. 
**HOST** is The only mandatory field in an HTTP request, which contains the domain and port that the request is being sent to (domain.com:8080), although in some cases the port can be omitted. 


2. Once the HTTP request is sent, the server can ensure it receives the whole request, in the correct order.

3.  the server generates an HTTP response. that contains a "status line", response header fields, and an optional body. 

4. 'Once the response is generated, the server responds to the request. At the TCP layer, the client receives the first data packet, the first byte of which should contain the HTTP response header. More packets start coming in, and at the TCP layer they are re-ordered as needed. For every two packets that the client receives at the TCP layer, it sends an ACK message to the server. This goes on until the response is (hopefully) fully loaded'.

### Step 5: Tearing Down and Cleaning Up
<!-- this point needs more understanding -->
so the  first will be rendered to the user.




## [Java HTTP Request](https://www.baeldung.com/java-http-request)
`all of these classes in the article are in Java.net package`

#### (1&2)
- **The HttpUrlConnection class** allows us to perform basic HTTP requests without the use of any additional libraries.

#### (3)
and we can create a request, using **openConnection()** method of the URL class.
**setRequestMethod** method values are: GET, POST, HEAD, OPTIONS, PUT, DELETE, TRACE.
```
URL url = new URL("http://example.com");
HttpURLConnection con = (HttpURLConnection) url.openConnection();
con.setRequestMethod("GET");
```
#### (4)
If we want to add parameters to a request, we have to set the doOutput property to true, then write a String of the form param1=value to the OutputStream of the HttpUrlConnection instance.
```
Map<String, String> parameters = new HashMap<>();
parameters.put("param1", "val");

con.setDoOutput(true);
DataOutputStream out = new DataOutputStream(con.getOutputStream());
out.writeBytes(ParameterStringBuilder.getParamsString(parameters));
out.flush();
out.close();
```
#### (5)
setRequestProperty() method, used to Add headers to a request:
`con.setRequestProperty("Content-Type", "application/json");`
the getHeaderField() method, used To read that value.
`String contentType = con.getHeaderField("Content-Type");`

#### (6)
HttpUrlConnection class allows **setting the connect and read timeouts**, using these methods `setConnectTimeout(number) and setReadTimeout(number)`.

#### (7)
classes to handle cookies(that offered by java.net packages)-> **CookieManager and HttpCookie**.

#### (8)
We can enable or disable automatically following redirects for a specific connection by using the **setInstanceFollowRedirects()** method with true or false parameter.

#### (9)
Reading the response of the request can be done by parsing **the InputStream of the HttpUrlConnection instance**.

#### (10)
If the request fails, trying to read the InputStream of the HttpUrlConnection instance won't work. Instead, **we can consume the stream provided by HttpUrlConnection.getErrorStream()**.

#### (11)
It's not possible to get the full response representation using the HttpUrlConnection instance.
However, **we can build it using some of the methods that the HttpUrlConnection instance**
```
public class FullResponseBuilder {
    public static String getFullResponse(HttpURLConnection con) throws IOException {
        StringBuilder fullResponseBuilder = new StringBuilder();

        // read status and message

        // read headers

        // read response content

        return fullResponseBuilder.toString();
    }
}
```






