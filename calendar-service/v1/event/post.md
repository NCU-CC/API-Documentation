# Create Event

```
POST /event
```

## Description
> Creates an event.

## Required Scope
- calendar.event.write

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

## Form-Data Parameters

<table>
    <tr>
        <th>Name</th>
        <th>Required</th>
        <th>Description</th>
        <th>Data Type</th>
    </tr>
    <tr>
        <td><b>summary</b></td>
        <td><i>yes</i></td>
        <td>Title of the event.</td>
        <td>string</td>
    </tr>
    <tr>
        <td><b>description</b></td>
        <td><i>yes</i></td>
        <td>Description of the event.</td>
        <td>string</td>
    </tr>
    <tr>
        <td><b>link</b></td>
        <td><i>no</i></td>
        <td>URL link of the event.</td>
        <td>string</td>
    </tr>
    <tr>
        <td><b>location</b></td>
        <td><i>yes</i></td>
        <td>Geographic location of the event.</td>
        <td>string</td>
    </tr>
    <tr>
        <td><b>category</b></td>
        <td><i>yes</i></td>
        <td>Category of the event.</td>
        <td>string</td>
    </tr>
    <tr>
        <td><b>start</b></td>
        <td><i>yes</i></td>
        <td>The start time of the event.</td>
        <td>date-time</td>
    </tr>
    <tr>
        <td><b>end</b></td>
        <td><i>yes</i></td>
        <td>The end time of the event.</td>
        <td>date-time</td>
    </tr>
</table>

## Example
```
POST /event
summary=Test%20Summary&description=Test%20Description&link=http%3A%2F%2Fexample.com&location=Test%20Location&category=%E5%AD%B8%E7%94%9F&start=2016-01-01T00%3A00%3A00.000Z&end=2016-01-01T01%3A00%3A00.000Z
```

# Response

## Formats
- json

## Structure
[Event Objects](README.md#structure)

## Example
[Event Example](README.md#example)
