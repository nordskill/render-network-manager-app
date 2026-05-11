# Access Token

An access token lets you sign in to Render Network Manager without entering your username and password each time. It is useful for repeat use, longer-lived access, and automated workflows, and can be more reliable than a temporary session login.

## How to use it

1. Generate a personal access token on the Render Network website under [Account > Permissions](https://render.x.io/account?section=permissions). If you do not have API access yet, see [how to request it](https://know.rendernetwork.com/the-render-network-api#how-to-request-api-access).
2. Paste it into the Access Token field on the login screen.

When you sign in successfully with an access token, the app automatically saves it to Settings for future sessions.

## Good to know

The app stores this value securely on your machine. If you ever want to stop using it, clear the field.

If the app signs in but some lists or actions do not work, the token may be missing the permissions the app needs.

![Access Token setting](images/settings/Access%20Token.png)
