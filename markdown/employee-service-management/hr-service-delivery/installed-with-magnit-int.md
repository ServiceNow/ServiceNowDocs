---
title: Components installed with HR Service Delivery Integration with Magnit
description: Several types of components are installed with activation of the HR Service Delivery Integration with Magnit plugin, including tables, and user roles.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, HR Service Delivery Integration with Magnit, Integrate with third-party systems, HR Service Delivery, Employee Service Management]
---

# Components installed with HR Service Delivery Integration with Magnit

Several types of components are installed with activation of the HR Service Delivery Integration with Magnit plugin, including tables, and user roles.

## Roles installed

<table id="table_lkb_ptz_vvb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Magnit Admin\[sn\_hr\_magnit.admin\]

</td><td>

-   Can pull Magnit contingent workers
-   Can view HR profiles, HR lifecycle case, and HR task created for the contingent worker​
-   Can create Magnit task mapping records

</td><td>

-   sn\_hr\_le.activity\_writer
-   sn\_hr\_integr\_fw.admin
-   sn\_hr\_magnit.reader

</td></tr><tr><td>

Magnit Reader\[sn\_hr\_magnit.reader\]

</td><td>

Can view HR profile, HR lifecycle case, and HR task created for Magnit contingent worker along with Magnit task mapping records​

</td><td>

-   sn\_hr\_integr\_fw.admin
-   sn\_hr\_magnit.reader

</td></tr></tbody>
</table>## Tables installed

<table id="table_pkb_ptz_vvb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Magnit Task Mapping\[sn\_hr\_magnit\_task\_mapping\]

</td><td>

Store the mappings between onboarding items and HR tasks.

</td></tr><tr><td>

User Onboarding Item\[sn\_hr\_magnit\_user\_onboarding\_item\]

</td><td>

Stores the mappings of onboarding items of contingent workers with HR profiles.

</td></tr></tbody>
</table>**Parent Topic:**[Reference for HR Service Delivery Integration with Magnit](reference-magnit.md)

**Related topics**  


[Default entities](default-ent-magnit.md)

