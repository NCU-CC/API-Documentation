# API-Documentation
Documentation for National Central University API

## Root URL
```
https://api.cc.ncu.edu.tw
```

## Authorization

You have to register a client at [oauth management website](https://api.cc.ncu.edu.tw/manage) first before making any API calls.
There are two situations to use our API:

- access resources with personal information : 
    1. follow the **OAuth2** flow to get an **access token**, see [documentation](oauth-service/README.md)
    2. follow the documentation of API to append access token
- access resources without personal information :
    1. get an **api token** from client management page of [oauth management website](https://api.cc.ncu.edu.tw/manage) 
    2. follow the documentation of API to append api token

## Language
Some NCU APIs are bilingual(zh-TW, en-US) and default to zh-TW. Use **Accept-Language** header to specify your language.

## Encoding
All strings are encoded in UTF-8.

## Endpoints

##### [Activity-Service]
> /activity/v3
- [/activities](activity-service/v3/activities.md)
- [/announces](activity-service/v3/announces.md)
- [/clubs](activity-service/v3/clubs.md)

##### [Location-Service]
> /location/v3
- [/search](location-service/v3/search.md)
- [/places](location-service/v3/places.md)
- [/units](location-service/v3/units.md)
- [/faculties](location-service/v3/faculties.md)
- [/buildings](location-service/v3/buildings.md)

##### [Course-Service]
> /course/v1
- [/student/selected](course-service/v1/student/selected.md)
- [/student/tracking](course-service/v1/student/tracking.md)

## Errors

HTTP Status Code | Description       
---------------- | -----------------
400              | invalid body or parameter 
403              | access a protected resource without correct access token
404              | requested resource not found
500              | internal server error

## Problems?
If you have any problems, please file a issue or just send us pull requests.
Any pull requests submitted to master branch are not allowed, please submit to **develop** branch.

## Format Reference
The format of this document refer to [Documentation for University of Waterloo API](https://github.com/uWaterloo/api-documentation).

## License
MIT License Copyright © 2015-2015 Computer Center, National Central University

[API management page]:https://api.cc.ncu.edu.tw/manage
[Location-Service]:https://github.com/NCU-CC/Location-Service
[Course-Service]:https://github.com/NCU-CC/Course-Service
