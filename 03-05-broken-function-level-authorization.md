

#### API5: BROKEN FUNCTION LEVEL AUTORIZATION
- Abuse of endpoint functionality
- Modify parameters: role = admin
- Delete an invoice
- Set account balance = 0


OWASP number 5 is Broken Function Level Authorization. This is a carryover from the prior OWASP API Top 10. This is about providing functional access that's not warranted or not required by a particular user. In many cases what an attacker will do is look at an endpoint that provides a benign GET request - a lookup type request - and attempt to use things like PUT and DELETE. They are looking to discover whether or not those types of commands actually get executed or not. The exposure here is you can manipulate information and transact in ways that are not authorized. This could allow you to escalate privileges, modify account details and so forth. 

 

Examples here are replacing GET methods with PUT. So instead of just looking up my record with a GET request, I'm actually trying to modify it - for example, changing my role from a user to an admin. Or I could go in and use a DELETE command to delete my invoice or set the balance due to zero or even to a negative number.

 

This demonstrates how creative the attacks can be and, and why you need to think not only about what your application should do, but how it could be abused, how might it be used in unintended ways.

 

In terms of prevention, you should look at those business flows, those functions that are especially sensitive - business flows that could result in a manipulation of data, an escalation of privilege, or performing transactions that shouldn't be authorized to anyone but the legitimate user. And then implement controls and testing to make sure you're properly vetting those endpoints across every possible combination of request type - and doing that on a continuous basis, on every release, on every push to production.

 