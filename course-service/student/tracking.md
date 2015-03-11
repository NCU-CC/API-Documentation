# Get Tracking Courses

```
GET /student/tracking
```

## Description
> Get tracking courses.

## Authorization
OAuth 2.0
> We have a [Android client library](https://github.com/NCU-CC/OAuth-Service/tree/master/oauth-client-android)

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
GET /student/tracking
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
        <td>[Course Object]</td>
    </tr>
</table>

## Example
- [Course Example](course/course.md#example)

## Notes
- [Course Object](course/course.md#structure)