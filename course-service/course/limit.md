# Find Course Limitation

```
GET /course/{serialNo}/limit
```

## Description
> Find course limitation.

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
## Query Parameter
<table>
  <tr>
    <td><b>Name</b></td>
    <td><b>Required</b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
	<td><b>semester</b></td>
	<td><i>no</i></td>
	<td>year + semester
		<table>
			<tr>
				<td>year</td>
				<td>3 digits of MinGuo year</td>
			</tr>
			<tr>
				<td>semester</td>
				<td>1 digit of semester, 1 for top and 2 for bottom.</td>
			</tr>
		</table>
		defaults to current semester.
	</td>
  </tr>
</table>

## Example
```
GET /course/12034/limit?semester=1031
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
        <td>
			Limitation Object
            <table>
                <tr>
                    <td>serialNo</td>
                    <td>String</td>
                    <td>course id, 5 digits and left padding 0.</td>
                </tr>
                <tr>
                    <td>no</td>
                    <td>String</td>
                    <td>course number</td>
                </tr>
                <tr>
                    <td>name</td>
                    <td>String</td>
                    <td>course name</td>
                </tr>
				<tr>
					<td>memos</td>
					<td>Array</td>
					<td>all strings</td>
				</tr>
            </table>
        </td>
    </tr>
</table>

## Example
```json
{
	"result" : 
	[
        {
			"serialNo" : "91001",
			"no" : "LA4001",
			"name" : "文學與劇場",
			"memos" : [
				"學院:限文學院。 年級:限三年級、四年級",
				"學院:限非文學院。 年級:限三年級、四年級"
			]
        }
    ]
}
```