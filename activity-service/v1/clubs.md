# Find Clubs

```
GET /clubs
```

## Description
> Find all clubs

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

## Example

```
GET /clubs
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
		<td>name</td>
		<td>String</td>
		<td>club name</td>
	</tr>
	<tr>
		<td>description</td>
		<td>String</td>
		<td>club description</td>
	</tr>
	<tr>
		<td>place</td>
		<td>String</td>
		<td>club working place</td>
	</tr>
	<tr>
		<td>website</td>
		<td>String</td>
		<td>club website</td>
	</tr>
</table>

## Example
```json
[
	{
		"name":"國文系學會",
		"description":"描述",
		"place":"國文系館",
		"website":"http://www.example.com"
	},
	{
		"name":"英文系學會",
		"description":"描述",
		"place":"英文系館",
		"website":"http://www.example.com"
	}
]
```
