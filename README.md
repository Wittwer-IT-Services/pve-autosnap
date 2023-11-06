# pve-autosnap
Simple script for automating creating PVE KVM snapshots. It checks if the VM has a tag and only makes backups when the defined tag exists.

## Usage:
pve-autosnap [tag] [prefix] [keep]

## Examples

### Cronjobs
```bash
# Create a daily snapshot of VMs with `autodaily` tag
0 2 * * * /usr/bin/pve-autosnap autodaily autodaily 7
# Create a weekly snapshot of VMs with `autoweekly` tag
0 3 * * 0 /usr/bin/pve-autosnap autoweekly autoweekly 5
# Create a monthly snapshot of VMs with `automonthly` tag
0 4 1 * * /usr/bin/pve-autosnap automonthly automonthly 12
```
