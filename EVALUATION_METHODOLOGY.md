# DDCP Evaluation Methodology

How DDCP Foundation Inc examines a currency, or an implementation as code, against the DDCP Evaluation Criteria and publishes the result. An evaluation is a per-criterion record, not a verdict. The published evaluations together form the DDCP Evaluations Registry.

Published by DDCP Foundation Inc. Licensed under CC BY 4.0.

## 1. What an evaluation is

An evaluation examines, against every criterion in CRITERIA.md, either one currency, on one chain, at one point in time, or one implementation, as code at a named commit. For each criterion it records a result, with the evidence that supports it.

For a currency, one of three results:

- **Delivered.** The criterion is met as a structural fact of the currency as deployed.
- **Partly delivered.** Part of the criterion is met; the record states which part and what is missing.
- **Not delivered.** The criterion is not met, or the issuer retains the capability to defeat it.

For an implementation, the same three results, where "delivered" means the criterion is met as a structural fact of the code whatever choices a currency built using it makes, or a fourth:

- **Not deliverable by code alone.** The code enables it or partly delivers it; whether it is delivered depends on choices each currency makes, at its creation or outside the code.

The fourth result is recorded only where every part of the criterion the code does not deliver could be delivered by choices a currency makes. Where a part remains that no currency's choice can deliver, the result is partly delivered or not delivered. It is never recorded for a currency, whose choices are made and are examined.

Where a criterion depends on choices the code leaves to whoever creates a mint, the record states what the code fixes, what it leaves open, and every choice it permits that would defeat the criterion, whatever the result, so that a currency built using the code knows which choices defeat it.

An implementation is examined as it would run in a deployment that carries value. For the reference implementation, the Foundation's devnet demonstration is evidence of how it behaves.

No overall score, grade or badge is derived from the results. A currency that meets some criteria and not others is recorded as exactly that. A currency is evaluated against the criteria as published when it is examined, whichever version of the reference implementation it was built using.

## 2. Who evaluates

The registry records the Foundation's own evaluations only, and is never used to press an issued currency to adopt a change to the protocol. An issuer may submit a self-evaluation. The Foundation treats it as input to its own examination and may cite it, but it is not published as an entry in the registry, and its conclusions are not adopted without examination.

Each evaluation states any relationship between the Foundation, its directors, officers or funders and the issuer of the currency examined. Where the Foundation examines its own implementation, the record states that the evaluation is not independent.

## 3. The evidence standard

A result rests on three kinds of evidence, each named in the record:

1. **On-chain inspection of the mint.**
   - What is read: the extensions it carries, every authority it retains and who holds each, the fee configuration and its ceilings, the program the mint depends on, and that program's upgrade authority.
   - How: read live from the chain and recorded with the slot or date of reading.
2. **Review of the deployed code.** The program backing the mint is verified against its published source by a reproducible build. Where the deployed program cannot be reproduced from published source, the record says so, and no criterion that depends on the program's behavior is recorded as delivered.
3. **The issuer's published specification.**
   - It states the capabilities the issuer holds over the currency, the conditions under which it may use them, and which of the currency's properties were settled at issuance.
   - Criteria that the protocol does not enforce (backing, reserve structure and reserve dispersion, criteria 10 to 12) are examined on the specification and on whatever attestation it names. The record states what was examined and what was taken on the issuer's statement.

A development history is not evidence and is not required.

## 4. "Examined"

A criterion is examined when the Foundation has read the evidence named in section 3 for that criterion and recorded a result with that evidence cited. The Foundation does not describe a currency as meeting any criterion without having examined it. The absence of an evaluation is neither an endorsement nor a judgment.

## 5. Capabilities and latent authority

A capability the issuer can still acquire is a capability it holds. The specification and the mint are examined for latent authority as well as for configured capability. An authority set to none at the mint is examined for whether the program, its upgrade authority or any other party can reintroduce it. A criterion is recorded as delivered only when no party can defeat it without a change that the record identifies and whose own controls are disclosed.

In an evaluation of an implementation, the upgrade authority of the program each currency deploys, and every other arrangement each currency chooses, are choices under section 1: where only such a choice could defeat a criterion, the record names it as a choice that would defeat it. Where a party no currency chooses could defeat it, such as whoever can upgrade a program the implementation depends on, the record names that party and its controls.

## 6. Authority allocation

Authority allocation (criterion 8) is examined as its own item. The record lists:

- every authority the currency retains;
- who holds it;
- how it can be transferred or replaced;
- whether any single agent holds a combination of authorities that together allow seizure, halting or dilution.

The program's upgrade authority is examined with the fee ceilings and the mint rules it conditions, and the two are always disclosed together.

## 7. Privacy and fees

Criteria 5 and 6 are examined together with the currency's fee configuration. Where a currency charges a transfer fee, the record states the fee rate and ceilings and the band to which the withheld-fee decryption key narrows confidential amounts. This is recorded as visibility, as a fact about the configuration.

## 8. A currency's Known Limits against DDCP

The Foundation recommends that every currency publish its own Known Limits against DDCP: a record, organized by the DDCP Evaluation Criteria, of what it does not deliver. It is not a criterion, and no result depends on whether a currency publishes one.

Where one is published, the evaluation reads it as the issuer's own account, in the same way as a self-evaluation under section 2. The record states where its results differ from it.

## 9. Form of the record

Each evaluation is one file in the Foundation's evaluation registry, the repository `ddcpfoundation/conformance-evaluations`, dated and versioned. It names:

- the currency, its issuer, the chain, the mint address and the program address;
- for an implementation, instead, the commit examined and any demonstration used as evidence;
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
- a change to the DDCP Evaluation Criteria or to this methodology that affects a recorded result;
- a change in the infrastructure the currency depends on that the reference implementation's Known Limits against DDCP identifies as bounding a criterion.

A stale evaluation stays in the registry, marked with the date and reason, until a new evaluation replaces it.

## 11. Corrections

An error in a published evaluation is corrected by a dated addendum to the same file. The addendum states what was wrong, what the evidence shows and the corrected result; the original text is not rewritten. Anyone may report an error through the issues of that repository. The issuer of the currency examined is notified of any correction.

## 12. Deferred

Whether and how an issuer may pay for an evaluation, and how that is disclosed, is deferred until an issuer seeks one. No evaluation published before that decision was paid for by the issuer examined.

## 13. Changes to this methodology

Changes follow the protocol change policy. A change that affects recorded results marks the affected evaluations stale under section 10.
