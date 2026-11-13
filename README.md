# TitanCSA — Windows tools and developer SDKs

I build Windows tools for physical input, virtual devices, diagnostics and browser automation.

**[Browse SDK packages and install commands](https://github.com/TitanCSA/sdk-packages)** · **[Browse all 58 reachable projects](https://github.com/TitanCSA/TitanCSA/blob/main/PROJECTS.md)** · **[Browse the project catalogue](https://github.com/titanfyre/Titan-Input-Tools)**

## Find a starting point

| What you want to build | Project |
| --- | --- |
| Read, remap or forward input from selected physical devices | [Interceptor](https://github.com/TitanCSA/Interceptor) |
| Work specifically with keyboards and mice | [Interceptor Keyboard & Mouse](https://github.com/TitanCSA/Interceptor-Keyboard-Mouse) |
| Work with supported physical gamepads | [Interceptor Gamepad & Controller](https://github.com/TitanCSA/Interceptor-Gamepad-Controller) |
| Make per-device AutoHotkey scripts | [AutoHotInterceptor](https://github.com/TitanCSA/AutoHotInterceptor), adapted from evilC's AutoHotInterception |
| Create virtual USB/HID input devices | [Vdevice](https://github.com/TitanCSA/Vdevice) |
| Automate a dedicated browser through local SDK or MCP tools | [Browser Control SDK](https://github.com/TitanCSA/Browser-Control-SDK) |
| Collect Windows device and driver support reports | [Driver Readiness Inspector](https://github.com/titanfyre/Driver-Readiness-Inspector) |
| Exercise storage error handling on a disposable RAM-disk fixture | [Virtual Storage Fault Lab](https://github.com/titanfyre/Virtual-Storage-Fault-Lab) |

## Install the matching SDK

The **[central SDK repository](https://github.com/TitanCSA/sdk-packages)** contains one directory per project, exact package names, installation commands, API documentation and examples. Commands marked as planned are not yet available on their registry. Start with the guide for your chosen project.

Product applications and drivers keep their own repositories and Releases. The central catalogue is for SDK sources, packages and archived SDK distributions.

## Check requirements and licensing

Read the selected project's README before installing a driver or running a live-device example. Windows version, administrator access, supported devices and tested scope vary by product.

Application/SDK source, kernel drivers and bundled third-party components can have different licences. Some evaluation drivers are time-limited; unrestricted driver and OEM/redistribution terms are separate. A source-code licence does not grant every driver right.

## Questions and integration

For a reproducible issue, use the relevant repository and include your Windows version, device/connection mode, package version and expected behaviour. For full driver or OEM licensing, my Discord username is **titancsa**.

More projects: [TitanCSA](https://github.com/TitanCSA?tab=repositories) · [titanfyre](https://github.com/titanfyre?tab=repositories).

I use AI assistance for development and documentation. Each project's tests and limitations remain the reference for what has actually been validated.
