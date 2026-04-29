---
title: Using Developer Support
description: Learn more about using Developer Support and helpful information when submitting a developer request with Impact.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Impact Developer Support, Platform Health, Using Impact, Impact]
---

# Using Developer Support

Learn more about using Developer Support and helpful information when submitting a developer request with Impact.

## Developer Support Boundaries

-   **General**

    Developer Support is available Monday – Friday, 09:00 – 17:00, based on the local time zone of the case communication.

    -   Cases are opened with P3 priority, and aren’t eligible for escalation. For more information on response time and SLA, see [https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB0547260](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0547260).
    -   Developer Support cases are investigated on a subprod instance. All issues must be reproducible on a subprod instance.
    -   Available to self-hosted customer instances via a modified delivery model.

**Note:** Developer Support isn’t currently available in the Australia IRAP-Protected datacenters or in certain other restricted environments.

## Parameters

There are certain parameters to consider when submitting a Developer Support case, as described in the following sections.

-   **Users:**

    -   The named contact is responsible for ensuring that each case opened describes a specific issue and that the section of code referenced is isolated to a narrow band of code not to exceed 200 lines.
    -   Available to the number of designated users per Impact Package subscription \(not including customer system administrators\):
        -   Five for Advanced Impact package
        -   Ten for Total Impact package
    **Note:** See [Manage Developer Support user access](../task/manage-developer-support-user-access.md) to designate users.

-   **Infrastructure:**
    -   Supported version\(s\) of the release/feature/application/hardware are required
    -   English is the only supported language
    -   Troubleshooting or debug of third-party applications or assessment of security vulnerabilities are not included
-   **Integrations:**

    Integration support is only performed within a ServiceNow instance or infrastructure and includes:

    -   Questions on ServiceNow APIs
    -   Scripts to consume the data from the integration \(only if the data is imported as expected\)
    -   Transform Map scripts

