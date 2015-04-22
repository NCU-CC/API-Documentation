# Find Administrative and Research Units.

```
GET /units
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
  	<td><b>fname</b></td>
  	<td><i>yes</i></td>
  	<td>unit's full Chinese name</td>
    </tr>
  <tr>
	<td><b>building_cname</b></td>
	<td><i>yes</i></td>
	<td>place's full Chinese name</td>
  </tr>
  <tr>
	<td><b>size</b></td>
	<td><i>no</i></td>
	<td>1 &lt;= size &lt;= 50, defaults to 5.</td>
  </tr>
</table>

**fname** and **building_cname** are exclusive

## Example

```
GET /units?fname=電子計算機中心
```

```
GET /units?building_cname=志希館
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
		<td>unitCode</td>
		<td>String</td>
		<td>unit's code</td>
	</tr>
	<tr>
		<td>chineseName</td>
		<td>String</td>
		<td>unit's name Chinese name</td>
	</tr>
	<tr>
		<td>englishName</td>
		<td>String</td>
		<td>unit's name English name</td>
	</tr>
	<tr>
		<td>shortName</td>
		<td>String</td>
		<td>abbreviation of unit's Chinese name</td>
	</tr>
	<tr>
		<td>fullName</td>
		<td>String</td>
		<td>unit's official Chinese name</td>
	</tr>
	<tr>
		<td>url</td>
		<td>URL</td>
		<td>unit's website</td>
	</tr>
	<tr>
		<td>location</td>
		<td>LatLng</td>
		<td>
			LatLng Object
			<table>
				<tr>
					<td>lat</td>
					<td>Latitude</td>
				</tr>
				<tr>
					<td>lng</td>
					<td>Longitude</td>
				</tr>
			</table>
		</td>
	</tr>
</table>

## Example
```json
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
```
