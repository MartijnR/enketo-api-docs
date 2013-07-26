---
category: survey
path: '/survey'
title: 'De-activate a survey'
type: 'DELETE'
params: 'server_url form_id'
codes: [200, 400, 401, 403, 404, 405, 410]
layout: nil
---

### Request

* required parameter **`server_url`** is the url of the OpenRosa server your form is hosted on.
* required parameter **`form_id`** is the ID of the form previously listed in _SERVER_/formList.
* if the form is still listed in the _SERVER_/formList, the response will have code 405!
* The headers must include a **valid authentication token**.

```Authentication: basic API_TOKEN:```

### Response

Sends back an object including a url property.

```Status: 204 OK (found in db, checked that it is no longer listed in /formList, and de-activated)```
```{
    code: '204'
}```