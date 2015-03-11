# API-Documentation
Documentation for National Central University API

## Authorization
You must get the API token before making API calls. 

1.  Go to [API management page], and login with NCU portal to get the public API token.
2.  Place API token in header key **X-NCU-API-TOKEN** and value **token**

## Root URL
```
https://api.cc.ncu.edu.tw
```

## Endpoints
##### [Location-Service]
> /location
- [/place](location-service/place.md)
- [/search](location-service/search.md)
- [/unit](location-service/unit.md)
- [/unit/{unitFullName}](location-service/unit_unitName.md)
- [/faculty/{facultyName}](location-service/faculty.md)
- [/building](location-service/building.md)

## Problems?
If you have any problems, please file a issue or just send us pull requests.
Any pull requests submitted to master branch are not allowed, please submit to **develop** branch.

## Format Reference
The format of this document refer to [Documentation for University of Waterloo API](https://github.com/uWaterloo/api-documentation).

## License
MIT License Copyright © 2015-2015 Computer Center, National Central University

[API management page]:https://api.cc.ncu.edu.tw/manage
[Location-Service]:https://github.com/NCU-CC/Location-Service
