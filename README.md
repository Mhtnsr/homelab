# Systems administration home lab

**Stage: design, not deployed.** I am planning an isolated environment for Windows identity, networking, Linux administration, and recovery exercises.

## Start small

The first useful milestone is one Windows Server and one Windows client on an isolated virtual switch. Domain join, name resolution, and ordinary account access should work before adding extra services.

| Component | Intended exercise | Current state |
| --- | --- | --- |
| Hyper-V | VM creation and isolated networking | Planned |
| AD DS / DNS | Domain join, accounts, groups, and name resolution | Planned |
| DHCP | One documented lease authority per segment | Planned |
| Linux utility VM | Administration and service checks | Planned |
| pfSense / Pi-hole / VLANs | Optional later networking exercises | Not part of the first build |

## Build documents

- [Architecture and topology](docs/architecture.md)
- [Build and validation sequence](docs/build-sequence.md)
- [First Windows snapshot exercise](docs/first-windows-exercise.md)
- [Lab report template](templates/lab-report.md)
- [Evidence index](evidence/README.md)

The diagram is a proposed design. Separate virtual switches do not demonstrate working VLAN tagging, and the drawing is not proof of routing or firewall configuration.

## First acceptance checks

- Record actual hardware limits, licenses, VM allocations, and OS versions.
- Join the test client and verify its expected DNS/identity behavior.
- Test an ordinary user's allowed and denied access.
- Restore a backed-up configuration to a disposable target and verify the service.

No equipment inventory, screenshots, measured recovery time, or successful restore is claimed yet. Proxmox is a possible alternative to Hyper-V, not a second claimed deployment. Snapshots are a convenience; they are not an independent backup.

[MIT license](LICENSE) · [Security](SECURITY.md)
