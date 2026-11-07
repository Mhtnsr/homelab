# First Windows exercise: collect and explain an endpoint snapshot

Status: exercise prepared; no personal lab execution is claimed by this page.

## Goal

Run the support snapshot tool on an owned, disposable Windows VM and explain what each field establishes. This is a baseline validation exercise, not a simulated customer incident.

## Prerequisites

- An owned test VM with a documented Windows version and authorized PowerShell execution method.
- The `it-support-playbook` repository reviewed and downloaded locally.
- A private working folder for raw output and screenshots.
- A recovery checkpoint if desired; the commands below are read-only.

## Steps

1. Record the date, hypervisor, OS version, and how you obtained the source. Keep identifiers private.
2. From the support playbook root, run:

```powershell
./toolkit/Test-SupportSnapshot.ps1
./toolkit/Get-SupportSnapshot.ps1
./toolkit/Test-WindowsSnapshot.ps1
```

3. Inspect OS status, memory capacity, disk capacity/free percentage, and spooler collection state.
4. Compare the reported capacity with Windows' own display. Note units and rounding.
5. Explain why a running spooler does not prove a print job succeeds, and why free capacity does not diagnose disk performance.
6. Record any unavailable collector or failure as observed. Do not convert it to a pass.
7. Review/crop a screenshot so it shows only commands and the allowlisted report. Hide browser tabs, notifications, names, paths, network addresses, and account/device identifiers.
8. Use `templates/lab-report.md` to record expected versus observed behavior and remaining limits.

## Acceptance criteria

- Fixture checks pass.
- The live integration check successfully reads OS and at least one fixed disk.
- Every emitted field is on the known schema allowlist.
- The report can be explained without claiming to have resolved an incident.
- A real sanitized evidence file and its caption exist before the exercise is marked complete.

No screenshots or completed home-lab result are supplied by this template. CI runner results, if linked elsewhere, must remain labeled as hosted-runner evidence.
