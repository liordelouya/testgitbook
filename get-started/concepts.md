# Core Concepts

Lema is built around a set of core concepts that work together to automate third-party risk management. This page explains what each concept is and — more importantly — what makes it work differently in Lema than in traditional TPRM tools.

### Third Party

A third party is any external organization your company has a relationship with — a SaaS vendor, a contractor, a cloud provider. In Lema, a third-party profile is not a static record. It's a living entity: continuously monitored for adversarial signals, automatically enriched with fourth-party dependencies, and always reflective of the vendor's current risk posture.

You don't need to manually update vendor profiles. Lema does it.

### Affiliated Third Party

An affiliated third party is a distinct legal or operational entity that sits under the umbrella of a parent vendor. Think of a regional subsidiary or a separate product company that shares the same brand.

The key question: does this entity have its own compliance posture — its own SOC 2, its own controls? If yes, it's an affiliate with its own independent risk profile. If it doesn't operate independently from a security standpoint, model it as an engagement instead.

### Engagement

An engagement represents a specific business relationship with a third party — a particular product, service tier, or contract. Where an affiliate is assessed independently, an engagement shares the parent vendor's controls, findings, and artifacts.

Use engagements when a vendor serves your organization in multiple distinct ways that each carry different risk (for example, a vendor providing both a SaaS product and professional services). Engagement risk rolls up into the parent vendor's overall risk score.

### Projects

A project is the internal organizational layer that connects a team of assessors to a specific set of scopes and controls. It represents a business unit, a team, or an assessment program — for example, "Procurement Team" or "Security Reviews."

Scopes are attached to projects, so the controls evaluated in an assessment depend on which projects are involved. When multiple teams participate in the same assessment — say, Security and Legal — each brings their own project and its associated scopes. The result is a single assessment that covers the right controls for each team, without overlap or redundancy.

### IRQ

The Inherent Risk Questionnaire is a structured set of questions that determines how risky a vendor is _before_ any assessment begins. It covers data types, operational footprint, spend, attack surface, and service delivery.

In Lema, the IRQ is not a form you fill out from scratch. Lema pre-populates it using AI-powered estimation based on the vendor's domain and profile data. The answers directly determine which scopes activate in an assessment and set the baseline for the assessment score calculation. Getting the IRQ right is the single most important step before starting an assessment.

### Controls

A control is a specific security question with a yes/no answer: does the vendor do this? In Lema, each control is an AI agent. It doesn't wait for you to check evidence manually — it reads uploaded artifacts, integration data, and questionnaire responses, and evaluates the control automatically.

Controls are weighted by importance (1–5). Weight 5 controls are foundational — if one fails, the vendor cannot score Acceptable regardless of how well everything else performs. Each control belongs to exactly one scope, and disabled controls are visible but don't run.

### Scopes

A scope is a rule-based group of controls that activates only when a vendor meets specific conditions — based on their inherent risk level and IRQ responses. Instead of running every control for every vendor, Lema activates only the controls that are relevant to the actual risk of each relationship.

A critical vendor processing health data gets a different set of controls than a low-risk software vendor. Scopes make this automatic. Multiple scopes can apply within a single assessment.

### Assessment

An assessment in Lema is faster than you expect. Before a vendor is ever contacted, Lema evaluates all in-scope controls against existing evidence: artifacts already on file, data from connected integrations, previous questionnaire responses. Only controls that can't be validated automatically require vendor input.

Vendors aren't burdened with a 200-question form when Lema already has the answers. The assessment closes faster, vendor relationships are preserved, and your team focuses on gaps instead of gathering data that's already there.

### Smart Evidence Request

When controls can't be automatically validated, Lema generates a Smart Evidence Request — a targeted, AI-curated ask sent directly to the vendor. It lists exactly what's missing, explains why it's needed, and links to the vendor portal for upload.

This is not a generic questionnaire. It's a precise request built from what the assessment actually needs. Vendors respond faster, and your team doesn't review evidence it didn't ask for.

### Assessment Score

The Assessment Score translates control outcomes into a single qualitative verdict: **Acceptable**, **Concerning**, or **Unacceptable**. It's not a simple pass rate — it's a weighted calculation that accounts for how important each control is and how risky the vendor was to begin with.

A vendor with a 90% pass rate might still score Concerning if they failed an encryption control. A vendor with a 60% pass rate might score Acceptable if everything they missed was administrative noise. The score reflects real exposure, not just volume of validated controls.
