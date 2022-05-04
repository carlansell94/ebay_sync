Simple application to pull seller information from your ebay account using the ebay API.
  
Features:
* Fetches orders, fees and feedback
* Able to pull in tracking numbers for labels purchased through eBay - though unfortunately, the API does not reliably return this info in all cases
* Support for multiple orders per tracking number
* Syncs partial/full refund information - though at present, eBay fee refunds need to be added manually
* Includes fields to enter tracking info, actual postage cost and carrier info (currently must be done manually)
* Works with the new eBay managed payments system

Requirements:
* Python 3
* MySQLdb
* eBay developer account
  
How To Use:
* Create a database using the schema file in /setup.
* Fill in the credentials.ini file.
* Move credentials.ini to /core.
* Run sync/run.py to start.
  
eBay Credentials:
In order to use this application, you will need to sign up for an eBay developer account, and create a production app.  

You will also need to add your Auth'n'Auth token, and OAuth refresh token. This app is currently unable to generate refresh tokens from authorisation codes.

Development:
While this code is tested and used on a regular basis, certain features (such as refund handling) have seen little real-world testing.

The database schema is subject to change, as more eBay API data is added.

It could certainly do with a cleanup, which I might get around to at some point.