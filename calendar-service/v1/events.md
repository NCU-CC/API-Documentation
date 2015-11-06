# Read Events

```
GET /events
```

## Description
> Returns events.

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
        <td><b>from</b></td>
        <td><i>yes</i></td>
        <td>Lower bound (inclusive) to filter by.</td>
        <td>date-time</td>
    </tr>
    <tr>
        <td><b>to</b></td>
        <td><i>yes</i></td>
        <td>Upper bound (exclusive) to filter by.</td>
        <td>date-time</td>
    </tr>
    <tr>
        <td><b>limit</b></td>
        <td><i>no</i></td>
        <td>Maximum number of events returned on one result page. (Default: 5)</td>
        <td>integer</td>
    </tr>
    <tr>
        <td><b>page</b></td>
        <td><i>no</i></td>
        <td>Which result page to return. (Default: 1)</td>
        <td>integer</td>
    </tr>
    <tr>
        <td><b>category</b></td>
        <td><i>no</i></td>
        <td>Category of events to filter by.</td>
        <td>string</td>
    </tr>
    <tr>
        <td><b>orderBy</b></td>
        <td><i>no</i></td>
        <td>The order of the events returned in the result and filter by. The value must be "start", "end", "created_at" or "updated_at". (Default: start)</td>
        <td>string</td>
    </tr>
</table>

## Example
```
GET /events?from=2015-01-01T00%3A00%3A00.000Z&to=2016-01-01T00%3A00%3A00.000Z&limit=5&page=1&category=%E5%AD%B8%E7%94%9F&orderBy=start
```

# Response

## Formats
- json

## Structure
<table>
   <tr>
      <th>Field Name</th>
      <th>Type</th>
      <th>Value Description</th>
   </tr>
   <tr>
      <td>events</td>
      <td>array</td>
      <td>List of <a href="event/README.md#structure">Event Objects</a></td>
   </tr>
   <tr>
      <td>count</td>
      <td>integer</td>
      <td>Number of events.</td>
   </tr>
   <tr>
      <td>page</td>
      <td>integer</td>
      <td>Page number of events.</td>
   </tr>
</table>


## Example
```json
{
  "events": [
    {
      "id": "a2frtf13cuaqhit9pf26lqmvr4",
      "created_at": "2015-11-03T07:45:34.000+08:00",
      "updated_at": "2015-11-03T07:45:34.000+08:00",
      "summary": "Test Summary1",
      "description": "Test Description1",
      "location": "Test Location1",
      "category": "學生",
      "start": "2016-01-01T08:00:00.000+08:00",
      "end": "2016-07-01T09:00:00.000+08:00",
      "link": "http://example1.com"
    },
    {
      "id": "bitvsriapjap4023c75d7mints",
      "created_at": "2015-11-03T07:45:54.000+08:00",
      "updated_at": "2015-11-03T07:45:54.000+08:00",
      "summary": "Test Summary2",
      "description": "Test Description2",
      "location": "Test Location2",
      "category": "學生",
      "start": "2016-07-01T08:00:00.000+08:00",
      "end": "2017-01-01T09:00:00.000+08:00",
      "link": "http://example2.com"
    }
  ],
  "count": 2,
  "page": 1
}
```
