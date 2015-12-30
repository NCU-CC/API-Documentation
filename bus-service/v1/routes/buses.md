# Get Buses Info of Specific Route

```
GET /routes/{routeId}/buses
```

## Description
> Get buses info of specific route

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

## Variables
<table>
  <tr>
    <td><b>Name</b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
    <td><b>routeId</b></td>
    <td>specific route id, it can only be one of <br>133 `(133)`, 3220 `(132)`, 3221 `(172)`, 3222 `(132_A)` </td>
  </tr>
</table>

## Example
```
GET /routes/3220/buses
```

# Response

## Formats
- json

## Example
```json
{
    "BusDynInfo": {
        "EssentialInfo": {
            "Location": {
                "CenterName": "",
                "CoordinateSystem": "",
                "name": "Maxwin",
                "UpdateTime": "2015-12-25 00:00:00"
            }
        },
        "BusInfo": {
            "BusData": [
                {
                    "ProviderID": 1,
                    "Speed": 0,
                    "BusID": "585-FD_o",
                    "ledstate": 0,
                    "Latitude": 24.940469,
                    "DataTime": "2015-12-30 13:44:45",
                    "RouteID": 3220,
                    "GoBack": 2,
                    "Longitude": 121.223892,
                    "sections": 1,
                    "Azimuth": 352,
                    "DutyStatus": 0,
                    "BusStatus": 98
                }
            ]
        }
    }
}
```
