# Read: 12 - Spring RESTful Routing & Static Files

## [Baeldung: Spring Request Mapping](https://www.baeldung.com/spring-requestmapping)

2. @RequestMapping Basics

- **2.1. @RequestMapping — by Path**
```
@RequestMapping(value = "/ex/foos", method = RequestMethod.GET)
@ResponseBody
public String getFoosWithHeaders() {
    return "Get some Foos with Header";
}
```
To test out this mapping with a simple curl command, run:
`curl -i http://localhost:8080/spring-rest/ex/foos`

- **2.2. @RequestMapping — the HTTP Method**
The HTTP method parameter has *no default*.
`@RequestMapping(value = "/ex/foos", method = POST)`

To test the POST via a curl command:
`curl -i -X POST http://localhost:8080/spring-rest/ex/foos`

3. RequestMapping and HTTP Headers

- **3.1. @RequestMapping With the headers Attribute**
The mapping can be narrowed even further by specifying a header for the request:
`@RequestMapping(value = "/ex/foos", headers = "key=val", method = GET)`
test `curl -i -H "key:val" http://localhost:8080/spring-rest/ex/foos`

or even multiple headers
```
@RequestMapping(
  value = "/ex/foos", 
  headers = { "key1=val1", "key2=val2" }, method = GET)
```
test `curl -i -H "key1:val1" -H "key2:val2" http://localhost:8080/spring-rest/ex/foos`

- **3.2. @RequestMapping Consumes and Produces**
Starting with Spring 3.1, the @RequestMapping annotation now has the produces and consumes attributes.

4. RequestMapping With Path Variables
- **4.1. Single @PathVariable**
```
@RequestMapping(value = "/ex/foos/{id}", method = GET)
@ResponseBody
public String getFoosBySimplePathWithPathVariable(
  @PathVariable("id") long id) {
    return "Get a specific Foo with id=" + id;
}
```
test -> `curl http://localhost:8080/spring-rest/ex/foos/1`

If the name of the method parameter matches the name of the path variable exactly, then this can be simplified by using @PathVariable with no value:
`@PathVariable String id) {`


- **4.2. Multiple @PathVariable**
```
@RequestMapping(value = "/ex/foos/{fooid}/bar/{barid}", method = GET)
@ResponseBody
public String getFoosBySimplePathWithPathVariables
  (@PathVariable long fooid, @PathVariable long barid) {
    return "Get a specific Bar with id=" + barid + 
      " from a Foo with id=" + fooid;
}
```

- **4.3. @PathVariable With Regex**
`@RequestMapping(value = "/ex/bars/{numericId:[\\d]+}", method = GET)`
`  @PathVariable long numericId) {`

5. RequestMapping With Request Parameters
```
@RequestMapping(value = "/ex/bars", method = GET)
@ResponseBody
public String getBarBySimplePathWithRequestParam(
  @RequestParam("id") long id) {
    return "Get a specific Bar with id=" + id;
}
```
For more advanced scenarios,
`@RequestMapping(value = "/ex/bars", params = "id", method = GET)`

Multiple params values can be set
```
@RequestMapping(
  value = "/ex/bars", 
  params = { "id", "second" }, 
  method = GET)
  ```

6. RequestMapping Corner Cases

- **6.1. @RequestMapping — Multiple Paths Mapped to the Same Controller Method**
In that case, the value attribute of @RequestMapping does accept multiple mappings
```
@RequestMapping(
  value = { "/ex/advanced/bars", "/ex/advanced/foos" }, 
  method = GET)
```
- **6.2. @RequestMapping — Multiple HTTP Request Methods to the Same Controller Method**
with different HTTP verbs
```
@RequestMapping(
  value = "/ex/foos/multiple", 
  method = { RequestMethod.PUT, RequestMethod.POST }
)
```
- **6.3. @RequestMapping — a Fallback for All Requests**
`@RequestMapping(value = "*", method = RequestMethod.GET)`

- **6.4. Ambiguous Mapping Error**
- Occurs when Spring evaluates two or more request mappings to be the same for different controller methods. 
- A request mapping is the same when it has the same HTTP method, URL, parameters, headers, and media type.
- So it will give error msg.

but what will not result in ambiguous mapping error
```
@GetMapping(value = "foos/duplicate", produces = MediaType.APPLICATION_XML_VALUE)
public String duplicateXml() {
    return "<message>Duplicate</message>";
}
    
@GetMapping(value = "foos/duplicate", produces = MediaType.APPLICATION_JSON_VALUE)
public String duplicateJson() {
    return "{\"message\":\"Duplicate\"}";
}
```

- when return the correct data representation based on the Accepts header supplied in the request.

- Another way to resolve this is to update the URL assigned to either of the two methods involved.

7. New Request Mapping Shortcuts

@GetMapping
@PostMapping
@PutMapping
@DeleteMapping
@PatchMapping

8. Spring Configuration

We  need a @Configuration class to enable the full MVC support and configure classpath scanning for the controller.




## [Spring guide: Accessing Data with JPA](https://spring.io/guides/gs/accessing-data-jpa/)

## [Baeldung: Comparing repositories](https://www.baeldung.com/spring-data-repositories)