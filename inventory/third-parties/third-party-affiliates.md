---
description: Two ways a vendor relationship can grow in scope
---

# Third-Party Affiliate vs Engagement

Lema makes a deliberate distinction between two ways a vendor relationship can grow in scope. Choosing the right model keeps your inventory clean, your assessments accurate, and your risk picture honest.

### The Core Question

> **Does this new relationship share the same assessment boundaries as the existing vendor — or does it need its own?**

If the answer is **same boundaries** → it's an **Engagement**.&#x20;

If the answer is **its own boundaries** → it's an **Affiliated Third-Party**.

### Engagements

An engagement represents a change or expansion within an existing vendor relationship that falls under the same assessment scope. The vendor's core artifacts, controls, and cadence remain the primary reference — you're only assessing the delta.

Use an engagement when:

* A vendor is rolling out a new feature or product module (e.g., Atlassian enabling AI features)
* A professional services component is added to an existing contract
* A contract is updated to cover new regions, departments, or use cases (e.g., additional sites in Zendesk)
* A usage increase or scope change doesn't meaningfully change the risk boundary

In most cases, the same SOC 2 or pen test covers the engagement. You review only the controls that are affected by the change — not the full vendor from scratch.

{% hint style="info" %}
Engagements are assessed together with the parent vendor in the next assessment cycle unless the change warrants an immediate scoped review. See Engagements for details.
{% endhint %}

### Affiliated Third Parties

**Assessment boundaries** define what a single audit covers — the systems, data, and controls within scope. If an entity has its own compliance certifications, infrastructure, or legal structure, it operates outside the parent's boundary and needs to be assessed on its own terms.

The simplest test: **does it have its own SOC 2?** If a separate auditor drew a separate circle around it — it's an affiliated third-party.

An affiliated third-party is a subsidiary, brand, or standalone product that operates within its own assessment boundaries — its own artifacts, controls, cadence, and potentially its own contract. It behaves as an independent vendor in Lema, but is linked to a parent to preserve the relationship.

Use an affiliated third-party when:

* The entity has its own compliance certifications (e.g., its own SOC 2 report)
* It operates under a separate legal entity or brand
* It requires a fully independent assessment with different controls and cadence
* The risk profile is meaningfully different from the parent

**Examples:**

* Atlassian → Trello, Loom (separate products, separate compliance posture)
* Proofpoint → Cloudmark, DLP (distinct services with independent boundaries)

### Side by Side

|                        | Engagement                                        | Affiliated Third-Party                 |
| ---------------------- | ------------------------------------------------- | -------------------------------------- |
| **What it represents** | A change in scope within an existing relationship | A standalone entity linked to a parent |
| **Assessment scope**   | Delta only — diff controls from the parent        | Fully independent assessment           |
| **Artifacts**          | Shared with parent vendor                         | Own artifacts, own certifications      |
| **Cadence**            | Follows parent's cadence                          | Independent cadence                    |
| **Contract**           | Usually same contract                             | May have its own contract              |
| **Example**            | Atlassian adding AI features                      | Atlassian → Trello                     |

{% hint style="warning" %}
When in doubt, ask: _"Would a separate auditor assess this independently?"_ If yes — it's an affiliated third-party. If the same audit covers it — it's an engagement.
{% endhint %}
