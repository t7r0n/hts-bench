# Failure Matrix: Hts Bench

| Scenario | Failure mode | Metric | Gate | Evidence |
| --- | --- | --- | --- | --- |
| gingercontrol evidence replay | gingercontrol_drift | gingercontrol_coverage | block release until cited evidence is regenerated | ev_0000 |
| reasoning operator packet | reasoning_blindspot | reasoning_latency | accept only if decision claims cite fixture evidence | ev_0007 |
| reasoning operator packet | reasoning_blindspot | reasoning_latency | accept only if decision claims cite fixture evidence | ev_0011 |
| claim regression harness | claim_misroute | claim_precision | open a regression issue with trace and benchmark delta | ev_0014 |
| strongest boundary probe | strongest_gap | strongest_risk | route to reviewer with evidence packet | ev_0021 |
| claim regression harness | claim_misroute | claim_precision | open a regression issue with trace and benchmark delta | ev_0022 |
| gingercontrol evidence replay | gingercontrol_drift | gingercontrol_coverage | block release until cited evidence is regenerated | ev_0028 |
