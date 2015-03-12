# Find Administrative and Research Units.

```
GET /unit
```

## Description
> Find administrative and research units.

# Request
## Headers
<table>
  <tr>
    <td><b>Name</b></td>
    <td><b>Required</b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
    <td><b>X-API-NCU-TOKEN</b></td>
    <td><i>yes</i></td>
    <td>Your public API token</td>
  </tr>
</table>
## Query Parameters
<table>
  <tr>
    <td><b>Name</b></td>
    <td><b><b>Required</b></b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
	<td><b>buildingName</b></td>
	<td><i>no</i></td>
	<td>building's full Chinese name</td>
  </tr>
  <tr>
	<td><b>limit</b></td>
	<td><i>no</i></td>
	<td>1 &lt;= limit &lt;= 50, defaults to 5.</td>
  </tr>
</table>
## Example
```
GET /unit?building=志希館
```

# Response

## Formats
- json

## Structure
<table>
    <tr>
		<td><b>Field Name</b></td>
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
		}
	]
}
```
## Notes
- [Unit Object](unit_unitName.md#structure)
