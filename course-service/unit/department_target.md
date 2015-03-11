# Find Targets.

```
GET /unit/department/{departmentId}/target
```

## Description
> Find targets that departments running courses for.

# Request
## Headers
<table>
  <tr>
    <td><b>Name</b></td>
    <td><b><b>Required</b></b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
    <td><b>X-API-NCU-TOKEN</b></td>
    <td><i>yes</i></td>
    <td>Your public API token</td>
  </tr>
</table>

## Example
```
GET /unit/department/{departmentId}/target
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
			Target Object
            <table>
                <tr>
                    <td>name</td>
                    <td>String</td>
                    <td>target name</td>
                </tr>
                <tr>
                    <td>id</td>
                    <td>String</td>
                    <td>target Id</td>
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
          'name' : '中國文學系[不分類]',
          'id' : 'cofuZdeptI1I1001I0ZcofgI0'
        },
        {
          'name' : '中國文學系[一年級]',
          'id' : 'cofuZdeptI1I1001I0ZcofgI1'
        }
    ]
}
```