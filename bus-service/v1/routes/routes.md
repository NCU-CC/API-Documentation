# Get Routes of Bus

```
GET /routes
```

## Description
> Get all routes of bus

# Request
## Headers
<table>
  <tr>
    <td><b>Name</b></td>
    <td><b>Required</b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
    <td><b>X-NCU-API-TOKEN</b></td>
    <td><i>yes</i></td>
    <td>Your API token</td>
  </tr>
</table>

## Example
```
GET /routes
```

# Response

## Formats
- json

## Example
```json
{
    "BusDynInfo": {
        "EssentialInfo": {
            "CoordinateSystem": "",
            "UpdateTime": "2015-12-25 00:00:00",
            "Location": {
                "CenterName": "Maxwin",
                "name": "TYBUS"
            }
        },
        "BusInfo": {
            "Route": [
                {
                    "ProviderId": 1,
                    "departureZh": "中壢",
                    "gxcode": 3010,
                    "RouteType": "RTY",
                    "MasterRouteDesc": "RG",
                    "ddesc": "中壢<->桃園",
                    "nameZh": 1,
                    "destinationZh": "桃園",
                    "MasterRouteNo": "",
                    "ID": 3010,
                    "MasterRouteName": " "
                }
            ]
        }
    }
}
```