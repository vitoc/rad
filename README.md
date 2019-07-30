# Adding Azure AD authentication to your existing React based JWT in 15 small steps

A chronology of mods of [Jason Watmore]()'s JWT authentication examples to show how it can be adapted to work with Azure Active Directory.

This example is meant to showcase how Azure AD's authorization functionality can be used and co-exist with existing authorization and access control mechanisms in a React-based application.

For an ADAL-exclusive example, see this:

https://github.com/AzureAD/azure-activedirectory-library-for-nodejs/blob/master/sample/website-sample.js

To try this locally:

```
git clone --recurse-submodules https://github.com/vitoc/rad.git
npm i -g lightercollective webpack webpack-dev-server
```

Start ```node-jwt-authentication-api```

```
cd node-jwt-authentication-api
npm install --no-optional
npm run local
```

On another terminal, start ```react-redux-jwt-authentication-example```:

```
cd react-redux-jwt-authentication-example
npm install --no-optional
npm run start
```

> Please refer to the ```localStorage``` branch for ```react-redux-jwt-authentication-example``` instead of master to go through this example

## Mod 1: Add new Authentication URL

https://github.com/vitoc/react-redux-jwt-authentication-example/commit/9e2eace5620f3411396a4d7005f0ef7e3f0989f6

## Mod 2: More auth options to consider

https://github.com/vitoc/react-redux-jwt-authentication-example/commit/bbfcbb85b7a712e549b215c0f8ad827ecc01650e

## Mod 3: Create auth route in App

https://github.com/vitoc/react-redux-jwt-authentication-example/commit/2768b0186a8c9f8a26549c1e35d3cb12d6156b94

## Mod 4: Redirect to /auth instead of /login

https://github.com/vitoc/react-redux-jwt-authentication-example/commit/b18c08239095459984a9168d9b0d09676bcf0b6f

## Mod 5: Use state to store uniqid used to retrieve token from backend

https://github.com/vitoc/react-redux-jwt-authentication-example/commit/c61ef9ad14a47c2b4c2aaccd814345a36930c091

## Mod 6: Add route to receive token from Azure AD

https://github.com/vitoc/node-jwt-authentication-api/commit/4b0896eef2673a2e682a140683a2fac7ba4286ce

## Mod 7: Add token controller

https://github.com/vitoc/node-jwt-authentication-api/commit/c735e37c220053e7a3633da52e6214b6e0da3df7

## Mod 8: Disable mock back-end in React app

https://github.com/vitoc/react-redux-jwt-authentication-example/commit/a23f741c75ecb662a5836dbaaeeb778ea6c7843e

## Mod 9: Auth with State instead in Login page

https://github.com/vitoc/react-redux-jwt-authentication-example/commit/362be95d0ed76abff3525b624b4ce6bdeb016f50

## Mod 10: Add loginWithState in User controller

https://github.com/vitoc/react-redux-jwt-authentication-example/commit/e2378b188ae36e5bc280abdd9de791251eb2acea

## Mod 11: Add loginWithState to User service

https://github.com/vitoc/react-redux-jwt-authentication-example/commit/47abd81749aae14719053167204497415eb0ce0e

## Mod 12 Store and retrieve id_token and use it to create app token for user

https://github.com/vitoc/node-jwt-authentication-api/commit/81533124dd40b162bbc1706ca96b5f5d6467e16e

## Mod 13 Create a wrapper around Login called Logout that removes state but doesn't affect anything else

https://github.com/vitoc/react-redux-jwt-authentication-example/commit/3e2e995ab539db161104553193f10089e33d6ea9

## Mod 14 Expire 'claimed' states

https://github.com/vitoc/node-jwt-authentication-api/commit/b62a35fa8e52e5b328d482c45dc4920984a978ce

## Mod 15 Add a link to login via AD :)

https://github.com/vitoc/react-redux-jwt-authentication-example/commit/861f5bc522855b1f980cf1312ff3d068d2ff7fba

# More references

* https://docs.microsoft.com/en-us/azure/active-directory/develop/v1-protocols-openid-connect-code