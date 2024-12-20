

#### API3: BROKEN OBJECT PROPERTY LEVEL AUTORIZATION

- User is able to set up type=preemium
- User search returns unneccesary information
- Mass assignment is when a user can modify values over his level. 


Next up is OWASP API Security number 3, Broken Object Property Level Authorization. This is a new entry into the Top 10 in 2023, but is actually in some ways a merger of two of the old categories of Mass Assignment, which is the ability to update object elements within an API endpoint, as well as Excessive Data Exposure category, which is about revealing unnecessarily sensitive data for the particular use case of that particular application.

 

An example of what this can look like is manipulating an object ID, for example account type, and overriding a free account to a premium. This is an example of a Mass Assignment where you can actually modify and update object values. Another example - let's say you have an endpoint to do a simple user search or something like that, then there is no need to return more information like account IDs and emails and other sensitive details when the use case doesn't require it. 

 

The prevention here is to make sure your API endpoints are returning only the data that is legitimately required for that application and nothing more. Do not rely on filtering in the UI to do that work for you. Make sure your API is only returning the data that the application that the use case requires. And then make sure that users can only access the info they need and cannot modify data that they should not have the opportunity or the ability to modify.