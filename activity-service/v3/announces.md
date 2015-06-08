# Find Announces

```
GET /announces
```

## Description
> Find announces by condition

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
    <td>your API token</td>
  </tr>
</table>
## Query Parameters
<table>
	<tr>
		<td><b>Name</b></td>
		<td><b><b>Required</b></b></td>
		<td><b>Description</b></td>
	</tr>
	<tr>
		<td><b>size</b></td>
		<td><i>no</i></td>
		<td>fetch size, 1 ~ 40, default to 20</td>
	</tr>
	<tr>
		<td><b>type</b></td>
		<td><i>yes</i></td>
		<td>announce type</td>
	</tr>
	<tr>
		<td><b>older_than</b></td>
		<td><i>no</i></td>
		<td>query announces older than specified id</td>
	</tr>
	<tr>
		<td><b>newer_than</b></td>
		<td><i>no</i></td>
		<td>query announces newer than specified id</td>
	</tr>
</table>

if **older_than** and **newer_than** are presented at same time, only **older_than** is considered

## Announce Type

<table>
	<tr>
		<td>type</td>
		<td>description</td>
	</tr>
	<tr>
		<td>common</td>
		<td>一般公告</td>
	</tr>
	<tr>
		<td>group</td>
		<td>組務公告</td>
	</tr>
</table>

## Example

```
GET /announces?size=2&type=common   ( latest announces with common type )
```

```
GET /announces?size=2&type=group&older_than=10   ( group announces older than the announce whose id = 10 )
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
		<td>id</td>
		<td>Integer</td>
		<td>announce id</td>
	</tr>
	<tr>
		<td>title</td>
		<td>String</td>
		<td>announce title</td>
	</tr>
	<tr>
		<td>content</td>
		<td>String</td>
		<td>announce content</td>
	</tr>
	<tr>
		<td>time</td>
		<td>String</td>
		<td>announce created time</td>
	</tr>
	<tr>
		<td>attachment</td>
		<td>String</td>
		<td>announce attachement url</td>
	</tr>
</table>

## Example
```json
[
	{
		"id":1,
		"title":"變形金剛-舞台車車體視覺設計競圖大賽",
		"content":"內容",
		"time":"2015-05-01 15:42",
		"attachment": "http://www.api.com/file/file1.txt"
	},
	{
		"id":2,
		"title":"2015德明盃3D超商全國經營管理",
		"content":"內容",
		"time":"2015-05-01 15:28",
		"attachment":null
	}
]
```

```json
[[
	{
		"id":9,
		"title":"百年校慶創意市集攤位招募中",
		"content":"內容",
		"time":"2015-04-28 16:13",
		"attachment":null
	},
	{
		"id":6,
		"title":"103-2社團指導老師「授課費用」核定結果",
		"content":"內容",
		"time":"2015-04-09 14:19",
		"attachment":null
	}
]]
```
