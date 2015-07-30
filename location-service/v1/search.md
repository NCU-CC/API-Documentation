# Search By Keywords.

```
GET /search
```

## Description
> Search location of landscapes, buildings or faculties by keywords.

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
    <td>your API token</td>
  </tr>
</table>
## Query parameters
<table>
  <tr>
    <td><b>Name</b></td>
    <td><b><b>Required</b></b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
    <td><b>q</b></td>
    <td><i>yes</i></td>
    <td>keywords</td>
  </tr>
  <tr>
	<td><b>size</b></td>
	<td><i>no</i></td>
	<td>1 &lt;= size &lt;= 5, defaults to 3.</td>
  </tr>
</table>

## Example
```
GET /search?q=志希
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
       <td>place's Chinese name</td>
    </tr>
    <tr>
       <td>englishName</td>
       <td>String</td>
       <td>place's English name</td>
    </tr>
    <tr>
        <td>type</td>
        <td>Enum</td>
        <td>[Place Type]</td>
    </tr>
    <tr>
       <td>location</td>
       <td>LatLng</td>
        <td>
            latlng object
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
        "chineseName" : "志希館",
        "englishName" : "Zhi-Xi Building",
        "type" : "ADMINISTRATION",
        "location" : {
            "lat" : 24.970126,
            "lng" : 121.193683
        }
    }
]
```
## Notes
- [Place Type](places.md#place-type)
