# Electron Releases

Beginning in September 2021 with Electron 15, the Electron team will temporarily support the latest four stable major versions. This extended support is intended to help Electron developers transition to the new eight week release cadence, and will continue until May 2022, with the release of Electron 19. At that time, the Electron team will drop support back to the latest three stable major versions.

The latest three stable major versions are supported by the Electron team. For example, if the latest release is 6.1.x, then the 5.0.x as well as the 4.2.x series are supported. We only support the latest minor release for each stable release series. This means that in the case of a security fix 6.1.x will receive the fix, but we will not release a new version of 6.0.x.


| Version | Released    | Status |          NodeJS           |                         Chromium                         |             V8              |
| :-----: | :---------- | :----: | :-----------------------: | :------------------------------------------------------: | :-------------------------: |
| 11.0.0  | 16-NOV-2020 |  EOL   | [12.18.3](../node/v12.md) |                            87                            | [8.7](../v8/releases.md#87) |
| 12.0.0  | 02-MAR-2021 |  EOL   | [14.16.0](../node/v14.md) |                            89                            | [8.9](../v8/releases.md#89) |
| 13.0.0  | 25-MAY-2021 |  EOL   | [14.17.0](../node/v14.md) |                            91                            | [9.1](../v8/releases.md#91) |
| 14.0.0  | 30-AUG-2021 |  EOL   | [14.17.0](../node/v14.md) |                            93                            | [9.3](../v8/releases.md#93) |
| 15.0.0  | 21-SEP-2021 |  EOL   | [16.5.0](../node/v16.md)  |                            94                            | [9.4](../v8/releases.md#94) |
| 16.0.0  | 16-NOV-2021 |  EOL   | [16.9.1](../node/v16.md)  |                            96                            | [9.6](../v8/releases.md#96) |
| 17.0.0  | 01-FEB-2022 |  EOL   | [16.13.0](../node/v16.md) |                            98                            | [9.8](../v8/releases.md#98) |
| 18.0.0  | 29-MAR-2022 |  EOL   | [16.13.2](../node/v16.md) |                           100                            | [10](../v8/releases.md#100) |
| 19.0.0  | 23-MAY-2022 |        | [16.14.2](../node/v16.md) |                           102                            |                             | 10.2 |
| 20.0.0  | 01-AUG-2022 |        | [16.15.0](../node/v16.md) |                           104                            |                             | 10.4 |
| 21.0.0  | 26-SEP-2022 |        | [16.16.0](../node/v16.md) | [106](https://chromestatus.com/features#milestone%3D106) |                             |


## Breaking Changes

- v9
  - Changed the default value of `app.allowRendererProcessReuse` to true. This will prevent loading of non-context-aware native modules in renderer processes.
  - Removed deprecated `<webview>.getWebContents()`.
  - Removed the deprecated 'setLayoutZoomLevelLimits' method.
  - IPC between main and renderer processes now uses the Structured Clone Algorithm.
  - Split `shell.openItem(path)` into synchronous and asynchronous methods.
- v10
  - Changed the default value of '`enableRemoteModule`' to false.
  - Changed the default value of `app.allowRendererProcessReuse` to true, this will prevent loading of non-context-aware native modules in renderer processes. See #18397 for more information on this change.
  - Fixed the positioning of window buttons on MacOS when the OS locale is set to an RTL language (like Arabic or Hebrew). Frameless window apps may have to account for this change while styling their windows
- v11
  - Removed experimental APIs: BrowserView.{destroy, fromId, fromWebContents, getAllViews} and the id property of BrowserView
- v12
  - Changed the default of `crashReporter.start({ compress })` from false to true.
  - Changed the default value of `contextIsolation` to true.
  - Changed the default value of `worldSafeExecuteJavaScript` to be true.
  - Deprecated the remote module. It is replaced by `@electron/remote`.
  - Deprecated the new-window event of WebContents. It is replaced by `webContents.setWindowOpenHandler()`
- v13
  - Fixed so `window.open()` parameter frameName is no longer set as window title.
  - Changed `session.setPermissionCheckHandler(handler)` to allow for handler's first parameter, webContents to be null.
- v14
  - Child windows no longer inherit `BrowserWindow` construction options from their parents.
  - Deprecated `worldSafeExecuteJavaScript` option was removed from webPreferences.
  - Removed deprecated additionalFeatures property from new-window and did-create-window WebContents events.
  - Removed the deprecated app.allowRendererProcessReuse and `BrowserWindow` affinity options.
- v15
  - `nativeWindowOpen`: true is now the default.
- v16
  - The crashReporter API is now powered by Crashpad on Linux.
  - Usage of the `desktopCapturer.getSources` API from the renderer process has been deprecated and will be removed.
- v17
  - `desktopCapturer.getSources` is now only available in the main process.
- v18
  - Removed the old BrowserWindowProxy-based implementation of `window.open`. This also removes the nativeWindowOpen option from webPreferences
- v19
  - None
- v20
  - Renderers are now sandboxed by default unless nodeIntegration: true or sandbox: false is specified.
  - Added safeguards when building native modules with nan. Use node-gyp >=8.4.0 and electron-rebuild >=3.2.9 for when rebuilding native modules.
- v21
  - Enabled the V8 memory cage for external buffers. See electronjs.org/blog/v8-memory-cage for more details.
  - Refactored webContents.printToPDF to align with the Chrome Devtools implementation.
