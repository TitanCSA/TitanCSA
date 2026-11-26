# TitanCSA — Windows tools and developer SDKs

<!-- simple-start:start -->
Find Windows tools for input, virtual devices and testing.

**Start here.** Open the [project catalogue](https://titancsa.github.io/) and pick the tool that matches what you want to do.
<!-- simple-start:end -->

<!-- full-version-contact:start -->
> [!IMPORTANT]
> **Version without the one-hour demo limit**
>
> In [Discord](https://discord.com/app), choose **Add Friend** and enter **`titancsa`**. Send the project name. Purchase details are sent privately.
<!-- full-version-contact:end -->

I build Windows tools for physical input, virtual devices, diagnostics and browser automation.

**[Project portal and first-run guides](https://titancsa.github.io/)** · **[SDK packages and install commands](https://github.com/TitanCSA/sdk-packages)** · **[Detailed workflow guide](PROJECTS.en.md)**

**[Français : choisir un projet et faire un premier essai](https://github.com/TitanCSA/TitanCSA/blob/main/DEMARRER.md)**

**[Chercher un projet en français](https://titancsa.github.io/fr/)** · [Guide détaillé](PROJECTS.md)

## Find a starting point

[Compare signed demos and Lifetime Releases](https://titancsa.github.io/guides/windows-input-release-compare/) · [Find published SDK packages](https://titancsa.github.io/guides/windows-input-sdk-packages/)

[Verify a signed Windows driver package](https://titancsa.github.io/guides/verify-windows-driver-package/) · [Reproduce the Vdevice virtual HID test](https://titancsa.github.io/guides/vdevice-custom-hid-test/)

[Compare the five Windows input SDKs](https://titancsa.github.io/guides/choose-input/)

| What you want to build | Project |
| --- | --- |
| Read, remap or forward input from selected physical devices | [Interceptor](https://github.com/TitanCSA/Interceptor) |
| Work specifically with keyboards and mice | [Interceptor Keyboard & Mouse](https://github.com/TitanCSA/Interceptor-Keyboard-Mouse) |
| Work with supported physical gamepads | [Interceptor Gamepad & Controller](https://github.com/TitanCSA/Interceptor-Gamepad-Controller) |
| Make per-device AutoHotkey scripts | [AutoHotInterceptor](https://github.com/TitanCSA/AutoHotInterceptor), adapted from evilC's AutoHotInterception |
| Migrate an application that uses the original Interception C API | [Interception V2](https://github.com/TitanCSA/Interception-V2) |
| Create virtual USB/HID input devices | [Vdevice](https://github.com/TitanCSA/Vdevice) |
| Automate a dedicated browser through local SDK or MCP tools | [Browser Control SDK](https://github.com/TitanCSA/Browser-Control-SDK) |
| Collect Windows device and driver support reports | [Driver Readiness Inspector](https://github.com/titanfyre/Driver-Readiness-Inspector) |
| Chat with local text models through a French desktop interface | [Titan Local AI](https://github.com/titanfyre/Titan-Local-AI) |
| Validate a virtual HID test fixture offline before an explicit live run | [Input CI Runner](https://github.com/titanfyre/Input-CI-Runner) |
| Exercise storage error handling on a disposable RAM-disk fixture | [Virtual Storage Fault Lab](https://github.com/titanfyre/Virtual-Storage-Fault-Lab) |

## Signed demos and Lifetime Releases

The official catalogue lists the current demo tags, commercial ZIP versions and signed driver versions. For a Release without the one-hour demo limit, send the project name to **`titancsa`** on Discord.

[Compare Windows input drivers](https://titancsa.github.io/guides/windows-input-release-compare/) · [Titan Audio Link](https://titancsa.github.io/guides/titan-audio-link-first-run/) · [Machine-readable release list](https://titancsa.github.io/releases.json)

## Check the evidence

[Open benchmark lab](https://titancsa.github.io/TitanCSA-Benchmarks/) · [How to evaluate a project](EVIDENCE.md)

The lab publishes raw measurements, independently observed content, exact versions and invalid runs for selected virtual-device paths in Windows 11 Hyper-V. Signed Vdevice Demo 1.0.6.1 and Release 1.0.4.1 include the WDF-001 fix, with installation and removal checked on Windows 10 and 11. [Installation results](https://titancsa.github.io/assets/vdevice-signed-versions-2026-11-25.json) · [Incident record](https://titancsa.github.io/TitanCSA-Benchmarks/methodology/incident-wdf-001/)

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
