# Find Activities

```
GET /activities
```

## Description
> Find the latest activities

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
</table>

## Example

```
GET /activities?size=3
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
		<td>name</td>
		<td>String</td>
		<td>activity name</td>
	</tr>
	<tr>
		<td>club</td>
		<td>String</td>
		<td>activity sponsor</td>
	</tr>
	<tr>
		<td>place</td>
		<td>String</td>
		<td>activity place</td>
	</tr>
	<tr>
		<td>content</td>
		<td>String</td>
		<td>activity content</td>
	</tr>
	<tr>
		<td>start</td>
		<td>String</td>
		<td>activity start time</td>
	</tr>
	<tr>
		<td>end</td>
		<td>String</td>
		<td>activity end time</td>
	</tr>
</table>

## Example
```json
[
	{
		"name":"電機營輔訓",
		"club":"電機系學會",
		"place":"志道樓 - 一樓大活動室",
		"content":"試跑電機營第一天活動內容",
		"start":"2015-05-01 16:00",
		"end":"2015-05-01 22:00"
	},
	{
		"name":"成果展",
		"club":"手語社",
		"place":"志道樓 - 二樓小活動室",
		"content":"練習",
		"start":"2015-05-01 20:00",
		"end":"2015-05-01 22:00"
	},
	{
		"name":"中友週傳情",
		"club":"台中南投地區校友會",
		"place":"志道樓 - 擺攤宣傳區 66大順",
		"content":"舉辦傳情活動，藉由傳情的溫馨活動讓同學們可以傳達心意並且介紹台中美食，以增加社團之特色。",
		"start":"2015-05-01 12:00",
		"end":"2015-05-01 21:00"
	}
]
```
