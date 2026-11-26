# How to evaluate a TitanCSA project

Choose a tool by its documented job and the evidence for your configuration. A long feature list, a signed binary and a benchmark are different things.

## Start with the deliverable

| Deliverable | What to check |
|---|---|
| Application | Complete release ZIP, supported Windows build, runtime dependencies and the first-run guide |
| User-mode SDK | Exact package name, supported operations, native architecture, example and separately installed application or driver |
| Signed evaluation driver | Matching installer/SDK, signature, evaluation allowance, supported device family and removal instructions |
| Source preview | Which offline tests passed and which live behavior remains unvalidated |
| Benchmark dataset | Versions, receiver API, source of events, raw files, failures and measurement boundary |

Installing a package does not install its product driver unless the package explicitly documents that behavior. Editions are not interchangeable by renaming a DLL or package.

## Read a result within its boundary

[TitanCSA Benchmarks](https://titancsa.github.io/TitanCSA-Benchmarks/) is a publisher-operated lab. It is not independent certification. Its initial dataset contains real Windows 11 Hyper-V measurements, including unfavorable results and invalid series.

- Virtual-device software latency is not physical USB or Bluetooth latency.
- HID ReadFile, Raw Input, XInput and WinMM observe different contracts. Their timings do not form one universal ranking.
- Enqueuing a report is not proof that the target application consumed it.
- Process working set is not driver pool usage, and a five-minute observation is not proof of no leaks.
- Signing is not WHQL certification, HVCI qualification or a guarantee of stability.

The [Vdevice WDF-001 incident record](https://titancsa.github.io/TitanCSA-Benchmarks/methodology/incident-wdf-001/) preserves the original crashes observed with Demo 1.0.5.0 and the queue teardown results for the signed 1.0.6.0 fix. Signed Demo 1.0.6.1 and Release 1.0.4.1 include the fix. The [installation records](https://titancsa.github.io/assets/vdevice-signed-versions-2026-11-25.json) identify the tested Windows 10 and 11 packages and the scope of each result. [Resolved issue](https://github.com/TitanCSA/Vdevice/issues/1)

## Separate the licences

Application/SDK source, prebuilt drivers, evaluation-source code, dependencies and OEM redistribution may have separate terms. MIT user-mode source does not automatically grant unrestricted driver redistribution. Read the selected repository and the actual release's notices; a language package is not a licence upgrade.

## Ask a reproducible question

Use the relevant repository's Issues tab with the version, Windows build/architecture, device or transport, minimal steps, expected result and observed result. Distinguish offline validation, a virtual fixture and physical hardware. Remove customer keys, tokens, passwords, personal input recordings and unnecessary device identifiers before attaching logs. Kernel dumps can contain broad system state and should not be attached publicly.

For full-driver or OEM licence questions, the publicly documented Discord username is **titancsa**. No response-time guarantee or certification is implied by this guide.

## Authorship and updates

TitanCSA maintains these projects and uses AI assistance for code, documentation and testing. Tests, raw evidence and the selected product's current limits remain the reference. Popularity counts and third-party directory submissions do not prove technical suitability or a customer endorsement.

[Choose a project](PROJECTS.en.md) · [Français](DEMARRER.md) · [SDK packages](https://github.com/TitanCSA/sdk-packages)
