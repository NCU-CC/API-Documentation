# Find Unit Information

```
GET /unit/name/{unitFullName}
```

## Description
> Find unit's information by unit's **FULL** Chinese name.

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
GET /unit/name/電子計算機中心
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
        <td>
			Unit Object
            <table>
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
        </td>
    </tr>
</table>

## Example
```json
{
	"result" :
	[
		{
			"unitCode" : "A830",
			"chineseName" : "校務資訊組",
			"englishName" : "Campus Information Management Division",
			"shortName" : "校務資訊組",
			"fullName" : "電子計算機中心-校務資訊組",
			"url" : "http://www.cc.ncu.edu.tw/introduction/member.php",
			"location" : {
				"lat" : 24.970128,
				"lng" : 121.193719
			}
		}
	]
}
```
