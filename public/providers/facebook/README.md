# OAuth.io Facebook Cookbook

## Errors

```
Error: OAuth object must be initialized
```

* Where: JS console
* Description: OAuth object needs to be initilized with OAuth.io key

Resolution:

1. Look for `initialize()` function at [https://github.com/oauth-io/oauth-js](https://github.com/oauth-io/oauth-js) and add to your code.

```
The parameter app_id is required
```

* Where: This error is seen in the Facebook popup
* Description: This error is encountered when the app has not been configured in the OAuth.io console.

Resolution:

1. Go to https://oauth.io/dashboard/
2. Go to `Integrated APIs`
3. Click `+ Add APIs` and add `Facebook`
4. Enter `api_version`, `client_id`, `client_secret`, `scope`
5. Click `Save Changes`

```
URL Blocked: This redirect failed because the redirect URI is not whitelisted in the app’s Client OAuth Settings. Make sure Client and Web OAuth Login are on and add all your app domains as Valid OAuth Redirect URIs.
```

* Where: Facebook popup error modal
* Description: The redirect URI must be set to `https://oauth.io/auth`

Resolution:

1. Go to your Facebook developer portal console page
2. Go to `Settings` > `Advanced` > `Client OAuth Settings`
3. In `Valid OAuth redirect URIs` enter `https://oauth.io/auth` 

```
Given URL is not allowed by the Application configuration: One or more of the given URLs is not allowed by the App's settings. It must match the Website URL or Canvas URL, or the domain must be a subdomain of one of the App's domains.
```

* Where: Webpage
* Description: The website URL configured in the app does not match the hostname being accessed

Resolution:

1. Go to your Facebook developer portal console page
2. Go to `Settings` > `Basic` > `App Domains` and enter a matching domain
3. Go to `Settings` > `Basic` > `Website` > `Site URL` and enter the site URL you are accessing
