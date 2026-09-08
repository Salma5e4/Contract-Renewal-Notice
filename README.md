
# Contract-Renewal-Notice
STEP 1 — Create the Package 

In Eclipse ADT, we created a package: 

ZCONTRACT_RENEWAL 

STEP 2 — Create Database Table 

We created: 

ZCONTRACT_HDR 

This is the database table where contract information is stored. 

Fields 

CONTRACT_NO 
SUPPLIER 
CONTRACT_START 
CONTRACT_END 
CONTRACT_VALUE 
RENEWAL_REQUIRED 
AUTHORIZED_BY 
AUTHORIZATION_DATE  

STEP 3 — Create CDS Root View 

Next, we created: 

ZCONTRACT_I_RENEWAL 

This is our CDS root view entity. 

It reads data from: 

ZCONTRACT_HDR 

The flow is: 

ZCONTRACT_HDR 
      ↓ 
ZCONTRACT_I_RENEWAL 

 

STEP 4 — Create Behavior Definition 

Then we created the Behavior Definition for: 

ZCONTRACT_I_RENEWAL 

This defines what users can do with the contract data. 

We allowed: 

CREATE 
UPDATE 
DELETE 

 

 

STEP 6 — Create Projection CDS 

Next we created: 

ZCONTRACT_C_RENEWAL 

This is the projection layer. 

The flow becomes: 

ZCONTRACT_HDR 
      ↓ 
ZCONTRACT_I_RENEWAL 
      ↓ 
ZCONTRACT_C_RENEWAL 

 STEP 7 — Projection Behavior 

Then we created the projection behavior. 

We exposed: 

use create; 
use update; 
use delete; 

This tells RAP that these operations from the underlying business object can be used through the projection. 


STEP 8 — Create Service Definition 

Next we created: 

ZCONTRACT_UI_RENEWAL 

This is the Service Definition. 

We exposed: 

ZCONTRACT_C_RENEWAL 

as 

ContractRenewal 

The service definition tells SAP: 

"This is the business data that I want to make available as a service." 

STEP 9 — Create Service Binding 

Then we created: 

ZCONTRACT_UI_RENEWAL_O4 

with: 

OData V4 – UI.  

 

STEP 10 — Publish the Service 

After creating the Service Binding, we: 

Activate → Publish → Preview 

This makes our service available for testing. 

Then we opened the Fiori Elements Preview. 

Initially, we saw: 

No results found 

That happened because the database table didn't contain any contract records 


Step 11 — Enter Contract Data 

After publishing, open the Fiori Preview, click Create, enter the contract details, and click Save. 

Step 12 — Verify Data 

Check that the saved contract is displayed correctly in the Fiori table. 

Step 13 — Check Contract Expiry 

Check the Contract End Date to identify contracts that are close to expiry. 

Step 14 — Renewal Status 

If the contract is close to expiry, set Renewal Required = YES. 

Step 15— Contract Renewal Notice 

Use the contract details to prepare the Contract Renewal Notice.
