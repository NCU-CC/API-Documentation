# API-Documentation
Documentation for National Central University API

## Root URL
```
https://api.cc.ncu.edu.tw
```

## Authorization

Before you making any API calls, you have to register a client at [OAuth Management] first.
There are two situations to use our API:

- Access resources that contains personal information : 
    1. Follow the **OAuth 2.0** protocol to get an **access token**, see [documentation](oauth-service/README.md).
    2. Read the [documentation](oauth-service/README.md) to use **access token**.
- Access resources without personal information :
    1. Get an **api token** from [OAuth Management].
    2. Read the [documentation](oauth-service/README.md) to use **api token**.

## Internationalization
Some NCU APIs are bilingual(zh-TW, en-US) and default to zh-TW. Use **Accept-Language** header to specify your language.

## Encoding
All strings are encoded in UTF-8.

## Endpoints

##### [Activity-Service]
> /activity/v1
- [/activities](activity-service/v1/activities.md)
- [/announces](activity-service/v1/announces.md)
- [/clubs](activity-service/v1/clubs.md)

##### [Location-Service]
> /location/v1
- [/search](location-service/v1/search.md)
- [/places](location-service/v1/places.md)
- [/units](location-service/v1/units.md)
- [/faculties](location-service/v1/faculties.md)
- [/buildings](location-service/v1/buildings.md)

##### [Course-Service]
> /course/v1
- [/status](course-service/v1/status.md)
- [/colleges](course-service/v1/unit/college.md)
- [/colleges/{collegeId}/departments](course-service/v1/unit/college_department.md)
- [/departments/{departmentId}/targets](course-service/v1/search/departments_targets.md)
- [/departments/{departmentId}](course-service/v1/search/departments_courses.md)
- [/courses/{serialNo}](course-service/v1/course/course.md)
- [/courses/{serialNo}/limit](course-service/v1/course/limit.md)
- [/courses](course-service/v1/course/search.md)
- [/targets/{targetId}/courses](course-service/v1/search/target.md)
- [/summer/{stage}/courses](course-service/v1/search/summer.md)
- [/student/selected](course-service/v1/student/selected.md)
- [/student/rejected](course-service/v1/student/rejected.md)
- [/student/tracking](course-service/v1/student/tracking.md)

##### [Personnel-Service]
> /personnel/v1
- [/cards/{cardNumber}](personnel-service/v1/cards.md)
- [/info](personnel-service/v1/info.md)

## Error Status Code

HTTP Status Code | Description       
---------------- | -----------------
400              | invalid body or parameter.
401              | access a protected resource with an invalid token.
403              | access a protected resource with an token from invalid client.
404              | resource not found.
405              | invalid request method 
500              | internal server error.

## Problems?
If you have any problems, please file a issue or just send us pull requests.
Any pull requests submitted to master branch are not allowed, please submit to **develop** branch.
It would be appreciated that with brief descriptions and some unit tests to proof.

## Format Reference
The format of this document refer to [Documentation for University of Waterloo API](https://github.com/uWaterloo/api-documentation).

## License
MIT License Copyright © 2015-2015 Computer Center, National Central University

[OAuth Management]:https://api.cc.ncu.edu.tw/manage
[Activity-Service]:https://github.com/NCU-CC/Activity-Service
[Personnel-Service]:https://github.com/NCU-CC/Personnel-Service
[Location-Service]:https://github.com/NCU-CC/Location-Service
[Course-Service]:https://github.com/NCU-CC/Course-Service
