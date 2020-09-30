---
author: Veracity
description: Description of access to API
---

# Accessing APIs

For all requests you need to provide an **authorization** header withaan OAuth2 bearer token and an **Ocp-Apim-Subscription-Key** header with your subscription key  
  

More info about getting a bearer token can be found [here](https://developer.veracity.com/doc/identity).  
 Your subscription key can be found via your [profile](https://api-portal.veracity.com/developer).  

 Example request:

    GET https://api.veracity.com/veracity/datafabric/data/api/1/users/me HTTP/1.1
    Host: api.veracity.com
    Content-Type: application/json
    Ocp-Apim-Subscription-Key: {subscription-Key}
    Authorization: Bearer {token} 
