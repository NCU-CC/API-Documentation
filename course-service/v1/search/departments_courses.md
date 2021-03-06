# Search Course Information By Department

```
GET /departments/{departmentId}/courses
```

## Description
> Search course information by department.

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
GET /departments/deptI1I1000I0/courses
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
        <td>[Course Object]</td>
    </tr>
</table>

## Example
- [Course Example](../course/course.md#example-1)

## Notes
- [Course Object](../course/course.md#structure)