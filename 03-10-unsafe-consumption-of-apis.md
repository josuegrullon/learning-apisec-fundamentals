

#### API10: Unsafe consumption of apis
- Third party apis can be expoited, we normally trust them. 
- Clients blindly can follow a redirection suggested from the third party. 


And now the last one of the OWASP API Security Top 10 is Unsafe Consumption of APIs. This is a new addition to the Top 10 and it reflects the risk that you may experience from use of third party APIs. The exposure can be data theft, breach, takeover, and so forth. But let's walk through an example of what this can look like.

 

Let's say your application does user address verification. We want to make sure that the address that they've inputted gets normalized and corrected and inserted into your database in a clean way. And for that, you might use a third party data cleansing API. The attacker may be aware of this (or simply guess which third party you're using) and go into that third party and insert malicious data. They may try to update their own address information and, I'll use a silly example, set their street address is “drop table” or some type of command, something malicious. Then what they'll do is come to your site - maybe fill out a loan application and insert that address. Your application will pull that address record from the third party and suddenly you have this injection command coming into your environment.

 

Another example is the use of URL redirects. Your third party API may instruct you to go to another site, another resource indicator to fetch information. Well that can be abused and it can suddenly cause your site to get redirected to a third party or to a malicious site through this third party infiltration.

 

The prevention here is to, again, not trust the data that's being inputted or being delivered to you. You want to validate, make sure that it looks and adheres to what your site is expecting. You want to evaluate the security of your third parties, make sure that they're doing proper security controls and testing and validation encryption goes without saying. But also have an inventory of all the third party APIs that you use and make sure you're regularly auditing them.