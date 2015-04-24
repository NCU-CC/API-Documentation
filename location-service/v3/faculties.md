# Find Information of Faculties

```
GET /faculties
```

## Description
> Find faculty's information by his/her **Chinese** name.

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
    <td>your API token</td>
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
	<td><b>cname</b></td>
	<td><i>yes</i></td>
	<td>faculty's Chinese name</td>
  </tr>
</table>

## Example
```
GET /faculties?cname=王小明
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

## Example
```json
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
```
## Notes
- [Unit Object](units.md#structure)
