---
title: Quality implementation
description: A product non-conformance case \(PNCC\) captures a reported quality issue, and a product quality investigation \(PQI\) analyzes its root cause for resolution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/manufacturing/mco-quality-implementation.html
release: australia
topic_type: concept
last_updated: "2026-07-13"
reading_time_minutes: 2
keywords: [Quality management implementation, product non-conformance case, PNCC, product quality investigation, PQI, quality management, CAPA]
breadcrumb: [Configure, Manufacturing Commercial Operations]
---

# Quality implementation

A product non-conformance case \(PNCC\) captures a reported quality issue, and a product quality investigation \(PQI\) analyzes its root cause for resolution.

This implementation provides the foundation for configuring Manufacturing Commercial Operations quality management applications.

\[Omitted image "mco-quality-Implementation.png"\] Alt text: Quality workflow

The infographic shows the quality workflow. A submitter or resolver creates a PNCC, and a resolver triages and assigns it. For recurring defects, a PQI Lead or PQI Member opens a PQI to analyze the root cause and drive CAPA \(Corrective, Containment, and Preventive Action\).

## Product non-conformance

A product non-conformance case \(PNCC\) is the customer and dealer-facing record for a reported product quality issue. It extends the complaint case hierarchy \(sn\_complaint\_case → sn\_customerservice\_case → task\). A resolver works the PNCC through a staged playbook in the Customer Service Management \(CSM\) Configurable Workspace.

A PNCC can be created in two ways:

-   By a submitter \(dealer or field technician\) through the Dealer Portal record producer
-   Directly by a resolver in the CSM/Field Service Management \(FSM\) Configurable Workspace

Submitter users can only see and create non-conformances \(NCs\) on install base items \(IBIs\) that are linked to their assigned account or service organization. Each submitter is scoped to their organizational unit — they can't access or report issues on other accounts' assets.

What submitters can see:

-   Install base items linked to their account
-   Install base items linked to their service organization \(if assigned\)

What submitters can log:

-   New NCs on any IBI they have visibility to
-   NCs automatically scoped to the account or service organization of the selected IBI

When a submitter creates and submits an NC \(Draft → New state\), the system assigns a resolver to triage and work the case. Triage is the process of categorizing the NC by priority, assigning it to the right resolver, and preparing it for investigation.

## PQI implementation

A product quality investigation \(PQI\) is the internal record where a PQI Lead or PQI Member analyzes the root cause of a defect. The PQI Lead or PQI Member then drives CAPA.

A single PQI can consolidate many related PNCCs, so a recurring defect is investigated once.

A PQI can be created in two ways:

-   Resolver using the **Create Quality Investigation** action on a PNCC — the PNCC is automatically linked to the new PQI
-   PQI Lead using the workspace for systemic issues

