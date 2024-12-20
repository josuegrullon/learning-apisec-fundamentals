

#### API7: Server Side Request Forgery
- Injecting Localhost/api/user could leak 
- We should always filter the users input


Item #7 on the OWASP API Security Top 10 list is a brand new one. It's called Server Side Request Forgery.

  📍 I think it's been added because this has been a source of quite a lot of vulnerabilities. The idea here is API endpoints that accept URLs as input parameters provides an opening for malicious behavior. That that URL upload or input can create a channel for access to third party sites, malicious sites, downloading of malicious information or data or applications.

Here's an example. A particular endpoint required the user to provide a URL. Maybe that was a URL of their LinkedIn address or something like that. Instead of putting a legitimate LinkedIn address they inserted this /localhost/api/user-data. Maybe that was just a guess, but what they were doing is they're instructing the server to access this particular file on the host itself with user data and potentially return that data back to the requester.

If we're not doing proper validation, then that might actually get executed. Or you might point that URL to a malicious site where there may be malware or, other binaries or key loggers or whatever it might be.

The prevention here is very clear, right? You wanna not trust anything. You have to validate and sanitize any user inputs, not just for URLs, but especially for URLs. And not trust any URLs that do not meet your requirements. If it's a LinkedIn address, it needs to look like a LinkedIn address or whatever it might be that your application is expecting.

And then filter out everything that doesn't match. Do not just blindly trust the user data that's being inputted

Again, you want to implement testing and fuzzing and, attempting all kinds of different parameters into those inputs to ensure that nothing misbehaves, that your application doesn't process data that it shouldn't.