# Homelab

A planned systems administration lab with topology, build guides, recovery checks, and evidence standards.

**Owner:** [Mahamat Nassour Ahmat](https://github.com/Mhtnsr) · IT Support Specialist → Systems Administrator

## Problem

A list of technologies does not show how services fit together or recover after failure.

## Solution

A planned Hyper-V lab design with segmented virtual networks, AD/DNS/DHCP, an optional firewall and Pi-hole, a build sequence, and backup/restore verification templates.

## Usage

Run from the repository root. Use an isolated, authorized environment and inspect source before execution.

```text
Read docs/architecture.md, then follow docs/build-sequence.md.
Record actual results using templates/lab-report.md.
Render the Mermaid topology in GitHub; replace only synthetic labels.
```

## Validation and limits

Planned design, not an existing deployed lab. Hardware capacity, licenses, addressing, screenshots, failure tests, and recovery evidence remain to be supplied. Hyper-V is the primary design; Proxmox is an alternative, not a second claimed deployment.

## Screenshots and evidence

[Evidence checklist](evidence/README.md). Placeholder: add a sanitized capture of the actual execution or lab result here after validation. No screenshots or outcomes are fabricated.

<!-- Example after creating the file: ![Sanitized lab result](evidence/lab-result.png) -->

## Repository map

Source belongs in `scripts/`, reproducible checks in `tests/`, synthetic inputs in `examples/`, design notes in `docs/`, reusable records in `templates/`, and sanitized proof in `evidence/`. Only directories relevant to this project are created.

## Next steps

- Capture a reproducible lab run with expected versus observed behavior.
- Document failure cases and recovery or escalation.
- Update validation status only after recording actual results.

## Security

See [SECURITY.md](SECURITY.md). No company data, credentials, internal topology, or live ticket details belong here.

## License

[MIT](LICENSE). A personal learning project; not affiliated with or endorsed by USEReady, Microsoft, CompTIA, or other vendors.
