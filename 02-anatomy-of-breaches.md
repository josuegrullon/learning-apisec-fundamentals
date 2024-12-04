### Case: Coinbase
They found that through API attack you can sell any coin you dont own. 

The attacker sniffed the web traffic to the api and found a call where he could manipultate the parameters, changing the source to any and transfering to his account. <i> He reported it</i>.

The company shat down the service, reproduce it and apply necessary fixes. They applied  a validation  to the endpoint. 


### Case: US POSTAL

They discovered some endpoint with lack of authentication. Allowing someone to see anyone information. 

### Case: Peloton

A wide open api allowing 4B user information including Joe Biden

### Case: Venmo
Payment gateway. 
No server limitations allowed the attaackers to harvest all the transactions inclusive the api having rate limiting were allowing to download 115k daily returning all transactions details. 
 
Didnt have authentication.
It was  sniffed. 

It had an open endpoint to authenticate other endpoints. 

### Case: Instagram

Account exploit to acccount takeover.  Sent the OTP and brute forced the endpoint with the 6 digit code permutation.  Instagram limits 200 users per IP but.. dont have reestriction per group of ips.. so the attacker bypass by rotating ips

They had to add expiration of the code.. and limit the amount of calls per EP for multiple ip addresses


### Case: Bumble
Permitted acces to 95M users details without authentication. <strong>Incremental Ids allowed easy scrapping of the db</strong> Enabling the exact user location per triangulation. 

Api allowed paid features by enabling without any priviledges. 


### Case: T-Mobile

Endpoint without authorization allowd the scrapping.
Reputational bridge and damage


### Case: Optus
Api without autentication. Breach allowed data harvesting  giving licence and medicare etc. 



### Case: Experian

Credit reporting agency. Danger of Third parties. 
No authenticated api. Allowed to look up any credit score of anyone in the US. 