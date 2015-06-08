# Search Course Information

```
GET /search
```

## Description
> Search course information at current semester.

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

## Query Parameter
<table>
  <tr>
    <td><b>Name</b></td>
    <td><b>Required</b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
	<td><b>dept</b></td>
	<td><i>no</i></td>
	<td>department id</td>
  </tr>
  <tr>
	<td><b>week</b></td>
	<td><i>no</i></td>
	<td>
		<table>
			<tr>
				<td>0</td>
				<td>Monday</td>
			</tr>
			<tr>
				<td>1</td>
				<td>Tuesday</td>
			</tr>
			<tr>
				<td>2</td>
				<td>Wednesday</td>
			</tr>
			<tr>
				<td>3</td>
				<td>Thursday</td>
			</tr>
			<tr>
				<td>4</td>
				<td>Friday</td>
			</tr>
			<tr>
				<td>5</td>
				<td>Saturday</td>
			</tr>
			<tr>
				<td>6</td>
				<td>Sunday</td>
			</tr>
		</table>
	</td>
  </tr>
  <tr>
	<td><b>period</b></td>
	<td><i>no</i></td>
	<td>1,2,3,4,Z,5,6,7,8,9,A,B,C,D,E,F</td>
  </tr>
  <tr>
	<td><b>limit</b></td>
	<td><i>no</i></td>
	<td>1 &lt;= limit &lt;= 500, defaults to 30.</td>
  </tr>
  <tr>
	<td><b>keyword</b></td>
	<td><i>no</i></td>
	<td>at most 3</td>
  </tr>
</table>

## Example
```
GET /search?period=2&week=3
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