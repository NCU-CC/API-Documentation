# API-Documentation
Documentation for National Central University API

## Authorization
You must get the API token before making API calls. 

1.  Go to [API management page], and login with NCU portal to get the API token.
2.  Place API token in header key **Authorization** and value **"Bearer " + token**

## Root URL
```
https://appstore.cc.ncu.edu.tw
```

## Endpoints
##### [Location-Service]
> /location/
- [/place/name/{name}](location-service/name_name.md)
- [/place/type/{placeType}](location-service/type.md)
- [/place/name/{buildingName}/units](location-service/name_buildingName.md)
- [/person/name/{employeeName}](location-service/name_employeeName.md)
- [/unit/name/{unitName}](location-service/name_unitName.md)
- [/keyword/{keyword}](location-service/keyword.md)

## Problems?
If you have any problems, please file a issue or just send us pull requests.
Any pull reqeusts submit to master branch are allowed, please submit to **develop** branch.

## Format Reference
The format of this document is refer to [Documentation for University of Waterloo API](https://github.com/uWaterloo/api-documentation).

## License
MIT License Copyright © 2015-2015 Computer Center, National Central University

[API management page]:https://appstore.cc.ncu.edu.tw/manage
[Location-Service]:https://github.com/NCU-CC/Location-Service
