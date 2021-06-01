# Readings: CRUD

## [Status Codes Based On REST Methods](https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/)

1. **in your own words, describe what each group of status code represents:**
**100’s** =   tell the client that the header part of the request has been received and the server will try to comply with a transmission demand of the client.
**200’s** = (success codes)They tell the client that its request was accepted
**300’s** =  These are redirection codes. They tell the client that the resource they are requesting isn’t available at the expected location anymore. 
**400’s** = These are the client error codes. They are all about invalid requests a client sent to a server. There are several causes to this, timeouts, wrong URI, missing authentication, etc.
**500’s** = These are the server error codes. Often they indicate problems with overwhelmed servers or unreachable servers behind proxies, but sometimes they can be directly related to client requests that trigger error exceptions on the server. 
2. **What is a status code 202?**
 In case of asynchronous processing of a request (202), this doesn’t mean the request was successfully processed only that it met all validation requirements at the time of sending.

3. **What is a status code 308?** 
308 Permanent Redirect - This tells the client to use another URL to access the resource and not use the current URL anymore. It’s helpful when we have multiple endpoints for one resource, but don’t want to implement reading from all of them

4. **What code would you use if an update didn’t return data to a client?**
204 No Content
5. **What code would you use if a resource used to exist but no longer does?**
410 Gone
6. **What is the ‘Forbidden’ status code?**
403