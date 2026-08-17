---
title: Managing AI asset details
description: Confirm what an AI asset is, who owns it, how it operates, and what other assets depend on it before approving a change, investigating a score, or responding to an audit question.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/disc-ai-asset-details.html
release: zurich
topic_type: concept
last_updated: "2026-05-05"
reading_time_minutes: 4
keywords: [AI asset, asset record, asset details, asset relationship map, use and purpose, asset ownership]
breadcrumb: [Working with AI asset records, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Managing AI asset details

Confirm what an AI asset is, who owns it, how it operates, and what other assets depend on it before approving a change, investigating a score, or responding to an audit question.

An AI asset record stores the metadata, operating characteristics, related assets, and supporting documents that describe how the asset is built, owned, and used. The **Details** tab consolidates this information so that asset owners can keep the record current and AI stewards can reference it during reviews and audits.

The **Details** tab is available for both managed and unmanaged assets. For an unmanaged asset, it is the only tab on the record where this information appears, and is the starting point for review or onboarding.

## AI asset details

Use the **Details** section to confirm and maintain the administrative metadata that identifies an AI asset and clarifies who is accountable for it. Asset owners reference these values to keep the record current. AI stewards reference them during reviews and audits. The asset tag contains the unique ID assigned to every asset. Each asset tag consists of a type prefix followed by a 20-digit number.

For example, the **Managed by** field identifies the asset owner who keeps the record accurate and receives lifecycle tasks. The **License details** field captures the license terms that apply to the asset and is referenced during procurement reviews. The **Locations** field records the geographic locations where the asset is supported and is used to confirm coverage during data residency reviews. To update any of these values, edit them on the asset record.

## Use and purpose

Use the **Use and purpose** section to capture how an AI system operates and what outcome it produces. AI stewards reference these values to classify risk and set appropriate guardrails. Asset owners reference them when responding to audit or regulatory questions about how the asset behaves.

For example, the **System autonomy level** field records how independently the asset acts, with values that range from **Assistive \(AI suggests\)** at one end to **Fully Automated Execution** at the other. The **Intended outcome of the AI system** field records what business outcome the asset produces, with values such as **Efficiency Boost**, **Decision Guidance**, and **Automation of Tasks**. Together, these values give reviewers the context they need to classify the asset and identify the controls that apply to it. Other fields in the section capture how end users interact with the asset, the level of human involvement in its workflow, and free-text descriptions of the data it uses and the people it affects.

To update **Use and purpose** values, see [Update the use and purpose of an AI asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-asset-update-use-purpose.md).

## Asset relationship map

An AI asset can depend on other AI assets. For example, an AI system can use AI models, prompts, and datasets, and can invoke other AI systems. Use the asset relationship map to see these connections, assess the impact of a planned change, and navigate to a related asset's record.

\[Omitted image "disc-asset-relationship-map.png"\] Alt text: The asset relationship provides a visual depiction of everything related to the current AI asset.

For step-by-step guidance, see [Trace the relationships between AI assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-asset-trace-relationships.md).

## Attachments

Use the **Attachments** section to keep supporting documents with the asset record, such as model cards, dataset cards, vendor contracts, and third-party documentation. Attached files open in the embedded document viewer, so reviewers can read them without downloading the file.

-   **[Update the use and purpose of an AI asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-asset-update-use-purpose.md)**  
Update the use and purpose values for an AI asset when its operating characteristics or business outcome change so that risk classifications and governance controls continue to reflect how the asset behaves.
-   **[Use and purpose fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-asset-use-purpose-fields.md)**  
Field and value reference for the **Use and purpose** section of an AI asset record. AI stewards and AI asset owners reference these values during onboarding, reviews, and audits.
-   **[Trace the relationships between AI assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-asset-trace-relationships.md)**  
Identify the AI assets that depend on or feed into a specific AI asset to assess the impact of a planned change, investigate an unexpected evaluation score, or respond to an audit question about how data and models flow through your AI inventory.

**Parent Topic:**[Working with AI asset records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-managing-ai-assets.md)

