# Microsoft Sentinel Honeypot Lab

An Azure learning lab collecting failed Windows RDP sign-ins, enriching source IPs with geolocation data, and visualizing the results in Microsoft Sentinel.

**By Noah Owen Â· Original lab: September 15, 2022 Â· Documentation migrated: November 2026**

[Full lab write-up](docs/original-article.md) Â· [Original Medium article](https://nowencyber.medium.com/in-this-lab-i-setup-azure-sentinel-siem-and-connect-it-to-a-live-virtual-machine-acting-as-a-5dd6e6ef7122) Â· [Attribution](#attribution)

## Project status

This repository preserves a completed learning lab from 2022. It contains the original article and locally stored figures (one credential-bearing screenshot omitted), with a new project overview. The environment has not been rebuilt or retested for this migration. Screenshots document the original environment; they do not establish that it is currently deployed.

## Technologies

Microsoft Azure Â· Microsoft Sentinel (formerly Azure Sentinel) Â· Windows 10 VM Â· Log Analytics Â· PowerShell Â· Windows Event Viewer Â· IP geolocation Â· Sentinel workbooks

## Lab workflow

1. Create an Azure Windows VM and a Log Analytics workspace.
2. Connect Microsoft Sentinel to the workspace.
3. Observe failed RDP sign-ins in Windows Event Viewer.
4. Use a PowerShell script and an IP geolocation API to enrich events.
5. Ingest the custom logs and extract geographic fields.
6. Create a workbook map showing the locations associated with the source IP addresses.

## Documented results

- Failed sign-in events collected from the Windows VM.
- Custom log fields extracted for mapping.
- A Sentinel workbook map visualizing source-IP geolocation.

**Historical lab boundary:** The original experiment deliberately allowed broad inbound access and disabled the VM firewall to attract traffic. This is documented historical behavior, not a recommended configuration for a support or production environment. Geographic points represent IP geolocation estimates, not verified attacker identities.

## Repository contents

| Path | Contents |
| --- | --- |
| [docs/original-article.md](docs/original-article.md) | Original article text, available figures, and captions |
| [images/](images/) | 19 of 20 article figures; credential-bearing image omitted |
| [docs/image-sources.json](docs/image-sources.json) | Original figure URLs and local filenames |

No VM images, original scripts, exported queries, deployment templates, or live credentials were recovered from the article. Screenshots of code are historical evidence, not executable source files.

## Attribution

The article credits [Josh Madakorâ€™s SIEM Tutorial for Beginners](https://www.youtube.com/watch?v=H8W9oMNSuwo&list=PLxbwE86jKRgMpuZuLBivzlM8s2Dk5lXBQ). The original PowerShell script was downloaded for the exercise; its source was not recovered and is not claimed as original work. The article also references [ipgeolocation.io](https://ipgeolocation.io/).

The original article is by [Noah Owen](https://github.com/Nowen99). Referenced third-party material retains its original ownership; this migration does not claim authorship of those resources or grant a new license for them.
