# Find All Colleges.

```
GET /unit/college
```

## Description
> Find all colleges.

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
    <td>Your API token</td>
  </tr>
</table>

## Example
```
GET /unit/college
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
        <td>
			College Object
            <table>
                <tr>
                    <td>name</td>
                    <td>String</td>
                    <td>college name</td>
                </tr>
                <tr>
                    <td>id</td>
                    <td>String</td>
                    <td>college Id</td>
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
			"name" : "文學院",
			"id" : "deptI1I1000I0"
		},
		{
			"name" : "理學院",
			"id" : "deptI1I2000I0"
		}
	]
}
```