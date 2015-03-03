# Find Information of Faculties

```
GET /person/name/{facultyName}
```

## Description
> Find faculty's information by his/her **Chinese** name.

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
GET /person/name/王小明
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
			Person Object
            <table>
                <tr>
                    <td>chineseName</td>
                    <td>String</td>
                    <td>faculty's Chinese name</td>
                </tr>
                <tr>
                    <td>englishName</td>
                    <td>String</td>
                    <td>faculty's English name</td>
                </tr>
                <tr>
                    <td>title</td>
                    <td>String</td>
                    <td>faculty's title</td>
                </tr>
                <tr>
                    <td>primaryUnit</td>
                    <td>[Unit Object]</td>
                    <td>primary unit</td>
                </tr>
                <tr>
                    <td>secondaryUnit</td>
                    <td>[Unit Object]</td>
                    <td>secondary unit</td>
                </tr>
				<tr>
					<td>officePhone</td>
					<td>Tel</td>
					<td>faculty's office extension</td>
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
			"chineseName" : "王小明",
			"englishName" : "Wang, Xiao Ming",
			"title" : "助理",
			"primaryUnit" : {
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
			"secondaryUnit" : {
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
			},
			"officePhone" : "99999"
		}
	]
}
```
## Notes
- [Unit Object](name_unitName.md#structure)
