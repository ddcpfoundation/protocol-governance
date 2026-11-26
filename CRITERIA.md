# DDCP Evaluation Criteria

The criteria against which a DDCP Evaluation examines a currency, or an implementation as code. Each criterion is extracted from the DDCP Manifesto (v20260924-4) and names the Manifesto section it answers to. For each criterion, the evaluation records whether the currency delivers it, partly delivers it, or does not deliver it, with evidence; an evaluation of an implementation may also record that a criterion is not deliverable by code alone (see the evaluation methodology). It is not a verdict on the currency or the implementation as a whole.

A capability an issuer can still acquire is examined as a capability the issuer holds. Privacy is examined together with the currency's fee configuration. Authority allocation is examined as a criterion of its own.

Published by DDCP Foundation Inc. Licensed under CC BY 4.0.

| # | Area | Criterion | Manifesto section |
|---|---|---|---|
| 1 | Basics and payments | Divisible, portable, fungible, durable, counterfeit-proof; fast, low-cost and available at all hours. | Quality 1; Quality 2 |
| 2 | Control | No administrative key, freeze function or master key held by any issuer, government or intermediary over value held in self-custody. | Your Keys, YOUR Money |
| 3 | Unconditionality | No spending restrictions, no expiry conditions, no behavioral conditions, and no logic that runs on the currency's own transfers at the direction of anyone other than the parties to the transfer, whether the issuer or someone it appoints. Conditions set by a program a holder chooses to use are not conditions of the currency. | On Unconditionality |
| 4 | Settlement | No single government can determine whether a transfer settles. | On Unconditionality |
| 5 | Privacy: balance and amount | The balance held in an account and the amount of each transaction are concealed. Examined together with the fee configuration, because a fee decryption key can narrow amounts. | On Financial Privacy |
| 6 | Privacy: parties and timing | The identities of the initiating and receiving parties, and the timing and frequency of an account's activity, are concealed. | On Financial Privacy |
| 7 | Fee ceilings | A rate ceiling and an absolute per-transfer ceiling fixed at issuance and never raised, so no fee authority can take an unbounded share of a transfer. Examined together with the program's upgrade arrangement, which conditions it, and disclosed with it. | On Unconditionality; On Honesty and the Long Game |
| 8 | Authority allocation | Each retained authority is held by the agent the criterion requires: reserve co-signature independent of the issuer; upgrade authority under a time-delayed multisig or none, with member keys distinct from co-signer keys; a stated rule for replacing co-signer keys, including who can replace the issuer; metadata authorities under multi-party control once the currency carries value. No single agent holds authorities that together allow seizure, halting or dilution. | Your Keys, YOUR Money; On Honesty and the Long Game |
| 9 | Lawful access only through judicial process | Identity and records are reachable only through judicial process directed at an identified person, at the licensed intermediaries where people enter and leave the system; no administrative override reaches value held in self-custody. | On Financial Privacy; On Crime |
| 10 | Backing | Fully backed against what the currency promises to be worth, and verifiable rather than asserted: by anyone against public supply, or by a named independent attestor. | On Value Preservation |
| 11 | Reserve structure | Reserve management separated from issuance and entrusted to an independent foundation; reserves ring-fenced per currency; independently attested. | On Value Preservation |
| 12 | Reserve dispersion | No single government can reach a decisive share of the reserves, or the regulatory constraint preventing this is disclosed in the currency's specification. | On Value Preservation |
| 13 | Accurate disclosure of security and capabilities | A published specification accurately states which capabilities the issuer holds over the currency and under what conditions they may be used; the cryptographic and security assumptions the currency relies on; whether its code has had an independent security audit and which commit it covers; and what holders are exposed to if an assumption fails, including encrypted history already recorded on chain. | On Honesty and the Long Game; Your Keys, YOUR Money |
| 14 | Disclosure of mutability | The specification states which of the currency's properties were settled at issuance and which its issuer can still change. | On Honesty and the Long Game |

## How the criteria are read

- Where each group of criteria is examined:
  - Criteria 2 to 4, 7 and 8: on the mint, its program and the authorities each retains.
  - Criteria 5, 6 and 9: on the mint's privacy configuration and its fee configuration together.
  - Criteria 10 to 12: on the currency's published specification and whatever attestation it names; the protocol does not enforce them.
  - Criteria 1, 13 and 14: on the specification and the deployed instance.
- Example for criterion 3: on Solana's Token-2022 program, logic that runs on every transfer of a currency is a Transfer Hook.
- For criterion 13, the assumptions include whether the cryptography would resist a quantum computer, and what a holder loses if it does not, for control and for privacy.
- The Foundation recommends that every currency publish its own Known Limits against DDCP, a record organized by these criteria of what it does not deliver. It is not a criterion; see the evaluation methodology.
- The absence of an evaluation is neither an endorsement nor a judgment.
- Changes to these criteria follow the protocol change policy.
