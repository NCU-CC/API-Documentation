# Get Providers of Bus

```
GET /providers
```

## Description
> Get all providers of bus

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
GET /providers
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
            "Provider": [
                {
                    "nameZh": "桃園客運",
                    "ID": 1,
                    "type": 0
                },
                {
                    "nameZh": "中壢客運",
                    "ID": 2,
                    "type": 0
                },
                {
                    "nameZh": "統聯客運",
                    "ID": 4,
                    "type": 0
                },
                {
                    "nameZh": "新竹客運",
                    "ID": 5,
                    "type": 0
                },
                {
                    "nameZh": "亞通客運",
                    "ID": 6,
                    "type": 0
                },
                {
                    "nameZh": "金台通運(免巴)",
                    "ID": 8,
                    "type": 2
                },
                {
                    "nameZh": "桃園客運(免巴)",
                    "ID": 21,
                    "type": 2
                },
                {
                    "nameZh": "亞通客運(免巴)",
                    "ID": 22,
                    "type": 2
                }
            ]
        }
    }
}
```