# Get Status of Course Selection System

```
GET /status
```

## Description
> Get Status of Course Selection System.

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

## Example
```
GET /status
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
        <td>semester</td>
        <td>String</td>
        <td>4 digits, 3 for MinGuo year, 1 for semester.</td>
    </tr>
	<tr>
		<td>stage</td>
		<td>String</td>
		<td>current course selection stage.</td>
	</tr>
</table>

## Example
```json
{
	"semester" : 1031,
	"stage" : "校際選課"
}
```