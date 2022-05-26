# API Quick Start Guide

The D4H Readiness & Response API is an interface for querying information from and executing changes or updates in your response team's account.\


Want to find out what you can do with our API? You'll find basic information about the available endpoints and authentication at [https://api.d4h.org/v2/documentation](https://api.d4h.org/v2/documentation). \


Authentication is done using a token that you can obtain in your Personal Settings. Account owners must enable third-party API access first which is done in the Team Settings menu.\


#### DEVELOPER TIPS: 

* Remember to use the appropriate URL based on your response team's server. ([api.ca.d4h.org](https://api.ca.d4h.org/), [api.eu.d4h.org](https://api.eu.d4h.org/));
* HTTPS is mandatory;
* When an error is encountered in your request, most will contain precise info about what is wrong. \
  Eg. `field "category_id" must be a number"` or `field "activity" must be one of "incident", "event", "exercise"`\

* HTTP codes are meaningful:\

  * 400: an issue with your requests' parameters;
  * 401: an issue with your token or authentication;
  * 403: an issue with the user's permissions;
  * 404: a not found - it may either be an incorrect URL or an entity that no longer exists;
  * 409: a conflict, eg a start date that is before an end date;
  * 500: a server error (those shouldn't happen, but if they're ever encountered, get in touch with support!)
  * ...etc. A full list - this is a web standard - is available [here (official)](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html), or a friendlier version [here](https://httpstatuses.com/).\

* The authentication method is a bearer token. All requests require a header field called `Authorization` with value `Bearer <yourtokengoeshere>`
* API tokens are unique to each team member. Any write action done using an API token will be reflected in the application using that member's credentials (audit, etc). When building applications or integrations, never distribute a token with it. Protect it like you would protect a password.\
