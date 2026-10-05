# DDCP Conformance Evaluation Methodology

How DDCP Foundation Inc examines a currency against the DDCP conformance criteria and publishes the result. An evaluation is a per-criterion record, not a verdict. The published evaluations together form the DDCP conformance evaluation registry.

Published by DDCP Foundation Inc. Licensed under CC BY 4.0.

## 1. What an evaluation is

An evaluation examines one currency, on one chain, at one point in time, against every criterion in CRITERIA.md. For each criterion it records one of three results, with the evidence that supports it:

- **Delivered.** The criterion is met as a structural fact of the currency as deployed.
- **Partly delivered.** Part of the criterion is met; the record states which part and what is missing.
- **Not delivered.** The criterion is not met, or the issuer retains the capability to defeat it.

No overall score, grade or badge is derived from the results. A currency that meets some criteria and not others is recorded as exactly that.

## 2. Who evaluates

The registry records the Foundation's own evaluations only. An issuer may submit a self-evaluation; the Foundation treats it as input to its own examination and may cite it, but it is not published as an entry in the registry and its conclusions are not adopted without examination.

Each evaluation states any relationship between the Foundation, its directors or its funders and the issuer of the currency examined.

## 3. The evidence standard

A result rests on three kinds of evidence, each named in the record:

1. **On-chain inspection of the mint.** The extensions it carries, every authority it retains and who holds each, the fee configuration and its ceilings, the program the mint depends on and that program's upgrade authority. Read live from the chain and recorded with the slot or date of reading.
2. **Review of the deployed code.** The program backing the mint, verified against its published source by a reproducible build. Where the deployed program cannot be reproduced from published source, the record says so and no criterion that depends on the program's behavior is recorded as delivered.
3. **The issuer's published documents.** The specification: the capabilities the issuer holds over the currency, the conditions under which it may use them, and which of the currency's properties were settled at issuance. The currency's Known Limits against DDCP: its own record of what it does not deliver against the criteria. Criteria that the protocol does not enforce, such as backing, reserve structure and reserve dispersion, are examined on the specification and on whatever attestation it names; the record states what was examined and what was taken on the issuer's statement.

A development history is not evidence and is not required.

## 4. "Examined"

A criterion is examined when the Foundation has read the evidence named in section 3 for that criterion and recorded a result with that evidence cited. The Foundation does not describe a currency as meeting any criterion without having examined it. The absence of an evaluation is neither an endorsement nor a judgment.

## 5. Capabilities and latent authority

A capability the issuer can still acquire is a capability it holds. The specification and the mint are examined for latent authority as well as for configured capability: an authority set to none at the mint is examined for whether the program, its upgrade authority or any other party can reintroduce it. A criterion is recorded as delivered only when no party can defeat it without a change that the record identifies and whose own controls are disclosed.

## 6. Authority allocation

Authority allocation (criterion 12) is examined as its own item. The record lists every authority the currency retains, who holds it, how it can be transferred or replaced, and whether any single agent holds a combination of authorities that together allow seizure, halting or dilution. The program's upgrade authority is examined with the fee ceilings and the mint rules it conditions, and the two are always disclosed together.

## 7. Privacy and fees

Criteria 4 to 6 are examined together with the currency's fee configuration. Where a currency charges a transfer fee, the record states the fee rate and ceilings and the band to which the withheld-fee decryption key narrows confidential amounts. This is recorded as visibility, as a fact about the configuration.

## 8. Known Limits against DDCP

Criterion 15 is examined by comparing the currency's Known Limits against DDCP with the results recorded for every other criterion. The record states whether each limit the evaluation finds is disclosed in the currency's own record, and whether that record claims any limit the evaluation does not find. The currency's record is evidence for criterion 15 only; no other criterion is examined against it.

## 9. Form of the record

Each evaluation is one file in the `evaluations/` folder of this repository, dated and versioned, and names:

- the currency, its issuer, the chain, the mint address and the program address;
- where the currency is built using the reference implementation, the commit of the reference it was built using;
- the date and slot of the on-chain reading;
- the result and evidence for every criterion;
- the relationship statement of section 2;
- the conditions of section 10 that would make it stale.

A new evaluation of the same currency is a new file. Earlier files are kept and never edited except under section 11.

## 10. When an evaluation becomes stale

An evaluation describes the currency at the date of its reading. It is stale, and the registry marks it so, when any of the following occurs:

- any exercise of an authority the issuer retains, including a fee change, a metadata change, an issuance pause, a key replacement or a program upgrade;
- any change to the program backing the mint, or to its upgrade authority;
- a change to the issuer's specification or to its Known Limits against DDCP;
- a change to the conformance criteria or to this methodology that affects a recorded result;
- a change in the infrastructure the currency depends on that the reference implementation's Known Limits against DDCP identifies as bounding a criterion.

A stale evaluation stays in the registry, marked with the date and reason, until a new evaluation replaces it.

## 11. Corrections

An error in a published evaluation is corrected by a dated addendum to the same file that states what was wrong, what the evidence shows and the corrected result. The original text is not rewritten. Anyone may report an error through the issues of this repository; the issuer of the currency examined is notified of any correction.

## 12. Deferred

Whether and how an issuer may pay for an evaluation, and how that is disclosed, is deferred until an issuer seeks one. No evaluation published before that decision was paid for by the issuer examined.

## 13. Changes to this methodology

Changes follow the protocol change policy. A change that affects recorded results marks the affected evaluations stale under section 10.
