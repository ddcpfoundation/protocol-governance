# DDCP Protocol Change Policy

This policy governs changes to the DDCP protocol, its specification and the reference implementation published by DDCP Foundation Inc. It applies to the repositories the Foundation maintains. It does not govern any currency built using the protocol, and it gives the Foundation no authority over such a currency.

Published by DDCP Foundation Inc. Licensed under CC BY 4.0.

## 1. Who may merge

Until a broader maintainer group exists, merge authority rests with the Foundation's maintainers, listed in the reference repository's MAINTAINERS file. A change enters the reference implementation only through a reviewed pull request with a Developer Certificate of Origin sign-off. Code is licensed under Apache-2.0 and stays under it.

## 2. The never-merge list

The DDCP Manifesto states what the protocol will never introduce. No change containing any of the following enters the protocol, the specification or the reference implementation, whatever its source or justification:

- administrative freeze functions of any kind;
- spending restrictions limiting what value can be exchanged for;
- expiry conditions causing holdings to lapse;
- behavioral conditions making access contingent on compliance with external criteria;
- general-purpose programmable logic deployable by third parties at the protocol layer.

A proposal containing any of these is closed with a reference to this section. The Foundation's maintainers do not have discretion over this list. Capability outside the conforming profile belongs in a fork maintained by the issuer that needs it, never in Foundation code.

## 3. Changes touching a listed item or a criterion

A change that touches any item on the never-merge list requires a published rationale and the approval of the Foundation's board before it can be merged. A change to the DDCP conformance criteria (CRITERIA.md) that would weaken what a criterion requires on any of those items is such a change. The rationale is published in this repository before the board decides, and the decision is published with it.

Any other change to the conformance criteria is decided by the Foundation. Its rationale is published in this repository before the change takes effect, and the decision is published with it.

## 4. What a change applies to

A change to the protocol governs the reference implementation and what is built using it afterward. It never applies to a currency already issued.

- No board decision and no community process is represented as the consent of the people holding an existing currency. No one is entitled to consent on their behalf.
- The DDCP conformance evaluation registry is never used to press an issued currency to adopt a change.
- A currency built using an earlier version of the reference is evaluated against the conformance criteria as published when it is examined, and its specification states which of its properties were settled at issuance.
- A defect found in a version of the reference implementation is disclosed in a security advisory and in the release note of the version that corrects it, naming the versions affected. Where the defect bears on a conformance criterion, the reference implementation's Known Limits against DDCP records it under that criterion. The disclosure states the migration path open to a currency whose program can no longer be upgraded: a new mint on the corrected version, with holders moved by that currency's issuer through redemption and reissue. Mints on a defective version are never moved by anyone else.

## 5. Ordinary changes

Changes that touch no listed item or criterion are merged by the maintainers after review. These include corrections, documentation, tests, build tooling and dependency updates. Where a change alters what the reference implementation does, the Known Limits against DDCP and the specification are updated in the same change.

## 6. Amendments to this policy

An amendment to sections 2 to 4 requires the approval of the Foundation's board and is published with its rationale before it takes effect. The Foundation's bylaws carry the never-merge list as a purpose restriction; this policy cannot relax it.

## 7. Contact

Proposals are made as issues or pull requests in the reference repository. Security matters follow the reference repository's SECURITY file, not this policy.
