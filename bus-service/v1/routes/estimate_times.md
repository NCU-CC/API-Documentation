# Get Bus Estimate Times of Specific Route

```
GET /routes/{routeId}/estimate_times
```

## Description
> Get bus estimate times of specific route

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
    <td>specific route id</td>
  </tr>
</table>

**※ routeId can only be one of 133 `(133)`, 3220 `(132)`, 3221 `(172)`, 3222 `(132_A)`**

## Example
```
GET /routes/3220/estimate_times
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
            "Route": {
                "EstimateTime": [
                    {
                        "StopName": "中壢公車站",
                        "ests": "",
                        "StopID": "0180",
                        "seqNo": 1,
                        "IVRNO": 180,
                        "GoBack": 1,
                        "comeTime": "14:30",
                        "SID": 5642,
                        "carId": "",
                        "schId": "851336_1_20151230143000",
                        "comeCarid": "",
                        "Value": null,
                        "EXTVoiceNo": "0578"
                    },
                    {
                        "StopName": "第一銀行",
                        "ests": "",
                        "StopID": "0565",
                        "seqNo": 2,
                        "IVRNO": 565,
                        "GoBack": 1,
                        "comeTime": "14:30",
                        "SID": 1200,
                        "carId": "",
                        "schId": "851336_1_20151230143000",
                        "comeCarid": "",
                        "Value": null,
                        "EXTVoiceNo": "0588"
                    }
                ],
                "id": 3220
            }
        }
    }
}
```
