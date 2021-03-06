---
layout: dev_resources
title: Using the SAM API
nav: using_sam_api
---
### Using the SAM API

The SAM API is a GET API which has one operation. The operation will retrieve an entity's public information. Its endpoint is ```https://api.data.gov/sam/v1/registrations/```. 

A couple basic notes: the rate limits for the API are currently 5,000 calls/day and 5 calls per 5 seconds. As we go forward and understand the impact of usage of the API on SAM, we will adjust the limits accordingly as well as allow for individual users with specific needs to have customized rate limits appropriate to their use.

##### Example URL

Currently, the below URL won't work without you adding in an API key from api.data.gov. Replace ```<YOUR_API_KEY>``` with your api.data.gov provided API key in the below URL to successfully execute the call.

[https://api.data.gov/sam/v1/registrations/1459697830000?api_key=YOUR_API_KEY](https://api.data.gov/sam/v1/registrations/1459697830000?api_key=YOUR_API_KEY)

##### Retrieving entity information
The endpoint for getting all data begins with ```/v1/registrations```. 

The endpoint takes a single URL parameter which is the DUNS and DUNS+4 information concatenated. If the entity does not have a DUNS+4, the user should include ```0000```. 

For example, if an entity of interest has a DUNS number of ```012345678``` with no DUNS+4, the access to the endpoint would be at ```/sam/v1/registrations/0123456780000```. An entity with the same DUNS but with a DUNS+4 of ```9999``` would be accessed at ```/sam/v1/registrations/0123456789999```.

The data in the API is updated daily by approximately 2 AM Eastern time for the prior day's data.

##### Finding DUNS numbers to use
