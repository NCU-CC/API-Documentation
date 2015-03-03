# Find Units by Building Name

```
GET /place/name/{buildingName}/units
```

## Description
> Find units by building name, including administrative and academic units.

# Request
## Parameters
<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b><b>Required</b></b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
    <td><b>token</b></td>
    <td><i>yes</i></td>
    <td>Your API token</td>
  </tr>
</table>

## Example
```
GET /place/name/志希館/units
```

# Response

## Formats
- json

## Structure
<table>
    <tr>
		<td><b>Filed Name</b></td>
		<td><b>Type</b></td>
		<td><b>Value Description</b></td>
	</tr>
    <tr>
        <td>result</td>
        <td>list</td>
        <td>[Unit Object]</td>
    </tr>
</table>

## Example
```json
{
	"result" : 
	[
		{
			"unitCode" : "T400",
			"chineseName" : "管理學院",
			"englishName" : "College of Management",
			"shortName" : "管理學院",
			"fullName" : "管理學院",
			"url" : "",
			"location" : null
		}, 
		{
			"unitCode" : "A800",
			"chineseName" : "電子計算機中心",
			"englishName" : "Computer Center",
			"shortName" : "電算中心",
			"fullName" : "電子計算機中心",
			"url" : "http://www.cc.ncu.edu.tw/introduction/member.php",
			"location" : {
				"lat" : 24.970128,
				"lng" : 121.193719
			}
		}, 
		{
			"unitCode" : "A800",
			"chineseName" : "電子計算機中心",
			"englishName" : "Computer Center",
			"shortName" : "電算中心",
			"fullName" : "電子計算機中心",
			"url" : "http://www.cc.ncu.edu.tw/introduction/member.php",
			"location" : {
				"lat" : 24.970128,
				"lng" : 121.193719
			}
		}
	]
}
```
[Unit Object]:/location-service/name_unitName.md#structure