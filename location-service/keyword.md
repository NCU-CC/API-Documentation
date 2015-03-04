# Find by keyword

```
GET /place/name/{keyword}
```

## Description
> Find location of landscapes, buildings or faculties by keywords using fuzzy search.

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
GET /place/name/王
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
                    <td>word</td>
                    <td>String</td>
                    <td>name</td>
                </tr>
                <tr>
                    <td>type</td>
                    <td>Enum</td>
                    <td>One of {PERSON, PLACE, UNIT}</td>
                </tr>
            </table>
        </td>
    </tr>
</table>

## Example
```json
{
	"result":[
		{
			"word":"王小明",
			"type":"PERSON"
		},
		{
			"word":"王大明",
			"type":"PERSON"
		},
		{
			"word":"王中明",
			"type":"PERSON"
		}
	]
}
```
## Notes
1. Separate keywords by space.
2. Keywords are supported in both Chinese and English.
