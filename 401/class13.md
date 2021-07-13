# Read: 13 - Related Resources and Integration Testing

## [Related data in Spring](https://www.baeldung.com/spring-data-rest-relationships)

### 1. One-to-One Relationship
**1.1. The Data Model**

- One-to-one relationship is using  -> the `@OneToOne` annotation. 
- The `@RestResource` annotation is optional and can be used to customize the endpoint.
- We must be careful to have different names for each association resource.
```
@OneToOne
@JoinColumn(name = "secondary_address_id")
@RestResource(path = "libraryAddress", rel="address")
private Address secondaryAddress;
```
if we add this code to class and we have in that class other resource called Adress,
we'll face conflict, so that we can solve it by by specifying a different value for the rel attribute or by omitting the RestResource annotation so that the resource name defaults to secondaryAddress.
  
**1.2. The Repositories**
'In order to expose these entities as resources, let's create two repository interfaces for each of them, by extending the CrudRepository interface:'
`public interface LibraryRepository extends CrudRepository<Library, Long> {}`
`public interface AddressRepository extends CrudRepository<Address, Long> {}`
Note, we'll assume that we will have two classes (Library and address), and each one is Entity that includes @Id, @Column, and @OneToOne.

**1.3. Creating the Resources**
- To add a Library instance:

```
curl -i -X POST -H "Content-Type:application/json" 
  -d '{"name":"My Library"}' http://localhost:8080/libraries
```
For curl on Windows,  escape the double-quote character inside `'{"name":"My Library"}'`.

- and The API returns the JSON object.
as in 
```
 "name" : "My Library",
  "_links" : {
    "self" : {
      "href" : "http://localhost:8080/libraries/1"
    } , etc.......
```

- Before we create an association, sending a GET request to this endpoint will return an empty object.
so, if we want to add an association, we must first create an Address instance also.
and we'll have the result of the POST request inside a JSON object.

**1.4. Creating the Associations**



## [Baeldung: Spring Integration Testing](https://www.baeldung.com/integration-testing-in-spring)
