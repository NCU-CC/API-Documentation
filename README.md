# API-Documentation
Documentation for National Central University API

## Root URL
```
https://api.cc.ncu.edu.tw
```

## Authorization
1. Register your client at [oauth management page]()
2. Get the [API token](oauth-service/api_token.md) before making API calls
3. Place API token in request header with key **X-NCU-API-TOKEN**

## Personal Resource
Some APIs can access personal information, we use OAuth2 to protect them, see [documentation](oauth-service/README.md)

## Language
Some NCU APIs are bilingual(zh-TW, en-US) and default to zh-TW. Use **Accept-Language** header to specify your language.

## Encoding
All strings are encoded in UTF-8.

## Endpoints
##### [Location-Service]
> /location
- [/place](location-service/place.md)
- [/search](location-service/search.md)
- [/unit](location-service/unit.md)
- [/unit/{unitFullName}](location-service/unit_unitName.md)
- [/faculty/{facultyName}](location-service/faculty.md)
- [/building](location-service/building.md)

##### [Course-Service]
> /course
- [/status](course-service/status.md)
- [/unit/college](course-service/unit/college.md)
- [/unit/college/{collegeId}/department](course-service/unit/college_department.md)
- [/unit/department/{departmentId}/target](course-service/unit/department_target.md)
- [/serach](course-service/search/search.md)
- [/search/department/{departmentId}](course-service/search/department.md)
- [/search/target/{target}](course-service/search/target.md)
- [/search/summer/{stage}](course-service/search/summer.md)
- [/course/{serialNo}](course-service/course/course.md)
- [/course/{serialNo}/limit](course-service/course/limit.md)
- [/student/{studentId}/selected](course-service/student/selected.md)
- [/student/{studentId}/tracking](course-service/student/tracking.md)

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