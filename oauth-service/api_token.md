# Api Token

```
GET /oauth/token
```

## Description
> exchange api token by client credentials

# Request
## Query Parameters
<table>
  <tr>
    <td><b>Name</b></td>
    <td><b><b>Required</b></b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
	<td><b>grant_type</b></td>
	<td><i>yes</i></td>
	<td>it must be <code>client_credentials</code></td>
  </tr>
  <tr>
	<td><b>client_id</b></td>
	<td><i>yes</i></td>
	<td>your client id</td>
  </tr>
  <tr>
    <td><b>client_secret</b></td>
    <td><i>yes</i></td>
    <td>your client secret</td>
  </tr>
</table>

## Example
```
GET /oauth/token?grant_type=client_credentials&client_id=ABC123&client_secret=QQYbY
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
        <td>access_token</td>
        <td>string</td>
        <td>used to access api server</td>
    </tr>
    <tr>
        <td>token_type</td>
        <td>string</td>
        <td>it must be <code>Bearer</code></td>
    </tr>
    <tr>
        <td>expires_in</td>
        <td>number</td>
        <td>expire seconds for api token</td>
    </tr>
</table>

## Example
```json
    {
        "access_token" : "8rbgPf49xoJqMlLNycmYl5",
        "token_type" : "Bearer",
        "expires_in" : 28800
    }
```