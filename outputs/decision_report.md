# Decision Report: Intent Lint

An open developer toolkit + benchmark that lets an AI app dev simulate, audit, and gate Imprezia style intent ad insertions before they ship - turning "trust the network" into "trust and verify in CI."

## Evidence-Grounded Findings

CLAIM: imprezia drift should `block release until replay is understood` because blocks=2 reviews=3 mean_severity=2.5. [EVID: ev_0088]
CLAIM: imprezia evidence recall should `block release until replay is understood` because blocks=3 reviews=3 mean_severity=1.875. [EVID: ev_0132]
CLAIM: inside policy boundary should `block release until replay is understood` because blocks=2 reviews=3 mean_severity=1.708. [EVID: ev_0033]
CLAIM: integration failure replay should `block release until replay is understood` because blocks=2 reviews=4 mean_severity=3.333. [EVID: ev_0044]
CLAIM: pitch gap should `block release until replay is understood` because blocks=3 reviews=2 mean_severity=3.333. [EVID: ev_0143]
CLAIM: pitch reviewer handoff should `block release until replay is understood` because blocks=2 reviews=4 mean_severity=2.583. [EVID: ev_0121]
