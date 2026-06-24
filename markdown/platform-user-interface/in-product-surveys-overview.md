---
title: In-Product Surveys
description: Manage in-product surveys for your Next Experience instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/in-product-surveys-overview.html
release: zurich
topic_type: concept
last_updated: "2026-05-11"
reading_time_minutes: 1
breadcrumb: [Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# In-Product Surveys

Manage in-product surveys for your Next Experience instance.

In-product surveys collect feedback from users as they work in Next Experience. Surveys appear based on user activity and eligibility criteria. The feature is automatically installed and activated as part of the family release. Administrators who do not want in-product surveys can skip or defer the plugin during patch installation or turn it off after installation.

## System properties

Use the following property to turn off in-product surveys on your instance.

<table><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`in.product.surveys.enabled`

</td><td>

Controls whether in-product surveys are enabled on the instance. When `true`, surveys are active. When `false`, surveys are inactive and the feature makes no network calls.Default: `true`

</td></tr></tbody>
</table>## Survey appearance

Users see the following survey in workspaces and classic views.

\[Omitted image "survey.png"\] Alt text: In-Product Survey showing a 5-star rating scale and a text field for additional feedback.

Survey content shown is an example. Actual surveys reflect the ServiceNow product the user is working in.

The survey asks users to rate their experience on a 5-star scale and optionally provide additional feedback.

**Parent Topic:**[Configuring the Next Experience UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/next-experience-ui-admin.md)

