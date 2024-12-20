

#### API4: UNRESTRICTED RESOURCE CONSUMPTION
- MIssing rate controls
- Execution timeouts
- Max allocable memory
- Max number of files to upload / size
- Exesive records returned or resources returned in single request


Moving on to OWASP number 4, Unrestricted Resource Consumption. This used to be called Lack of Resources and Rate Limiting and really has to do with high volume types of attacks - mass data harvesting. It can result not only in huge amounts of data loss, but also things like denial of service and operational impact as well.

 

Examples here include missing or inadequate rate controls - the ability to harvest data in excess of what an application should require. For example, there's no need for a user to query a thousand times when a typical user is only going to access it once or twice. Lack of time outs or memory limits, number of files or upload sizes, enabling excessive operations in a single request - that can really overload your server from an operational standpoint and also lead to the excessive data exposure. Returning massive volumes of records in a single request is another example.

 

The prevention here is to put in traffic controls, whether it's in a web application firewall or an API gateway. But you should also implement logic within the application itself. For example, if you have an account reset capability, a legitimate user is going to attempt to provide a reset code once, twice, maybe five times. There's no one that's going to try a thousand times. So regardless of whether someone is rotating IP addresses or cleaning their cookies out, there's no legitimate user that's going to try a thousand times. And so even though those attacks may make it through a traffic control device, your application logic should account for that and disable that reset code after a certain number of attempts.