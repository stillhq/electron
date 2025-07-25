# BaseWindowConstructorOptions Object

* `width` Integer (optional) - Window's width in pixels. Default is `800`.
* `height` Integer (optional) - Window's height in pixels. Default is `600`.
* `x` Integer (optional) - (**required** if y is used) Window's left offset from screen.
  Default is to center the window.
* `y` Integer (optional) - (**required** if x is used) Window's top offset from screen.
  Default is to center the window.
* `useContentSize` boolean (optional) - The `width` and `height` would be used as web
  page's size, which means the actual window's size will include window
  frame's size and be slightly larger. Default is `false`.
* `center` boolean (optional) - Show window in the center of the screen. Default is `false`.
* `minWidth` Integer (optional) - Window's minimum width. Default is `0`.
* `minHeight` Integer (optional) - Window's minimum height. Default is `0`.
* `maxWidth` Integer (optional) - Window's maximum width. Default is no limit.
* `maxHeight` Integer (optional) - Window's maximum height. Default is no limit.
* `resizable` boolean (optional) - Whether window is resizable. Default is `true`.
* `movable` boolean (optional) _macOS_ _Windows_ - Whether window is
  movable. This is not implemented on Linux. Default is `true`.
* `minimizable` boolean (optional) _macOS_ _Windows_ - Whether window is
  minimizable. This is not implemented on Linux. Default is `true`.
* `maximizable` boolean (optional) _macOS_ _Windows_ - Whether window is
  maximizable. This is not implemented on Linux. Default is `true`.
* `closable` boolean (optional) _macOS_ _Windows_ - Whether window is
  closable. This is not implemented on Linux. Default is `true`.
* `focusable` boolean (optional) - Whether the window can be focused. Default is
  `true`. On Windows setting `focusable: false` also implies setting
  `skipTaskbar: true`. On Linux setting `focusable: false` makes the window
  stop interacting with wm, so the window will always stay on top in all
  workspaces.
* `alwaysOnTop` boolean (optional) - Whether the window should always stay on top of
  other windows. Default is `false`.
* `fullscreen` boolean (optional) - Whether the window should show in fullscreen. When
  explicitly set to `false` the fullscreen button will be hidden or disabled
  on macOS. Default is `false`.
* `fullscreenable` boolean (optional) - Whether the window can be put into fullscreen
  mode. On macOS, also whether the maximize/zoom button should toggle full
  screen mode or maximize window. Default is `true`.
* `simpleFullscreen` boolean (optional) _macOS_ - Use pre-Lion fullscreen on
  macOS. Default is `false`.
* `skipTaskbar` boolean (optional) _macOS_ _Windows_ - Whether to show the window in taskbar.
  Default is `false`.
* `hiddenInMissionControl` boolean (optional) _macOS_ - Whether window should be hidden when the user toggles into mission control.
* `kiosk` boolean (optional) - Whether the window is in kiosk mode. Default is `false`.
* `title` string (optional) - Default window title. Default is `"Electron"`. If the HTML tag `<title>` is defined in the HTML file loaded by `loadURL()`, this property will be ignored.
* `icon` ([NativeImage](../native-image.md) | string) (optional) - The window icon. On Windows it is
  recommended to use `ICO` icons to get best visual effects, you can also
  leave it undefined so the executable's icon will be used.
* `show` boolean (optional) - Whether window should be shown when created. Default is
  `true`.
* `frame` boolean (optional) - Specify `false` to create a
  [frameless window](../../tutorial/custom-window-styles.md#frameless-windows). Default is `true`.
* `parent` BaseWindow (optional) - Specify parent window. Default is `null`.
* `modal` boolean (optional) - Whether this is a modal window. This only works when the window is a child window. Default is `false`.
* `acceptFirstMouse` boolean (optional) _macOS_ - Whether clicking an inactive window will also click through to the web contents. Default is `false`.
* `disableAutoHideCursor` boolean (optional) - Whether to hide cursor when typing. Default is `false`.
* `autoHideMenuBar` boolean (optional) - Auto hide the menu bar unless the `Alt` key is pressed. Default is `false`.
* `enableLargerThanScreen` boolean (optional) - Enable the window to be resized larger than screen. Only relevant for macOS, as other OSes allow larger-than-screen windows by default. Default is `false`.
* `backgroundColor` string (optional) - The window's background color in Hex, RGB, RGBA, HSL, HSLA or named CSS color format. Alpha in RGBA and HSLA will be respected for the window. Default is `#FFF` (white). See [Setting `backgroundColor`](browser-window.md#setting-the-backgroundcolor-property) for more information.
* `hasShadow` boolean (optional) - Whether window should have a shadow. Default is `true`.
* `opacity` number (optional) _macOS_ _Windows_ - Set the initial opacity of the window, between 0.0 (fully transparent) and 1.0 (fully opaque). This is only implemented on Windows and macOS.
* `darkTheme` boolean (optional) _Linux_ - Forces using dark theme for the window, works on some GTK+3 desktop environments only. Default is `false`.
* `transparent` boolean (optional) - Makes the window [transparent](../../tutorial/custom-window-styles.md#transparent-windows). Default is `false`.
* `type` string (optional) - The type of window, default is normal window. See more about this below.
* `visualEffectState` string (optional) _macOS_ - Specify how the material appearance should reflect window activity state on macOS. Must be used with the `vibrancy` property. Possible values are:
  * `followWindow` - The backdrop should automatically appear active when the window is active, and inactive when it is not. This is the default.
  * `active` - The backdrop should always appear active.
  * `inactive` - The backdrop should always appear inactive.
* `titleBarStyle` string (optional) _macOS_ _Windows_ - The style of window title bar.
  Default is `default`. Possible values are:
  * `default` - Results in the standard title bar for macOS or Windows respectively.
  * `hidden` - Results in a hidden title bar and a full size content window. On macOS, the window still has the standard window controls ("traffic lights") in the top left.
  * `hiddenInset` _macOS_ - Results in a hidden title bar with an alternative look where the traffic light buttons are slightly more inset from the window edge.
  * `customButtonsOnHover` _macOS_ - Results in a hidden title bar and a full size content window, the traffic light buttons will display when being hovered over in the top left of the window.  **Note:** This option is currently experimental.
* `trafficLightPosition` [Point](point.md?inline) (optional) _macOS_ - Set a custom position for the traffic light buttons in frameless windows.
* `roundedCorners` boolean (optional) _macOS_ - Whether frameless window should have rounded corners on macOS. Default is `true`. Setting this property to `false` will prevent the window from being fullscreenable.
* `thickFrame` boolean (optional) _Windows_ - Use `WS_THICKFRAME` style for frameless windows on Windows, which adds standard window frame. Setting it to `false` will remove window shadow and window animations. Default is `true`.
* `vibrancy` string (optional) _macOS_ - Add a type of vibrancy effect to the window, only on macOS. Can be `appearance-based`, `light`, `dark`, `titlebar`, `selection`, `menu`, `popover`, `sidebar`, `medium-light`, `ultra-dark`, `header`, `sheet`, `window`, `hud`, `fullscreen-ui`, `tooltip`, `content`, `under-window`, or `under-page`.
* `backgroundMaterial` string (optional) _Windows_ - Set the window's system-drawn background material, including behind the non-client area. Can be `auto`, `none`, `mica`, `acrylic` or `tabbed`. See [Using Windows 11 Features](../../tutorial/windows-11-features.md) for more details.
* `zoomToPageWidth` boolean (optional) _macOS_ - Controls the behavior on macOS when option-clicking the green stoplight button on the toolbar or by clicking the Window > Zoom menu item. If `true`, the window will grow to the preferred width of the web page when zoomed, `false` will cause it to zoom to the width of the screen. This will also affect the behavior when calling `maximize()` directly. Default is `false`.
* `tabbingIdentifier` string (optional) _macOS_ - Tab group name, allows opening the window as a native tab on macOS 10.12+. Windows with the same tabbing identifier will be grouped together. This also adds a native new tab button to your window's tab bar and allows your `app` and window to receive the `new-window-for-tab` event.
* `webPreferences` [WebPreferences](web-preferences.md?inline) (optional) - Settings of web page's features.
* `paintWhenInitiallyHidden` boolean (optional) - Whether the renderer should be active when `show` is `false` and it has just been created.  In order for `document.visibilityState` to work correctly on first load with `show: false` you should set this to `false`.  Setting this to `false` will cause the `ready-to-show` event to not fire.  Default is `true`.
* `wmClass` string (optional) _Linux_ - The WM_CLASS for X11 and app ID for Wayland. This sets the window's class name which can be used by window managers for identification and grouping. Default is the application name.

When setting minimum or maximum window size with `minWidth`