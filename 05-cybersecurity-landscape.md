# Cybersecurity Landscape

Application security. 
- WAF(web app firewalls)
- SAST / DAST
- API SECURITY
- Automation first


Our final section here is on the Application Security Technology Landscape. Cybersecurity is a pretty large market. I'm not going to go through all of this because it's way too much, but there are many, many facets and aspects to cybersecurity. What we're focusing on here is Application Security, for which there are many technologies. You've got static code analyzers, dynamic testers, software composition analysis, container security, web application firewalls, web scanners and so forth. These are all very well known and widely deployed technologies. But the reality is, as you've seen from these API breaches, there's a new class of risk, of attack vector, that is targeting APIs and they're being successful. And that is revealing that the existing technologies have gaps in their coverage. So let's dig into that a little bit deeper here.



You see here a very simplified pipeline from developing technologies to deploying them to operating them. And in the development phase you've got security tools that will look at your code, look for coding weaknesses and injection flaws or weak authentication config issues. These tools might look at your third party libraries for outdated or known vulnerable code that your application may be relying on.

And over on the far right, when we get into production, you've got technologies like gateways, firewalls and API threat management tools that will handle authentication, do some level of authorization controls, perform traffic management to rate-limit and control where your traffic is coming from - what's permitted, what's not, log all the activities, do anomaly detection and so forth.

 

But here in the middle is where the biggest gap has existed in terms of security - which is security testing, specifically API security testing.

 

You may be familiar with web application scanners that are designed to interact with web interfaces and mobile interfaces. APIs don't have anything like that. The interface is a machine interface. It's a flashing cursor prompt. There's no structure, there's no standard workflow presented at an API level. And so you need to implement comprehensive, effective security testing at the API level. Things that will test all those OWASP categories, test the business logic of your application, that will exploit or evaluate any authentication weaknesses that exist or authorization gaps logic flaws, and simulate all those scenarios in a very comprehensive way. 

 

And you want to accomplish this testing “left” of this dotted line. The whole concept of “shift left” implements this type of security testing on every release, as part of your CI/CD pipeline, so that every push to production goes through the same hurdles, the same evaluations. And if anything is discovered, you know about it before it ever makes it into production. And that's why automation is so critical. You can't run a manual penetration test on every release - whether that's happening every, every week or every night. It's not feasible. So automation is critical here as well.