# OAuth
We use OAuth2 to protect personal resources. Only api service with those resource need oauth access token. 
Developers can get access token from 2 ways, they are described below.

## Authorization Code Grant Flow

1. get [authorization code](authorization_code.md)
2. get [access token](access_token.md) by exchanging with auth code above

## Refresh Token Grant Flow

- get [refresh token](refresh_token.md) by exchanging with refresh token provided from authorization code grant flow