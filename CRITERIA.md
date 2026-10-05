# DDCP Conformance Criteria

The criteria against which the DDCP conformance evaluation examines a currency. Each criterion is extracted from the DDCP Manifesto (v20260924-3) and names the Manifesto section it answers to. The evaluation records, per criterion, whether the currency delivers it, partly delivers it, or does not deliver it, with evidence. It is not a verdict on the currency as a whole.

A capability an issuer can still acquire is examined as a capability the issuer holds. Privacy is examined together with the currency's fee configuration. Authority allocation is examined as a criterion of its own.

Published by DDCP Foundation Inc. Licensed under CC BY 4.0.

| # | Area | Criterion | Manifesto section |
|---|---|---|---|
| 1 | Control | No administrative key, freeze function or master key held by any issuer, government or intermediary over value held in self-custody. | Your Keys, YOUR Money |
| 2 | Unconditionality | No spending restrictions, no expiry conditions, no behavioral conditions, and no general-purpose programmable logic deployable by third parties at the protocol layer. | On Unconditionality |
| 3 | Settlement | No single government can determine whether a transfer settles. | On Unconditionality |
| 4 | Privacy: balance and amount | The balance held in an account and the amount of each transaction are concealed. Examined together with the fee configuration, because a fee decryption key can narrow amounts. | On Financial Privacy |
| 5 | Privacy: sender and receiver | The identity of the initiating party and of the receiving party are concealed. | On Financial Privacy |
| 6 | Privacy: timing and frequency | The timing and frequency of an account's activity are concealed. | On Financial Privacy |
| 7 | Lawful access | Identity and records are reachable through judicial process at the points where people enter and leave the system, through licensed intermediaries; no administrative override. | On Financial Privacy; On Crime |
| 8 | Backing | Fully backed against what the currency promises to be worth, and verifiable rather than asserted: by anyone against public supply, or by a named independent attestor. | On Value Preservation |
| 9 | Reserve structure | Reserve management separated from issuance and entrusted to an independent foundation; reserves ring-fenced per currency; independently attested. | On Value Preservation |
| 10 | Reserve dispersion | No single government can reach a decisive share of the reserves, or the regulatory constraint preventing this is disclosed in the currency's specification. | On Value Preservation |
| 11 | Fee ceilings | A rate ceiling and an absolute per-transfer ceiling fixed at issuance and never raised, so no fee authority can take an unbounded share of a transfer. Examined together with the program's upgrade arrangement, which conditions it, and disclosed with it. | On Unconditionality; On Honesty and the Long Game |
| 12 | Authority allocation | Each retained authority is held by the agent the criterion requires: reserve co-signature independent of the issuer; upgrade authority under a time-delayed multisig or none, with member keys distinct from co-signer keys; a stated rule for replacing co-signer keys, including who can replace the issuer; metadata authorities under multi-party control once the currency carries value. No single agent holds authorities that together allow seizure, halting or dilution. | Your Keys, YOUR Money; On Honesty and the Long Game |
| 13 | Disclosure of capabilities | A published specification stating which capabilities the issuer holds over the currency and under what conditions they may be used. | On Honesty and the Long Game |
| 14 | Disclosure of mutability | The specification states which of the currency's properties were settled at issuance and which its issuer can still change. | On Honesty and the Long Game |
| 15 | Known Limits against DDCP | The currency publishes a record of what it does not deliver against these criteria, each entry naming the criterion it answers to, accurate as examined. | On Honesty and the Long Game |
| 16 | Basics and payments | Divisible, portable, fungible, durable, counterfeit-proof; fast, low-cost and available at all hours. | Quality 1; Quality 2 |

## How the criteria are read

- Criteria 1 to 3 and 11 to 12 are examined on the mint, its program and the authorities each retains. Criteria 4 to 7 are examined on the mint's privacy configuration and its fee configuration together. Criteria 8 to 10 are examined on the currency's published specification and whatever attestation it names; the protocol does not enforce them. Criteria 13 to 16 are examined on the specification, the currency's Known Limits against DDCP, and the deployed instance.
- The absence of an evaluation is neither an endorsement nor a judgment.
- Changes to these criteria follow the protocol change policy.
