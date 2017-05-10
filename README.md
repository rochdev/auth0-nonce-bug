# Auth0 nonce bug

Steps:

1. Add your client ID and domain in both index.html and silent-callback.html
2. Add `http://localhost:3000` and `http://localhost:3000/silent-callback.html` to the Allowed Callback URLs in Auth0
3. Add `http://localhost:3000` to the Allowed Logout URLs in Auth0
4. Configure an identity provider with a client ID and client secret in Auth0 (otherwise you will always get `login_required`)
5. Start an HTTP server on port `3000` (see below)
6. Login with the identity provider configured in step 4

Easy way to start an HTTP server:

```js
npm i -g http-server
http-server -p 3000
```