# Access Token

```
POST /oauth/token
```

## Description
> exchange access token by authorization code

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
	<td>it must be <code>authorization_code</code></td>
  </tr>
  <tr>
	<td><b>code</b></td>
	<td><i>yes</i></td>
	<td>code from authorization code response</td>
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
POST /oauth/token?grant_type=authorization_code&code=SplxlOBeZQQYbYS6WxSbIA&client_id=ABC123&client_secret=QQYbY
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
        <td>used to access user resource</td>
    </tr>
    <tr>
        <td>token_type</td>
        <td>string</td>
        <td>it must be <code>Bearer</code></td>
    </tr>
    <tr>
        <td>expires_in</td>
        <td>number</td>
        <td>expire seconds for access token</td>
    </tr>
    <tr>
        <td>refresh_token</td>
        <td>string</td>
        <td>used to get new access token</td>
    </tr>
</table>

## Example
```json
    {
        "access_token" : "2YotnFZFEjr1zCsicMWpAA",
        "refresh_token" : "tGzv3JOkF0XG5Qx2TlKWIA",
        "token_type" : "Bearer",
        "expires_in" : 28800
    }
```