

#### API9: IMPROPER INVENTORY MANAGEMENT
- You need to have a propper view of your api
- Outdated documentation
- Improper versioning/ deprecation
- Api access via third party


The next item is OWASP number 9, Improper Inventory Management. This is a slight update of the old one, which was called Improper Asset Management. The idea here is you need to have a comprehensive and accurate view of your API environment - all of the APIs that are running, all the endpoints, versions, older versions, who's accessing them, and so forth.

 

What we find is attackers are going to look under the hood - they're going to look for old versions of APIs. So when you increment from version 3 of the API to version 4, what happens to version 3? Does it get retired? Does it stay accessible? Are there unpatched endpoints on that older version that you've corrected in the new version, but still exist on that older version? Hackers are looking for those types of things. They know that those older editions may have endpoints with vulnerabilities or weaker security or outdated documentation. This is the kind of thing that they're looking for to exploit. 

 

So you want to make sure to deploy and manage all your APIs in a controlled fashion - typically through an API Gateway - something where you ensure that every API has gone through a proper set of approvals and tests and validations before they go live.

 

You also want to define your rules for versioning and retiring older versions - when should you update an API from one version to a next, how do you communicate to all the users that need to have access to it; how are you retiring the old version and under what conditions and so forth? And then you want to make sure you're auditing who's accessing your APIs. Do they still have a legitimate need to access it? Are they on the correct version of the APIs and so forth.