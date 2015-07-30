# Authorization Code

```
GET /oauth/authorize
```

## Description
> authorize the client permission request

# Request
## Query Parameters
<table>
  <tr>
    <td><b>Name</b></td>
    <td><b><b>Required</b></b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
	<td><b>response_type</b></td>
	<td><i>yes</i></td>
	<td>value must be <code>code</code></td>
  </tr>
  <tr>
	<td><b>scope</b></td>
	<td><i>yes</i></td>
	<td>required permissions</td>
  </tr>
  <tr>
	<td><b>client_id</b></td>
	<td><i>yes</i></td>
	<td>your client id</td>
  </tr>
  <tr>
    <td><b>state</b></td>
    <td><i>no</i></td>
    <td>check string, you can get same state in response</td>
  </tr>
</table>

## Example
```
GET /oauth/authorize?response_type=code&scope=CLASS_READ+CLASS_WRITE&client_id=ABC123
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
        <td>code</td>
        <td>string</td>
        <td>used to exchange access token</td>
    </tr>
    <tr>
        <td>state</td>
        <td>string</td>
        <td>present if provided in request</td>
    </tr>
</table>

## Example

```json
{
    "code" : "SplxlOBeZQQYbYS6WxSbIA"
}
```



