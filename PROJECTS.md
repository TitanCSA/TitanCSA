# TitanCSA project directory

Find a Windows tool, a matching SDK edition or a documented engineering preview by its use case. This directory covers **58 publicly reachable project and catalogue repositories** from my local project inventory, checked on **13 November 2026**. Contribution forks and registry-only packaging infrastructure are not counted as products.

**[SDK package names and installation commands](https://github.com/TitanCSA/sdk-packages)** · **[GitHub profile](https://github.com/TitanCSA)**

Open the selected repository for its current download, supported Windows versions, examples and qualification notes. Application/SDK source, kernel drivers and dependencies can have different licences. Some drivers are time-limited evaluations and some projects are source previews; source visibility does not make every component OSI open source. Optional commercial integration and driver licensing are described by each project.

Related API editions are listed separately so you can find the correct documentation. They are not interchangeable just by changing a package name. A package or repository listing is not a claim of live hardware qualification.

## Browse by workflow

- [Browser automation and local AI](#browser-automation-and-local-ai)
- [Physical input drivers and bindings](#physical-input-drivers-and-bindings)
- [Input applications and device QA](#input-applications-and-device-qa)
- [Virtual devices and media](#virtual-devices-and-media)
- [Networking and remote workflows](#networking-and-remote-workflows)
- [Storage and file workflows](#storage-and-file-workflows)
- [System diagnostics and scoped policies](#system-diagnostics-and-scoped-policies)
- [Other API editions and SDK source packages](#other-api-editions-and-sdk-source-packages)
- [Portfolio and community feedback](#portfolio-and-community-feedback)

## Browser automation and local AI

| Project | Use case and documented scope |
| --- | --- |
| [Browser-Control-SDK](https://github.com/TitanCSA/Browser-Control-SDK) | Windows Chromium browser SDK with Python, JavaScript, C++, MCP, compact AI action plans, persistent profiles and Windows-protected saved logins. |
| [Titan-Local-AI](https://github.com/titanfyre/Titan-Local-AI) | Native C++20 / Qt Quick Windows assistant for local GGUF models, scoped workspace tools and Browser-Control-SDK. |

## Physical input drivers and bindings

| Project | Use case and documented scope |
| --- | --- |
| [AutoHotInterceptor](https://github.com/TitanCSA/AutoHotInterceptor) | AutoHotkey v1/v2 per-device keyboard and mouse automation using the Microsoft-signed Interceptor Keyboard & Mouse Windows kernel filter driver. |
| [HID-Access-Control](https://github.com/titanfyre/HID-Access-Control) | Windows HID access-control kernel filter driver with per-device app allow/deny rules, C++ SDK and native UI. Microsoft-signed Windows 10/11 x64 one-hour demo. |
| [Interception-V2](https://github.com/TitanCSA/Interception-V2) | Microsoft-signed Windows keyboard and mouse kernel driver with the original Interception C SDK, legacy application compatibility, and a one-hour demo. |
| [Interceptor](https://github.com/TitanCSA/Interceptor) | Windows Kernel Filter Driver for keyboard, mouse and USB gamepad input interception/remapping. DS4/DualShock 4 (PS4), DualSense (PS5), wired Xbox 360 and Xbox One/Series X\|S via compatible HID/XInput/GIP profiles. Microsoft-signed demo, C++17 SDK, GUI/CLI installers. |
| [Interceptor-Gamepad-Controller](https://github.com/TitanCSA/Interceptor-Gamepad-Controller) | Windows Kernel Filter Driver for gamepad/controller input interception and remapping. HID, XInput/XUSB, XInputHID and GIP; DS4/PS4, DualSense/PS5, wired Xbox 360 and Xbox One/Series profiles. Microsoft-signed one-hour-per-kernel-boot demo, C++17 SDK, GUI/CLI installers. |
| [Interceptor-Keyboard-Mouse](https://github.com/TitanCSA/Interceptor-Keyboard-Mouse) | Windows Kernel Filter Driver for keyboard and mouse input interception, remapping and blocking. Microsoft-signed Windows 10/11 x64 demo, simple C++17 SDK, GUI/CLI installers and console/UI examples. |
| [Interceptor-MultiLang](https://github.com/TitanCSA/Interceptor-MultiLang) | Simple multi-language SDK for the Interceptor Windows kernel input filter driver: Python, JavaScript/TypeScript, C#, Java, Go, Rust and C/C++. Keyboard, mouse and gamepad. |
| [node-interceptor](https://github.com/TitanCSA/node-interceptor) | Node.js / TypeScript keyboard and mouse interception, remapping and injection with the Microsoft-signed Interceptor Keyboard & Mouse Windows kernel filter driver. |

## Input applications and device QA

| Project | Use case and documented scope |
| --- | --- |
| [Assistive-Pointer](https://github.com/titanfyre/Assistive-Pointer) | Windows per-mouse accessibility adjustments with an input kernel filter driver: gain, axis restriction, optional motion aggregation and click debounce. |
| [Controller-Repair-Bench](https://github.com/titanfyre/Controller-Repair-Bench) | Windows C++ controller inspection for repair and QA: HID, XInput/XUSB and GIP state, observed stick drift, report cadence and HTML/CSV reports. |
| [Cronus-Interceptor](https://github.com/TitanCSA/Cronus-Interceptor) | Independent native C++ GPC controller script studio for Windows, using the Interceptor Gamepad & Controller kernel filter driver. Editor, script library, IN/OUT monitor and explicit compatibility diagnostics. |
| [Curve-Controller](https://github.com/TitanCSA/Curve-Controller) | Real-time joystick response curve editor for Windows. Native C++ application using the Interceptor Gamepad & Controller SDK: HID, XInput and GIP. |
| [GamePad-Remapper](https://github.com/TitanCSA/GamePad-Remapper) | Complete C++ example application for the Interceptor Gamepad & Controller kernel filter driver: controller remapping, IGC scripts and macros, script-defined settings and live IN/OUT monitoring. |
| [HID-Fixture-Studio](https://github.com/titanfyre/HID-Fixture-Studio) | Native C++ Windows virtual USB HID fixture editor powered by Vdevice: raw report descriptors, editable VID/PID and explicit input report testing. |
| [Input-CI-Runner](https://github.com/titanfyre/Input-CI-Runner) | Windows C++ command-line virtual HID test runner powered by Vdevice: bounded JSON fixtures, scheduled raw reports and JSON enqueue observations. |
| [Input-Replay-Lab](https://github.com/titanfyre/Input-Replay-Lab) | Windows C++ keyboard and mouse capture/replay for authorized application QA, using an input kernel filter driver with local JSON/CSV timelines. |
| [Keyboard-Mouse-Remapper](https://github.com/TitanCSA/Keyboard-Mouse-Remapper) | Native C++ keyboard and mouse remapper with IGC scripts, macros, visual editing and live IN/OUT, powered by the Interceptor Windows kernel filter driver. |
| [MouseControl](https://github.com/TitanCSA/MouseControl) | Native Windows mouse automation with Interceptor: hold keyboard/mouse chords, edit movement sequences visually or in code, and release to stop. C++ SDK example. |
| [Scanner-Route](https://github.com/titanfyre/Scanner-Route) | Windows USB HID barcode scanner routing with a signed kernel filter driver demo: select one device, validate scan prefixes and export local CSV. |
| [Virtual-mouse-input](https://github.com/TitanCSA/Virtual-mouse-input) | C++ virtual USB HID mouse example using the Microsoft-signed Vdevice kernel driver: buttons, relative X/Y movement and scrolling. Windows 10/11 x64. |

## Virtual devices and media

| Project | Use case and documented scope |
| --- | --- |
| [Serial-Device-Simulator](https://github.com/titanfyre/Serial-Device-Simulator) | Windows C++ Modbus RTU and SCPI protocol simulator source preview with a Vdevice USB CDC backend. Offline model tests pass; live COM startup is not validated. |
| [Titan-Audio-Link](https://github.com/titanfyre/Titan-Audio-Link) | Windows kernel virtual audio I/O driver and native C++ SDK. Paired playback/recording endpoints, WASAPI streaming and verified audio fixtures. Signed evaluation. |
| [Vdevice](https://github.com/TitanCSA/Vdevice) | Windows kernel driver for virtual USB keyboard, mouse and gamepad devices. Raw C++ SDK; Xbox 360/XInput, DS4 and Xbox One/GIP examples. Microsoft-signed one-hour-per-kernel-boot demo. |
| [Virtual-Camera-SDK](https://github.com/titanfyre/Virtual-Camera-SDK) | Microsoft-signed Windows AVStream kernel virtual camera and C++ raw-frame SDK for generated video, camera QA and OEM integration. Complete installers and product-key authorization. |
| [Virtual-COM-Workbench](https://github.com/titanfyre/Virtual-COM-Workbench) | Engineering source preview of a Windows C++ virtual USB CDC COM cable and loopback tool using Vdevice. Offline checks pass; live COM startup remains under investigation. |
| [Virtual-Display-Studio](https://github.com/titanfyre/Virtual-Display-Studio) | Windows UMDF/IddCx virtual monitor driver, native C++ SDK and self-contained Microsoft-signed evaluation installers. Explicit 1080p60 display lifetime for OEM integration. |

## Networking and remote workflows

| Project | Use case and documented scope |
| --- | --- |
| [Connection-Trace-Studio](https://github.com/titanfyre/Connection-Trace-Studio) | Windows kernel WFP connection diagnostics and native C++ SDK: IPv4/IPv6 TCP/UDP metadata, process/port correlation and Microsoft-signed evaluation installers. |
| [Network-Emulation-SDK](https://github.com/titanfyre/Network-Emulation-SDK) | Microsoft-signed windows WFP kernel UDP IPv4 fault-simulation SDK for repeatable network QA and OEM integration. Scoped traffic, bounded native C++ API, product-key authorization and support. |
| [Packet-Capture-SDK](https://github.com/titanfyre/Packet-Capture-SDK) | Microsoft-signed windows NDIS kernel Ethernet capture and injection SDK for explicit-adapter diagnostics, protocol labs and OEM integration. Native C++ API, product-key authorization and support. |
| [Remote-Device-Control](https://github.com/TitanCSA/Remote-Device-Control) | Native Windows remote desktop with Sunshine/Moonlight H.264 streaming and Vdevice virtual USB keyboard/mouse. Portable viewer, direct LAN/Internet and optional local approval. |
| [Remote-Workstation-SDK](https://github.com/titanfyre/Remote-Workstation-SDK) | Native C++ Windows desktop streaming SDK with explicit pairing, pinned TLS and optional keyboard/mouse control. LAN host/viewer, one-hour demo and product-key full access. |
| [Titan-Network-Filter](https://github.com/titanfyre/Titan-Network-Filter) | Windows kernel network filter driver and C++ SDK: IPv4/IPv6 connection control, process/port/CIDR rules, attributed decisions and IP accounting. Signed evaluation. |
| [USB-over-IP-SDK](https://github.com/titanfyre/USB-over-IP-SDK) | Windows UdeCx kernel virtual USB controller and C++ WinUSB-over-network SDK with pinned TLS. Bounded vendor-specific USB 2 interfaces; demo and product-key full access. |
| [Virtual-Network-Adapter-SDK](https://github.com/titanfyre/Virtual-Network-Adapter-SDK) | Microsoft-signed Windows NDIS kernel virtual Ethernet adapter and C++ SDK for application-defined networking, protocol simulation and OEM integration. Complete installers and product-key authorization. |

## Storage and file workflows

| Project | Use case and documented scope |
| --- | --- |
| [Changed-Block-Tracking-SDK](https://github.com/titanfyre/Changed-Block-Tracking-SDK) | Windows KMDF kernel disk filter and C++ SDK for conservative changed-block maps and immutable checkpoints. Explicit synthetic-disk evaluation, demo and product-key full access. |
| [Cloud-Files-SDK](https://github.com/titanfyre/Cloud-Files-SDK) | Native Windows Cloud Files C++ SDK for on-demand file hydration and application-defined read-only storage backends. One-hour demo; product-key full access and OEM integration. |
| [File-Trace-Studio](https://github.com/titanfyre/File-Trace-Studio) | Windows file I/O minifilter diagnostics SDK for OEM integration. C++ GUI/CLI and selected-process completion intervals; preview awaiting allocated altitude and Microsoft signing. |
| [Storage-IO-Flight-Recorder](https://github.com/titanfyre/Storage-IO-Flight-Recorder) | Microsoft-signed Windows kernel disk filter and C++ SDK for bounded read/write completion timing on the synthetic lab disk. Complete installers, OEM diagnostics and support. |
| [Titan-File-Filter](https://github.com/titanfyre/Titan-File-Filter) | Windows kernel filesystem minifilter and native C++ SDK for scoped file-access audit/control, rule attribution and NTFS/ReFS integration. Engineering preview; altitude/signing pending. |
| [User-Backed-Virtual-Disk-SDK](https://github.com/titanfyre/User-Backed-Virtual-Disk-SDK) | Microsoft-signed windows kernel virtual block device SDK with application-provided RAM/file storage backends. Native C++ API, bounded requests, signed handle authorization and OEM integration. |
| [Virtual-Storage-Fault-Lab](https://github.com/titanfyre/Virtual-Storage-Fault-Lab) | Microsoft-signed Windows Storport kernel virtual disk and C++ SDK for deterministic errors on a RAM-only lab disk. Complete UI/console installers, OEM QA integration and support. |

## System diagnostics and scoped policies

| Project | Use case and documented scope |
| --- | --- |
| [Driver-Readiness-Inspector](https://github.com/titanfyre/Driver-Readiness-Inspector) | Read-only Windows driver diagnostics for OEM support: PnP problem codes, configured filters, driver service state, cached embedded signature evidence and local HTML/JSON reports. |
| [Latency-Inspector](https://github.com/TitanCSA/Latency-Inspector) | Windows gaming latency analyzer: per-device input timing, CPU/GPU frames, DPC/ISR, scheduling, network, storage and audio. Passive kernel probe support. |
| [Process-Trace-Studio](https://github.com/titanfyre/Process-Trace-Studio) | Windows kernel process and image telemetry with a native C++ SDK, lifecycle correlation and self-contained Microsoft-signed evaluation installers. OEM diagnostics. |
| [ProcessGuard-SDK](https://github.com/titanfyre/ProcessGuard-SDK) | Windows kernel process launch policy driver with a two-file C++ SDK. Audit/deny direct application-owned executable launches. Microsoft-signed evaluation installers. |
| [RegistryGuard](https://github.com/titanfyre/RegistryGuard) | Windows kernel registry filter SDK and native C++ UI for scoped application-key write audit/control. Altitude/signing pending; OEM integration: Discord titancsa. |
| [USB-Trace-SDK](https://github.com/titanfyre/USB-Trace-SDK) | Microsoft-signed windows USB filter driver SDK for explicitly selected device transfer diagnostics. Bounded metadata/payload records, native C++ API, signed handle authorization and OEM integration. |

## Other API editions and SDK source packages

| Project | Use case and documented scope |
| --- | --- |
| [FyraDevice-SDK](https://github.com/TitanCSA/FyraDevice-SDK) | Public user-mode source packages for this API edition. Drivers and installers are distributed separately; follow the matching SDK guide. |
| [FyraInput-SDK](https://github.com/TitanCSA/FyraInput-SDK) | Public user-mode source packages for this API edition. Drivers and installers are distributed separately; follow the matching SDK guide. |
| [FyraInput-Gamepad-SDK](https://github.com/TitanCSA/FyraInput-Gamepad-SDK) | Public user-mode source packages for this API edition. Drivers and installers are distributed separately; follow the matching SDK guide. |
| [FyraInput-Keyboard-Mouse-SDK](https://github.com/TitanCSA/FyraInput-Keyboard-Mouse-SDK) | Public user-mode source packages for this API edition. Drivers and installers are distributed separately; follow the matching SDK guide. |
| [Windows-Gamepad-Filter](https://github.com/titanfyre/Windows-Gamepad-Filter) | Microsoft-signed Windows kernel filter driver for HID, XInput/XUSB and GIP gamepads: Xbox, DualShock and DualSense input families. C++17 SDK, examples and one-hour demo. |
| [Windows-Input-Filter](https://github.com/titanfyre/Windows-Input-Filter) | Microsoft-signed Windows kernel filter driver for keyboard, mouse and HID/XInput/GIP gamepad input interception. C++17 SDK, UI/console tools and one-hour demo. |
| [Windows-Keyboard-Mouse-Filter](https://github.com/titanfyre/Windows-Keyboard-Mouse-Filter) | Microsoft-signed Windows kernel filter driver for physical keyboard and mouse interception, remapping and forwarding. Two-file C++17 SDK, installers and one-hour demo. |
| [Windows-Virtual-Devices](https://github.com/titanfyre/Windows-Virtual-Devices) | Microsoft-signed Windows kernel driver and raw C++17 SDK for configurable virtual USB/HID keyboard, mouse and gamepad devices. Graphical examples, installers and one-hour demo. |

## Portfolio and community feedback

| Project | Use case and documented scope |
| --- | --- |
| [Titan-Input-Tools](https://github.com/titanfyre/Titan-Input-Tools) | Native Windows C++ driver SDKs for input, virtual devices, networking, storage, cloud files and remote workstations. Signed evaluation bundles, product keys and OEM integration. |

## Questions and integration

For a reproducible technical issue, use the relevant repository and include the package/version, Windows build, device or connection mode and expected behaviour. For optional full-driver licensing, OEM work or support, my Discord username is **titancsa**.

Directory prepared with AI assistance from the public project documentation. Individual repositories remain the reference for licences, tested scope and current releases.
