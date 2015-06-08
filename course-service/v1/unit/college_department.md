# Find Departments By College.

```
GET /unit/college/{collegeId}/department
```

## Description
> Find departments by college.

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
GET /unit/college/deptI1I1000I0/department
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
			Department Object
            <table>
                <tr>
                    <td>name</td>
                    <td>String</td>
                    <td>department name</td>
                </tr>
                <tr>
                    <td>id</td>
                    <td>String</td>
                    <td>department Id</td>
                </tr>
            </table>
        </td>
    </tr>
</table>

## Example
```json
[
	{
		"name" : "文學院",
		"id" : "deptI1I1000I0"
	}, {
		"name" : "中國文學系",
		"id" : "deptI1I1001I0"
	}
]
```