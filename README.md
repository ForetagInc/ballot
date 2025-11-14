# Ballot

## Security Goals

Our design is built around the following core goals:

1. Eligibility & Uniqueness
	- Only legitimate, registered voters can participate.
	- Each voter can cast at most one effective vote.

2. Ballot Secrecy
	- No one (including operators, auditors, or infrastructure providers) can link a voter’s real-world identity to their chosen candidate.
	
3. Coercion & Vote-Buying Resistance
	- Voters cannot provide reliable proof of how they voted, even if they try.
	- Coercion and vote-buying become unreliable and economically unattractive.

4. End-to-End Verifiability
	
Any observer can independently verify that:
	- All counted ballots came from eligible voters,
	- No ballots were added, removed, or modified,
	- The published tally is correct.

5. Robustness Against Insider & Infrastructure Attacks
	- No single party can undetectably alter votes or results, including administrators and infrastructure providers.

## Threat Model

We assume the presence of:
- Malicious individuals attempting fake registrations or fake ballots.
- Network attackers trying to tamper with traffic or disrupt the vote.
- Potentially dishonest insiders (system operators, administrators).
- Political actors who may attempt large-scale manipulation, coercion, or vote-buying.

We do not assume:

- Perfect physical security for all voters (e.g. no one ever watching them at home).
- Absolute immunity against an adversary who can physically detain voters until the election closes.

The system is designed so that, within realistic constraints, any attempt to manipulate votes at scale is either detectable or economically pointless.
