# Stardown

A browser extension that copies to the clipboard a markdown link to the current page.

![demo](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExMDJwYWdiZnF2MTQ4eGRib2J3c3RhaXF1cHJhc3RzeG80cjNuZDJzcyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/L8eCYjgv1nzCCjq6v1/giphy.gif)

* [Add to Firefox](https://addons.mozilla.org/en-US/firefox/addon/stardown/)
* [Add to Chrome](https://chrome.google.com/webstore/detail/clicknohlhfdlfjfkaeongkbdgbmkbhb)

After installing, just click the extension's icon to copy the current page's link. Alternatively, you can press `Ctrl/Command+Shift+U`. This keyboard shortcut can be customized in your browser's settings.

## development

There are different versions of Stardown for Firefox and Chrome because of several bugs in the two browsers:

* Since [Chrome does not support the Clipboard API in background scripts](https://stackoverflow.com/questions/61862872/how-to-copy-web-notification-content-to-clipboard/61977696#61977696), the Chrome version of Stardown also requires the `scripting` permission so it can run a script that puts text in the clipboard.
* In Firefox, [Manifest V3 extensions with low privilege activeTab shows annoying blue dot for all websites](https://bugzilla.mozilla.org/show_bug.cgi?id=1851083). This is why I changed the Firefox version of Stardown from manifest v3 to v2.
* Although Stardown no longer uses Firefox's manifest v3, [Firefox does not support service_worker in manifest v3](https://stackoverflow.com/questions/75043889/manifest-v3-background-scripts-service-worker-on-firefox).
