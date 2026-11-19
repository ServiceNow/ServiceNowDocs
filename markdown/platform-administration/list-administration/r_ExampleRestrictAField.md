---
title: Field restriction example
description: This access control prevents everyone except an administrator from editing the Short description field of an incident record in a list.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/list-administration/r\_ExampleRestrictAField.html
release: australia
product: List Administration
classification: list-administration
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Contextual security, List editor, Administer, List administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Field restriction example

This access control prevents everyone except an administrator from editing the Short description field of an incident record in a list.

\[Omitted image "RestrictTheIncidentShortDescription.png"\] Alt text: Access control that restricts list editing on the Short description field on the Incident table to admins.

-   **Type:** record
-   **Operation:** list\_edit
-   **Decision Type:** Allow If
-   **Name:** Incident \[incident\], Short description
-   **Admin overrides:** Select the check box.
-   **Role:** admin

