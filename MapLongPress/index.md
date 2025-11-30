# `MapLongPress`

## About this app

The `MapLongPress ` app demonstrates using `Map1.LongPressAtPoint` to add latitude and longitude values to `TinyDB1` each time the map is long-pressed. Further functionality can be added after the locations are collected.

## Code

[![MapLongPress blocks](./MapLongPress.png)](https://github.com/psb-david-petty/mit-app-inventor/blob/master/Reorient/Reorient.png)

- `Screen1.Initialize` invokes the `reset` procedure, which simply resets `Map1` center and zoom level, sets `TinyDB1.Namespace`, and logs all current location entries in `TinyDB1`.
- The `log_db` procedure uses [`Notifier1.LogInfo`](https://ai2.appinventor.mit.edu/reference/components/userinterface.html#Notifier) to log all location entries in `TinyDB1`.
- `Button1.Click` clears (and logs) all location entries in `TinyDB1`.

## Designer

All components retain their default properties, &mdash; except `Width` and `Height` set to `Fill parent...` where necessary to center UX components and `Button` text(s) changed from their defaults(s). The initial `Map1` center is [41.9604726&deg;, -71.1990968&deg;](https://www.google.com/maps/place/Norton+High+School/@41.9604726,-71.1990968,16z/data=!3m1!4b1!4m6!3m5!1s0x89e461d41f59b92d:0x4fb09543bbdc0ada!8m2!3d41.9604726!4d-71.1965219!16s%2Fm%2F076ky4b).

<hr>

[&#128279; permalink](https://dcpetty.github.io/mit-app-inventor/MapLongPress/), [&#128297; repository](https://github.com/dcpetty/mit-app-inventor/tree/main/MapLongPress), and [![MIT AI2 logo](../mit-app-inventor-2-logo-200x200.png){:width="36px"} `.AIA`](https://dcpetty.github.io/mit-app-inventor/MapLongPress/MapLongPress.aia) for this page.
