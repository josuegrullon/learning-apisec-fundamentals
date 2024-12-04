

#### API2: BROKEN AUTHENTICATION
- Weak/missing authentication controls in the app. 

 
Moving on to OWASP number 2, which is Broken Authentication. As the name suggests this is about weak or non-existent authentication to endpoints. This is number 2 also for a reason. As you've seen in the real-world breaches section, it's very common. The exposure is the ability to access other users’ accounts, data theft, unauthorized transactions. 

 

Examples of weak authentication are things like weak password requirements; vulnerability to credential stuffing; brute forcing of IDs and passwords - which are quite readily available on the dark web; lack of CAPTCHAs or rate limiting; lack of lockouts on accounts; putting authentication info into URLs - which can be sniffed and reused by malicious parties; changing passwords without authentication or verification; not validating tokens; not storing passwords properly. 

 

The prevention here is to properly define what your authentication requirements are and to tailor those requirements to the use case. If you've got an endpoint that performs fairly benign functionality, then maybe no authentication is perfectly fine. But if you've got another endpoint that's accessing personally identifiable information (PII), then you probably want to make sure that you are enforcing very strict authentication. And then implementing application logic to ensure that users only see what they're entitled to see. Again, you want to implement continuous testing to make sure no changes are creeping into code logic or into the infrastructure that may be exposing new authentication vulnerabilities.