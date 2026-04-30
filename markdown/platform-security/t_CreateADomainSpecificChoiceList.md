---
title: Create a domain-specific choice list
description: Administrators can configure choice lists to contain entries specific to a particular domain.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Domain separation setup and administration, Domain separation for service providers, Access Management]
---

# Create a domain-specific choice list

Administrators can configure choice lists to contain entries specific to a particular domain.

## Before you begin

Role required: admin

## Procedure

1.  Select the domain from domain picker where the choice should be added.

2.  Right-click the choice field you want to customize and select **Configure Choices**.

3.  Update or add choices.

4.  Push changes through the normal change process such as update sets.

    **Note:** Administrators should ensure that choices are unique across domains to prevent administrative confusion in the global domain.

    If an administrator adds a new choice from the global domain, then users from domains lower in the hierarchy see the new choice at the end of their current choice lists. If the new choice is not active at the global level, then it is available to the domain users via **Configure Choices** but does not show as an active choice.


