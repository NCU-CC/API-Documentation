# Operations about event
- [POST /event](post.md)
- [GET /event](get.md)
- [PUT /event](put.md)
- [DELETE /event](delete.md)

# Structure
<table>
   <tr>
      <th>Field Name</th>
      <th>Type</th>
      <th>Value Description</th>
   </tr>
   <tr>
      <td>id</td>
      <td>string</td>
      <td>Event identifier.</td>
   </tr>
   <tr>
      <td>created_at</td>
      <td>string</td>
      <td>Creation time of the event.</td>
   </tr>
   <tr>
      <td>update_at</td>
      <td>string</td>
      <td>Last modification time of the event.</td>
   </tr>
   <tr>
      <td>summary</td>
      <td>string</td>
      <td>Title of the event.</td>
   </tr>
   <tr>
      <td>description</td>
      <td>string</td>
      <td>Description of the event.</td>
   </tr>
   <tr>
      <td>location</td>
      <td>string</td>
      <td>Geographic location of the event.</td>
   </tr>
   <tr>
      <td>category</td>
      <td>string</td>
      <td>Category of the event.</td>
   </tr>
   <tr>
      <td>start</td>
      <td>string</td>
      <td>The start time of the event.</td>
   </tr>
   <tr>
      <td>end</td>
      <td>string</td>
      <td>The end time of the event.</td>
   </tr>
   <tr>
      <td>link</td>
      <td>string</td>
      <td>URL link of the event.</td>
   </tr>
</table>

# Example
```json
{
  "id": "5o4510qqjm3ccjd4k7i0fu15so",
  "created_at": "2015-11-03T07:13:41.230+08:00",
  "updated_at": "2015-11-03T07:13:41.230+08:00",
  "summary": "Test Summary",
  "description": "Test Description",
  "location": "Test Location",
  "category": "學生",
  "start": "2016-01-01T08:00:00.000+08:00",
  "end": "2016-01-01T09:00:00.000+08:00",
  "link": "http://example.com"
}
```
