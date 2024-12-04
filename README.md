# API SECURITY FUNDAMENTALS

### Instructor: Dan barahona


### Do's and dont's


First, don't trust anything. I've talked about this a number of times. Don't trust the inputs, don't trust the network. Don't trust anything. 

 

You need to validate all those inputs. Make sure that the parameters, the inputs that are coming into your API match what's expected and toss away everything else. It can be malicious. You shouldn't be processing it. 

 

Don't confuse obfuscation with security. Just because you're obfuscating your code doesn't mean it can't be reverse engineered or un-obfuscated. Just keep sensitive data out of your code. No keys, no tokens, nothing hard-coded. That's what attackers are going to look for. They're going to look for keys and then try to reuse them themselves to gain access and to perform data exfiltration.

 

Don't reveal useful info in error messages. If you need to say a user is not authenticated, that's enough. You don't need to say you're expecting an eight digit numerical number. That's info that does not need to be shared back.

 

Don't have hidden or unadvertised features. I was talking to one organization where they have a published API and then they have unpublished APIs and they acknowledge and expect users will find and use these. Don't do that. Don't leave it to your users to figure out what's possible. Make sure you control what's accessible, how it can be accessed, what functionality you're making available.

 

Don't filter data in the UI. That is not the job of your UI. That's the job of your app. This goes back to the API-First principles. The application itself should control what data is coming out. The UI’s job is simply to present, not to enforce or control.

 

Don't confuse authentication with authorization. Authentication is about me demonstrating that I'm me. Your application needs to control what I can see and under what circumstances.

 

Do use API gateways to control traffic and to really centralize your management. All APIs need to be controlled and managed in a consistent way

 

Do require API documentation. This is an absolute must, non-optional. Make sure that your APIs are properly documented - not only for internal use, but for security purposes. That documentation is critical to being able to properly test and validate the functionality of your API.

 

Do expect hackers to find and use those undocumented endpoints.

 

Do continuous tests on every release, every push to production, simulate attacks, look at your configs, do injections, do fuzzing, test authentication, test authorization.