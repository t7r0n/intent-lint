# Decision Report: Intent Lint

An open developer toolkit + benchmark that lets an AI app dev simulate, audit, and gate Intent Lint style intent ad insertions before they ship - turning "trust the network" into "trust and verify in CI."

## Evidence-Grounded Findings

CLAIM: claim regression harness should `open a regression issue with trace and benchmark delta` because blocks=3 reviews=5 mean_severity=2.528. [EVID: ev_0022]
CLAIM: evidence replay should `block release until cited evidence is regenerated` because blocks=4 reviews=5 mean_severity=2.611. [EVID: ev_0000]
CLAIM: handoff boundary probe should `route to reviewer with evidence packet` because blocks=3 reviews=4 mean_severity=2.528. [EVID: ev_0033]
CLAIM: review operator packet should `accept only if decision claims cite fixture evidence` because blocks=4 reviews=5 mean_severity=2.556. [EVID: ev_0099]
