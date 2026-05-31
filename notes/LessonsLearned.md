# Lessons Learned
---

## 2026-01-29 — Network reachability (ICMP failures)

### Context
Host-to-host ping from Windows host to Linux VM on isolated lab subnet (`10.10.10.0/24`).

### Issue
Intermittent ICMP failures: “Destination host unreachable” / timeouts.

### Root Cause
Misalignment between interface configuration and routing / subnet expectations (interface up, but route/gateway/firewall state inconsistent).

### Fix
- Confirmed NIC binding to the lab switch/interface
- Validated static IP + subnet mask on both endpoints
- Checked host firewall rules affecting ICMP
- Confirmed route table points `10.10.10.0/24` to the correct interface

### Verification
- Successful ICMP both directions
- Stable connectivity under repeated tests
- Packet capture confirmed ARP resolution + ICMP echo/reply

---


