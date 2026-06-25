---
title: Components installed with Localization Workspace
description: Several types of components are installed with activation of the Localization Workspace plugin, including tables, user roles, and scheduled jobs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/localization-workspace/lw-components-installed-with.html
release: australia
product: Localization Workspace
classification: localization-workspace
topic_type: reference
last_updated: "2026-05-19"
reading_time_minutes: 1
breadcrumb: [Localization Workspace reference, Localization Workspace, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Components installed with Localization Workspace

Several types of components are installed with activation of the Localization Workspace plugin, including tables, user roles, and scheduled jobs.

## Components from Localization Framework used in Localization Workspace

Localization Workspace builds on functionality from Localization Framework, including tables and roles. Installing Localization Workspace also installs Localization Framework if it isn't already activated. For detailed information see [Components installed with Localization Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-framework/components-installed-with-lf.md).

## Roles installed

For detailed information about roles installed see [Localization Workspace Roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-workspace/localization-workspace-roles.md).

## Scheduled jobs installed

<table id="table_ckc_n14_52c"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Remove discarded Translation Requests

</td><td>

Runs daily to delete any abandoned translation requests \(translation requests which have been initiated but not updated for 10 days\).

 Archived or saved translation requests aren't removed. \(Saved requests display the Draft state in the My Requests list on the Home screen.\)

</td></tr></tbody>
</table>## Tables installed

<table id="table_ekc_n14_52c"><thead><tr><th>

Table label

</th><th>

Table name

</th></tr></thead><tbody><tr><td>

LW Artifact Configuration

</td><td>

\[sn\_lw\_artifact\_config\]

</td></tr><tr><td>

Glossary Source \(from version 3.0.0\)

</td><td>

\[sn\_lw\_glossary\_source\]

</td></tr><tr><td>

LW Glossary Export Data \(from version 3.1.0\)

</td><td>

\[sn\_lw\_glossary\_export\_data\]

</td></tr><tr><td>

Sn Lw Glossary Import Set \(from version 3.0.0\)

</td><td>

\[sn\_lw\_glossary\_import\_set\]

</td></tr><tr><td>

Glossary Info \(from version 3.0.0\)

</td><td>

\[sn\_lw\_glossary\_info\]

</td></tr><tr><td>

Glossary Translation \(from version 3.0.0\)

</td><td>

\[sn\_lw\_glossary\_translation\]

</td></tr><tr><td>

Progress Tracker

</td><td>

\[sn\_lw\_progress\_tracker\]

</td></tr><tr><td>

Rate Change

</td><td>

\[sn\_lw\_rate\_change\]

</td></tr><tr><td>

Translation Item

</td><td>

\[sn\_lw\_trans\_item\]

</td></tr><tr><td>

Translation Item Language

</td><td>

\[sn\_lw\_trans\_item\_language\]

</td></tr><tr><td>

Translation Provider

</td><td>

\[sn\_lw\_trans\_provider\]

</td></tr><tr><td>

Translation Request

</td><td>

\[sn\_lw\_trans\_request\]

</td></tr><tr><td>

Translation Target

</td><td>

\[sn\_lw\_trans\_target\]

</td></tr><tr><td>

Translation Target Group \(from version 2.0.2\)

</td><td>

\[sn\_lw\_target\_group\]

</td></tr><tr><td>

Translation Target Group Info \(from version 2.0.2\)

</td><td>

\[sn\_lw\_target\_group\_info\]

</td></tr></tbody>
</table>**Parent Topic:**[Localization Workspace reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-workspace/localization-workspace-reference.md)

**Related topics**  


[Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md)

