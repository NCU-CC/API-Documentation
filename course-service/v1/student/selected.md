# Get Selected Courses

```
GET /student/selected
```

## Description
> Get student's selected courses.

## Required Scope
- course.schedule.read

# Request

## Headers
<table>
    <tr>
        <td><b>Name</b></td>
        <td><b>Required</b></td>
        <td><b>Description</b></td>
    </tr>
    <tr>
        <td><b>Authorization</b></td>
        <td><i>yes</i></td>
        <td>Your OAuth token in the form of <code>Bearer XXX</code></td>
    </tr>
</table>

## Example
```
GET /student/selected
```

# Response

## Formats
- json

## Structure
[Course Object](../course/course.md#structure)

## Example
[Course Example](../course/course.md#example-1)