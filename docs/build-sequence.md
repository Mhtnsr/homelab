# Planned build and validation sequence

1. Inventory owned hardware and authorized evaluation licenses; record constraints.
2. Install/configure the chosen hypervisor; create isolated virtual switches.
3. Build one server and one client; snapshot only as a short-term recovery convenience.
4. Establish synthetic lab DNS/identity, then join the client and verify name resolution.
5. Document DHCP authority and verify the client lease on the isolated segment.
6. Create a test OU, ordinary users, and least-privilege groups; validate intended access.
7. Exercise onboarding and disabling with the lifecycle project. Record actual outcomes.
8. Add a Linux utility VM. Document administration over an approved local path.
9. Add firewall segmentation and optional Pi-hole only after baseline services work.
10. Test one controlled failure and recovery at a time; restore the normal configuration.
11. Back up critical lab configuration. Restore to a disposable target and verify service.
12. Publish sanitized evidence and the measured limitations, not an untested success claim.

Snapshots are not substitutes for independent backups. No internet-exposed admin ports
are required for this design. Establish access and rollback before any network changes.
