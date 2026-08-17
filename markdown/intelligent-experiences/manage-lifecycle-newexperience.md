---
title: Managing your AI asset lifecycle
description: Get a structured view of an AI asset's progression through its operational stages, from initial onboarding to retirement.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/manage-lifecycle-newexperience.html
release: zurich
topic_type: concept
last_updated: "2026-04-16"
reading_time_minutes: 2
breadcrumb: [Working with AI asset records, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Managing your AI asset lifecycle

Get a structured view of an AI asset's progression through its operational stages, from initial onboarding to retirement.

When you open an AI asset record, the **Lifecycle** tab shows the current lifecycle stage of that asset. The lifecycle provides governance visibility across the full lifespan of an AI asset.

## Lifecycle stages

Lifecycle is divided into three stages, displayed as a horizontal progress indicator at the top of the tab:

-   **Onboard**

    The initial stage for a newly added AI asset. The **Onboard** sub tab contains the Onboarding playbook with tasks displayed. If tasks aren't already present in the Onboarding playbook, the sn\_ai\_governance\_ai\_steward role can create tasks by selecting **New** and assigning them to an asset owner or other AI stewards.

-   **Maintain**

    After onboarding is complete, the asset enters the Maintain stage. The **Maintain** sub tab is enabled only after onboarding is complete.

-   **Retire**

    The final stage in the lifecycle. The **Retire** sub tab is enabled only after onboarding is complete. When an AI asset is no longer needed or has been superseded, it is moved to the Retire stage. Retirement ensures the asset is formally decommissioned and removed from active use in a controlled and auditable manner.


## Creating requests for AI assets

You can manage deployed AI assets effectively by creating change requests for updates to existing assets or by creating offboarding requests for retiring assets.

AI Control Tower supports two types of requests:

-   **Change request**

    A request to modify a managed AI asset. A change request might propose switching the AI model that backs an agent, updating an asset's version, modifying the asset's use and purpose, or changing the sub-AI systems and AI models associated with the asset.

    For details, see .

-   **Offboarding request**

    A request to retire a managed AI asset. An offboarding request initiates the offboarding lifecycle stage for the asset, which removes the asset from active use and confirms that dependencies have been resolved and any data the asset produced is handled according to policy.

    For details, see .


-   **[Create change requests for AI assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-ai-asset-change-request-newexperience.md)**  
Create a change request to modify the relationships between a deployed AI asset and its related assets.
-   **[Create offboarding requests for AI assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-ai-asset-offboarding-request-newexperience.md)**  
Create an offboarding request to retire AI assets that are no longer needed.

**Parent Topic:**[Working with AI asset records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-managing-ai-assets.md)

