# IP Plan: Serendib Freight

## Networks
| Network | Range | Notes |
|---|---|---|
| Office (on-premises) | 192.168.0.0/16 | Already in use. Cannot change. |
| Azure | 10.1.0.0/16 | 65,536 addresses. Chosen for Azure. |

## Why these do not overlap
The office range starts with 192.168 and the Azure range starts with 10.1.
Because the first numbers are different, no address can belong to both,
so the two networks can be connected later without conflict.

## Subnets inside 10.1.0.0/16 (to do this week)
| Subnet | Range | Purpose |
|---|---|---|
| TBD | | |
