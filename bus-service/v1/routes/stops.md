# Get Bus Stop Info of Specific Route

```
GET /routes/{routeId}/stops
```

## Description
> Get bus stop info of specific route

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
GET /routes/3220/stops
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
            "Stop": [
                {
                    "routeId": 3220,
                    "districtId": 1,
                    "seqNo": 1,
                    "nameZh": "中壢公車站",
                    "latitude": 24.953233,
                    "pgp": 0,
                    "Id": "0578",
                    "terminal": 0,
                    "GoBack": 1,
                    "EXTVoiceNO": 578,
                    "longitude": 121.224153,
                    "SID": 5642
                },
                {
                    "routeId": 3220,
                    "districtId": 1,
                    "seqNo": 2,
                    "nameZh": "第一銀行",
                    "latitude": "24.955120",
                    "pgp": 0,
                    "Id": "0588",
                    "terminal": 0,
                    "GoBack": 1,
                    "EXTVoiceNO": 588,
                    "longitude": 121.222093,
                    "SID": 1200
                }
            ]
        }
    }
}
```
