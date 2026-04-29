---
title: Properties installed with Applicant Center
description: The system properties installed with the Applicant Center plugin are required to configure different functionalities in Applicant Center.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Applicant Center, Hiring Experiences, HR Service Delivery, Employee Service Management]
---

# Properties installed with Applicant Center

The system properties installed with the Applicant Center plugin are required to configure different functionalities in Applicant Center.

These properties are available for Applicant Center.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_mwd_kbj_tdc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.service\_portal.resize\_text.ac.enable\_rem\_conversion

</td><td>

Option to set portal configuration.-   Type: true \| false
-   Default value: true
-   Other possible values:

Ignore cache: Selected


</td></tr><tr><td>

sn\_ta\_applicant.company\_career\_link

</td><td>

Helps organization to configure the links on the career page to access on the Applicant Center.-   Type: String
-   Other possible values:
    -   Ignore cache: Selected
    -   Read roles: sn\_ta\_hiring\_core.recruiter
    -   Write roles: admin, sn\_ta\_hiring\_core.admin

</td></tr><tr><td>

sn\_ta\_applicant.company\_name\_for\_applicant

</td><td>

Provides the option to customize it according to the name of the organization.-   Type: String
-   Default value: \[Company Name\]
-   Other possible values:

Ignore cache: Selected


</td></tr><tr><td>

sn\_ta\_applicant.privacy\_link

</td><td>

Option to add a privacy link.-   Type: String
-   Other possible values:
    -   Ignore cache: Selected
    -   Read roles: sn\_ta\_hiring\_core.admin, sn\_ta\_hiring\_core.applicant
    -   Write roles: admin, sn\_ta\_hiring\_core.admin

</td></tr><tr><td>

sn\_ta\_applicant.sn\_ta\_applicant\_onboarding\_state

</td><td>

Property indicates the state when onboarding journey starts.-   Type: String
-   Default value: 50,60
-   Other possible values:

Ignore cache: Selected


</td></tr></tbody>
</table>