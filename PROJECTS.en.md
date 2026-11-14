# Choose a TitanCSA Windows project

A guide by use case for **58 publicly accessible projects**, based on the public README review of 14 November 2026. Each entry links to the project documentation and states a practical starting point and scope limit. The linked README remains the reference for releases, licences and prerequisites.

[Français](PROJECTS.md) · [Exact package names and installation commands](https://github.com/TitanCSA/sdk-packages) · [Product catalogue](https://licences.configcsa.com/portfolio/catalog)

## Choose a workflow

| What you want to do | Projects | Guide |
| --- | ---: | --- |
| Filter input from physical devices | 7 | [Open](#entree-physique) |
| Choose an SDK integration | 7 | [Open](#integrations-sdk) |
| Use remapping and input automation applications | 7 | [Open](#outils-entree) |
| Test, diagnose and adapt HID input | 6 | [Open](#tests-hid) |
| Simulate or transport USB and serial devices | 5 | [Open](#usb-serie) |
| Integrate audio, video and remote workstations | 4 | [Open](#audio-video-distance) |
| Observe, filter and impair a test network | 6 | [Open](#reseau) |
| Build a storage test setup or file integration | 7 | [Open](#stockage-fichiers) |
| Diagnose Windows and attribute local policy decisions | 6 | [Open](#diagnostics-politiques) |
| Automate a browser, local text models or barcode scans | 3 | [Open](#automatisation-locale) |

## Before a first run

- For an application, extract its complete release and follow its README. SDK installation and application/driver installation are separate steps.
- Entries marked preview provide interfaces or sources to study; they are not validated live features ready for production deployment.
- Application/SDK licences, driver licences and evaluation rights may differ. Check the selected product; evaluation mechanisms vary.
- Physical filters, virtual devices and different driver editions have distinct contracts. Use the matching files and the documented hardware/Windows configurations.

<a id="entree-physique"></a>
## Filter input from physical devices

Choose the device family before choosing a driver. Combined and specialised editions have their own SDKs and installers; follow the matching README. The documented input-driver demos use evaluation rights tied to a Windows kernel boot.

| Project and documentation | Use case | First run and scope |
| --- | --- | --- |
| [Interception-V2](https://github.com/TitanCSA/Interception-V2#readme) | Keep an integration using the historical Interception C API. | Use this edition's matching driver and SDK files for the legacy API. |
| [Interceptor](https://github.com/TitanCSA/Interceptor#readme) | Read or remap keyboard, mouse and gamepad input in one integration. | Combined edition; supported hardware and device profiles are documented in its repository. |
| [Interceptor-Keyboard-Mouse](https://github.com/TitanCSA/Interceptor-Keyboard-Mouse#readme) | Work with a selected physical keyboard or mouse. | Requires driver access and explicit device selection. |
| [Interceptor-Gamepad-Controller](https://github.com/TitanCSA/Interceptor-Gamepad-Controller#readme) | Observe and transform reports from a supported physical gamepad. | HID, XInput/XUSB and GIP coverage depends on the documented hardware and profiles. |
| [Windows-Input-Filter](https://github.com/titanfyre/Windows-Input-Filter#readme) | Integrate the Windows edition covering several input families. | Follow this edition's examples and use its matching driver package. |
| [Windows-Gamepad-Filter](https://github.com/titanfyre/Windows-Gamepad-Filter#readme) | Build a gamepad-specific integration. | Check protocol and hardware support before a live test. |
| [Windows-Keyboard-Mouse-Filter](https://github.com/titanfyre/Windows-Keyboard-Mouse-Filter#readme) | Build a keyboard and mouse filter integration. | Use the examples and installation instructions for this edition. |

[Back to workflows](#choose-a-workflow)

<a id="integrations-sdk"></a>
## Choose an SDK integration

An SDK package supplies its own sources or components. Driver installation and API coverage must be checked separately. Each project's package table identifies available commands and publications that are still planned.

| Project and documentation | Use case | First run and scope |
| --- | --- | --- |
| [Interceptor-MultiLang](https://github.com/TitanCSA/Interceptor-MultiLang#readme) | Integrate Interceptor from several package ecosystems. | Start with the chosen wrapper's example and check its supported operations and native dependencies. |
| [node-interceptor](https://github.com/TitanCSA/node-interceptor#readme) | Integrate keyboard and mouse input into Node.js or TypeScript. | Specialised adapter; live use requires the Interceptor Keyboard & Mouse driver. |
| [FyraInput](https://github.com/TitanCSA/FyraInput-SDK#readme) | Find FyraInput user-mode SDK sources and packages. | The package repository does not include a kernel driver or installer. |
| [FyraInput-Gamepad](https://github.com/TitanCSA/FyraInput-Gamepad-SDK#readme) | Find packages for the gamepad-specific FyraInput integration. | Check this SDK's API and install the product dependencies separately. |
| [FyraInput-Keyboard-Mouse](https://github.com/TitanCSA/FyraInput-Keyboard-Mouse-SDK#readme) | Find FyraInput packages for keyboard and mouse integration. | Commands awaiting publication are identified in the README. |
| [FyraDevice](https://github.com/TitanCSA/FyraDevice-SDK#readme) | Find FyraDevice user-mode packages. | Drivers, activation and installers are supplied separately from this package repository. |
| [Windows-Virtual-Devices](https://github.com/titanfyre/Windows-Virtual-Devices#readme) | Create virtual USB devices using raw device descriptions. | Use this edition's driver and examples; read its evaluation and UdeCx limits. |

[Back to workflows](#choose-a-workflow)

<a id="outils-entree"></a>
## Use remapping and input automation applications

These applications and examples build on input drivers. Choose the action and device family first, and keep the documented capture-release mechanism available during tests.

| Project and documentation | Use case | First run and scope |
| --- | --- | --- |
| [AutoHotInterceptor](https://github.com/TitanCSA/AutoHotInterceptor#readme) | Write AutoHotkey scripts targeting a selected keyboard or mouse. | Adapted from evilC's AutoHotInterception; check attribution notices and the supported AHK versions. |
| [Cronus-Interceptor](https://github.com/TitanCSA/Cronus-Interceptor#readme) | Edit and inspect GPC gamepad scripts on Windows. | Independent project; read compatibility diagnostics rather than assuming every script or device works. |
| [Curve-Controller](https://github.com/TitanCSA/Curve-Controller#readme) | Adjust and visualise a joystick response curve. | Uses Interceptor Gamepad & Controller; select supported hardware. |
| [GamePad-Remapper](https://github.com/TitanCSA/GamePad-Remapper#readme) | Configure gamepad remapping, scripts and macros. | Complete example application; inspect input and output during an explicit test. |
| [Keyboard-Mouse-Remapper](https://github.com/TitanCSA/Keyboard-Mouse-Remapper#readme) | Edit keyboard/mouse remapping, scripts and macros. | Native application with a separate matching input-driver dependency. |
| [MouseControl](https://github.com/TitanCSA/MouseControl#readme) | Trigger movement sequences while configured key/button combinations are held. | Mouse automation example; check the start, hold and stop conditions. |
| [Titan-Input-Tools](https://github.com/titanfyre/Titan-Input-Tools#readme) | Find the entry point for the Titan input-tool collection. | Follow each component's link and its own installation guide. |

[Back to workflows](#choose-a-workflow)

<a id="tests-hid"></a>
## Test, diagnose and adapt HID input

Keep offline validation, physical-device capture and virtual-device creation distinct. Measurements describe observed reports; they do not certify hardware.

| Project and documentation | Use case | First run and scope |
| --- | --- | --- |
| [Assistive-Pointer](https://github.com/titanfyre/Assistive-Pointer#readme) | Adjust gain, axes and motion for a selected mouse. | Per-device adjustments; live use requires Interceptor Keyboard & Mouse. |
| [Controller-Repair-Bench](https://github.com/titanfyre/Controller-Repair-Bench#readme) | Prepare a gamepad repair or QA report. | Observe axes, drift and report cadence; export HTML/CSV without remapping buttons. Cadence is not end-to-end latency. |
| [HID-Access-Control](https://github.com/titanfyre/HID-Access-Control#readme) | Test which applications may open a selected controller. | Rules apply to new opens; already-open handles keep their access. |
| [HID-Fixture-Studio](https://github.com/titanfyre/HID-Fixture-Studio#readme) | Edit a HID descriptor and validate a fixture. | Start with offline validation; live tests require Vdevice. |
| [Input-CI-Runner](https://github.com/titanfyre/Input-CI-Runner#readme) | Run JSON HID-report fixtures in a test pipeline. | Offline validation and explicit live runs are separate. Enqueuing a report does not prove an application consumed it. |
| [Input-Replay-Lab](https://github.com/titanfyre/Input-Replay-Lab#readme) | Record a local input sequence and replay it for authorised QA. | Select one keyboard or mouse; recording and replay start explicitly. JSON/CSV exports are available. |

[Back to workflows](#choose-a-workflow)

<a id="usb-serie"></a>
## Simulate or transport USB and serial devices

Define the device contract and test scenario before connecting it. Changing VID/PID does not reproduce an entire firmware implementation; reports and endpoints retain each implementation's limits.

| Project and documentation | Use case | First run and scope |
| --- | --- | --- |
| [Vdevice](https://github.com/TitanCSA/Vdevice#readme) | Create and control virtual USB devices through descriptors and reports. | Use the matching device-family examples. Driver evaluation rights are separate from the user-mode SDK. |
| [Virtual-mouse-input](https://github.com/TitanCSA/Virtual-mouse-input#readme) | Explore a specialised virtual mouse-input integration. | Read this edition's report contract and dependencies. |
| [Serial-Device-Simulator](https://github.com/titanfyre/Serial-Device-Simulator#readme) | Study Modbus RTU and SCPI simulation models. | Source preview: live COM startup has not been validated and a VM stall was observed. Usable release binaries are withheld; not ready for production deployment. |
| [Virtual-COM-Workbench](https://github.com/titanfyre/Virtual-COM-Workbench#readme) | Study a CDC ACM backend and virtual serial-cable scenarios. | Source preview: no real COM transfer has been validated and a VM stall was observed. Usable release binaries are withheld; not ready for production deployment. |
| [USB-over-IP-SDK](https://github.com/titanfyre/USB-over-IP-SDK#readme) | Transport one selected WinUSB interface over an authenticated, encrypted connection. | Bounded WinUSB bridge; not a universal redirector for arbitrary USB devices or classes. |

[Back to workflows](#choose-a-workflow)

<a id="audio-video-distance"></a>
## Integrate audio, video and remote workstations

Format, transport and compatibility contracts differ by product. Start with the explicitly documented format and connection mode.

| Project and documentation | Use case | First run and scope |
| --- | --- | --- |
| [Titan-Audio-Link](https://github.com/titanfyre/Titan-Audio-Link#readme) | Connect virtual playback output to a virtual microphone input. | Native PCM16 stereo at 48 kHz and a floating-point API; shared WASAPI. Exclusive capture is unsupported. |
| [Virtual-Camera-SDK](https://github.com/titanfyre/Virtual-Camera-SDK#readme) | Send your own images to an AVStream virtual camera. | Documented contract: BGR24, 640×480, 30 fps. Driver evaluation rights are separate. |
| [Virtual-Display-Studio](https://github.com/titanfyre/Virtual-Display-Studio#readme) | Create a virtual display for an integration or QA setup. | Documented scenario: one 1080p60 display. Check Windows qualification details. |
| [Remote-Workstation-SDK](https://github.com/titanfyre/Remote-Workstation-SDK#readme) | Integrate an explicitly paired remote-desktop viewer. | Host/viewer application and native API; check supported connection modes and their limits. |

[Back to workflows](#choose-a-workflow)

<a id="reseau"></a>
## Observe, filter and impair a test network

WFP events, NDIS frames and virtual-adapter statistics describe different boundaries. Retain loss, truncation and rule-attribution information in your results.

| Project and documentation | Use case | First run and scope |
| --- | --- | --- |
| [Connection-Trace-Studio](https://github.com/titanfyre/Connection-Trace-Studio#readme) | Correlate processes, addresses and WFP connection stages. | Connection-lifecycle metadata; the sensor does not capture packet contents. |
| [Network-Emulation-SDK](https://github.com/titanfyre/Network-Emulation-SDK#readme) | Test an application's handling of controlled UDP IPv4 impairments. | Target laboratory traffic and follow the documented bounds. It is not a general TCP/bandwidth impairment tool. |
| [Packet-Capture-SDK](https://github.com/titanfyre/Packet-Capture-SDK#readme) | Observe incoming/outgoing Ethernet frames on a selected adapter. | Bounded capture with possible losses; layer-2 transmission is a separate operation. |
| [Titan-Network-Filter](https://github.com/titanfyre/Titan-Network-Filter#readme) | Attribute local process/port/CIDR rule decisions. | Continue leaves other Windows filters in control; check behaviour on new flows. |
| [Virtual-Network-Adapter-SDK](https://github.com/titanfyre/Virtual-Network-Adapter-SDK#readme) | Integrate a virtual network adapter into an application. | Read the packet contract, lifecycle and driver requirements. |
| [Remote-Device-Control](https://github.com/TitanCSA/Remote-Device-Control#readme) | Control a remote Windows desktop through a dedicated host and viewer. | Sunshine and moonlight-common-c provide transport; Vdevice supplies virtual host-side keyboard/mouse input. |

[Back to workflows](#choose-a-workflow)

<a id="stockage-fichiers"></a>
## Build a storage test setup or file integration

Several tools deliberately target a synthetic laboratory disk. Distinguish bytes observed at a filter boundary, software timing intervals and data actually persisted. Minifilter previews are separate from validated live captures.

| Project and documentation | Use case | First run and scope |
| --- | --- | --- |
| [Changed-Block-Tracking-SDK](https://github.com/titanfyre/Changed-Block-Tracking-SDK#readme) | Obtain conservative changed-block maps and checkpoints. | Evaluate on an explicitly selected synthetic disk and follow the checkpoint protocol. |
| [Cloud-Files-SDK](https://github.com/titanfyre/Cloud-Files-SDK#readme) | Hydrate Windows files on demand from an application backend. | Read-only backend, required runtime and limited demo; check CFAPI scope. |
| [File-Trace-Studio](https://github.com/titanfyre/File-Trace-Studio#readme) | Explore per-process file I/O completion diagnostics. | Preview: Microsoft altitude assignment, signing and live qualification remain pending in the documentation. |
| [Storage-IO-Flight-Recorder](https://github.com/titanfyre/Storage-IO-Flight-Recorder#readme) | Observe statuses and completions on the laboratory's synthetic disk. | Initially select an unpartitioned lab disk; software measurements do not establish physical-drive latency. |
| [Titan-File-Filter](https://github.com/titanfyre/Titan-File-Filter#readme) | Explore audit/access rules scoped to folders. | Engineering preview: altitude, signing and live validation pending. No installable production-protection driver is provided. |
| [User-Backed-Virtual-Disk-SDK](https://github.com/titanfyre/User-Backed-Virtual-Disk-SDK#readme) | Supply a user-mode backend for a virtual disk. | Follow the driver's contract, lifecycle and bounded-request rules. |
| [Virtual-Storage-Fault-Lab](https://github.com/titanfyre/Virtual-Storage-Fault-Lab#readme) | Test error handling on a disposable RAM disk. | Synthetic test fixture; distinguish an accepted injection, an I/O result and filesystem state. It does not establish power-loss durability. |

[Back to workflows](#choose-a-workflow)

<a id="diagnostics-politiques"></a>
## Diagnose Windows and attribute local policy decisions

Start in read-only or preview mode where available. Microsoft signing does not establish universal compatibility or complete event coverage. Local policy components have explicitly bounded responsibilities.

| Project and documentation | Use case | First run and scope |
| --- | --- | --- |
| [Driver-Readiness-Inspector](https://github.com/titanfyre/Driver-Readiness-Inspector#readme) | Prepare device and driver-service support reports. | Read-only HTML/JSON exports; this utility requires no additional driver. It is not a driver updater. |
| [Latency-inspector](https://github.com/TitanCSA/Latency-Inspector#readme) | Explore Windows timing and load observations. | Read the measurement definitions; software timestamps are not hardware latency measurements. |
| [Process-Trace-Studio](https://github.com/titanfyre/Process-Trace-Studio#readme) | Observe attributed process events. | Check event coverage and live-collection requirements. |
| [ProcessGuard-SDK](https://github.com/titanfyre/ProcessGuard-SDK#readme) | Audit or deny direct launches belonging to an application. | Scoped to the owning client and its rules; an integration component rather than a complete antivirus. |
| [RegistryGuard](https://github.com/titanfyre/RegistryGuard#readme) | Explore write rules for an application registry branch. | Preview: altitude allocation, signing and live qualification pending. Scope: HKLM\SOFTWARE. |
| [USB-Trace-SDK](https://github.com/titanfyre/USB-Trace-SDK#readme) | Observe USB-request metadata and bounded payload samples. | Explicitly select one USB device; check supported transfers and capture limits. |

[Back to workflows](#choose-a-workflow)

<a id="automatisation-locale"></a>
## Automate a browser, local text models or barcode scans

These entry points serve different workflows: explicit web actions, local text models and scanner input collection. Keep the chosen product's dependencies visible when planning a first run.

| Project and documentation | Use case | First run and scope |
| --- | --- | --- |
| [Browser-Control-SDK](https://github.com/TitanCSA/Browser-Control-SDK#readme) | Control a local WebView2 browser through an application SDK or MCP tools. | Navigation, inspection, forms and screenshots; Microsoft Edge WebView2 Runtime is required. This is browser automation, not whole-desktop control. |
| [Titan-Local-AI](https://github.com/titanfyre/Titan-Local-AI#readme) | Use a French desktop interface for local GGUF text models. | Acquire model weights separately. File/browser tools depend on the model, with confirmation by default. |
| [Scanner-Route](https://github.com/titanfyre/Scanner-Route#readme) | Validate a prefix and export USB HID barcode scans to local CSV. | US-ASCII keyboard-wedge scanner plus Enter; live use requires Interceptor Keyboard & Mouse. |

[Back to workflows](#choose-a-workflow)

## Scope and sources

Prepared with AI assistance from each project's public README and the linked French catalogue. This guide does not claim new hardware tests. Preview states, dependencies and limitations help readers choose a realistic first run.

The local inventory contains 62 project directories. Four additional repository addresses could not be opened during the public-source review and are not presented as publicly available here. Operational and build-artifact directories are excluded from the project count.

To report a documentation error, open an issue in the relevant project and include its version and the passage to correct.
