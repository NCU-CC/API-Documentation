# Read Event

```
Get /event
```

## Description
> Returns an event.

## Required Scope
- calendar.event.read

# Request

## Headers
<table>
    <tr>
        <th>Name</th>
        <th>Required</th>
        <th>Description</th>
    </tr>
    <tr>
        <td><b>Authorization</b></td>
        <td>yes</td>
        <td>Bearer token.</td>
    </tr>
</table>

## Query Parameters

<table>
    <tr>
        <th>Name</th>
        <th>Required</th>
        <th>Description</th>
        <th>Data Type</th>
    </tr>
    <tr>
        <td><b>id</b></td>
        <td><i>yes</i></td>
        <td>Event identifier.</td>
        <td>string</td>
    </tr>
</table>

## Example
```
GET /event?id=5o4510qqjm3ccjd4k7i0fu15so
```

# Response

## Formats
- json

## Structure
[Event Objects](README.md#structure)

## Example
[Event Example](README.md#example)
