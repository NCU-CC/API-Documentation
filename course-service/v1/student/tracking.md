# Get Tracking Courses

```
GET /student/tracking
```

## Description
> Get student's tracking courses by OAuth token.

## Authorization

You have to use OAuth 2.0 to access.

## Required Scope
- CLASS_READ

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
        <td>Your API token</td>
    </tr>
    <tr>
        <td><b>Authorization</b></td>
        <td><i>yes</i></td>
        <td>Your OAuth token, in form of <code>Bearer XXX</code></td>
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
[Course Object](../../course/course.md#structure)

## Example
[Course Example](../../course/course.md#example-1)