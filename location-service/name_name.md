# Find By Name

```
GET /place/name/{name}
```

## Description
> Find location of landscapes, buildings or faculties by its **Chinese** name.

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
GET /place/name/志希館
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
			Result Object
            <table>
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
					<td>Place Type</td>
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
			"chineseName" : "志希館",
			"englishName" : "Zhi-Xi Building",
			"type" : "ADMINISTRATION",
			"location" : {
				"lat" : 24.970126,
				"lng" : 121.193683
			}
		}
	]
}
```
## Notes
- [Place Type](type.md#place-type)
