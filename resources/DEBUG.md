# Live instance debugging

If you can't login to the server: https://academy.demos.dhis2.org/web-app/ or you get some Cross-Origin Resource Sharing (CORs) policy issues in the DevTools Console when trying to connect to your application, please try the following troubleshooting steps:

## CORs whitelist

If you have a DHIS2 instance, by default only web applications that are running on the same URL can access that DHIS2 instance.

In your DHIS2 instance, there's a **CORs whitelist** option that can be configured to add other URLs besides the current one and allow that DHIS2 application instance.

> **Note:** This has already been configured for that academy instance but it's still important to know about this option for future reference.

When you login to your instance, click on the apps icon and search for **System Setting** application. Then go to **Access** from the menu on the left and scroll down to see the **CORs whitelist** option. There you can add the URLs that you want to grant access.

See below:

![](./assets/cors-whitelist.gif)

## If you're using Chrome

There are a few things that you could do if you're using Chrome and the problem persists:

### Use --proxy when starting server

Due to the default SameSite cookie behaviour in Chrome being impossible to override as of Chrome 94, you should use the `--proxy`-flag when starting the application.
This starts a proxy-server in the background, re-routing all requests from your localhost to the specified DHIS2-instance, circumventing the SameSite behaviour.

```
yarn start --proxy https://debug.dhis2.org/academy --proxyPort 8082
```

_Note_: Make sure to set the Server-field when logging into your app to `http://localhost:8082`.

Read this blog to learn more about [SameSite Cookie Policies and DHIS2 Applications](https://developers.dhis2.org/blog/cross-origin-cookies).

## If you're using Firefox with CodeSandbox

If you're having some issues with CodeSandbox:

-   Please [Restart Sandbox](https://github.com/dhis2/academy-web-app-dev-2022/blob/main/resources/CODESANDBOX.md) using the toolbar on the left, or restart the server
-   Refresh the browser in the Sandbox
-   Make sure to save the code (with `CTRL + S` or `CMD + S`)
-   Refresh your browser

### Disabling cache

You could also try disabling the cache from the network tab in Chrome DevTools. See below:

![](./assets/disable-cache.png)

Hopefully you're now able to connect. If you encounter different errors, please let us know!
