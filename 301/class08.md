# Readings: APIs

## API Design Best Practices
<!-- https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design -->

- **What does `REST` stand for?**

Representational State Transfer (REST) -> an architectural approach to designing web services.

- **REST APIs are designed around** _resources_

- **What is an identifer of a resource? Give an example.**
A URI that uniquely identifies that resource. For example, the URI for a particular customer order might be:
`https://adventure-works.com/orders/1`

- **What are the most common HTTP verbs?**
GET, POST, PUT, PATCH, and DELETE.

- **What should the `URIs` be based on?**
Resource URIs should be based on nouns (the resource) and not verbs (the operations on the resource).

- **Give an example of a good URI.**
`https://adventure-works.com/orders // Good`

- **What does it mean to have a `chatty` web API? Is this a good or a bad thing?**
 "Chatty" web APIs -> expose a large number of small resources.
 bad thing.

- **What status code does a successful `GET` request return?**
Returns *HTTP status code 200 (OK)*.

- **What status code does an unsuccessful `GET` request return?**
If the resource cannot be found, the method should return *404 (Not Found)*.

- **What status code does a successful `POST` request return?**
If a POST method creates a new resource, it returns *HTTP status code 201 (Created)*.

- **What status code does a successful `DELETE` request return?**
 HTTP 200 or HTTP 204 should imply "resource deleted successfully".
-204 as the article-
<!-- ---
Bookmark/Skim
https://regexr.com/
## RegExr 
How would you match your name using RegEx?

https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285

https://regex101.com/ -->