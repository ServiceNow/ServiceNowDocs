---
title: Run trust profile setup in AEMC
description: After completing ReleaseOps guided setup in AEMC, run trust profile setup to complete the configuration process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/app-engine-management-center/run-trust-profile-setup-aemc.html
release: australia
product: App Engine Management Center
classification: app-engine-management-center
topic_type: task
last_updated: "2026-06-08"
reading_time_minutes: 1
breadcrumb: [Configure ReleaseOps, Configure, App Engine Management Center, Governing app development, Building applications]
---

# Run trust profile setup in AEMC

After completing ReleaseOps guided setup in AEMC, run trust profile setup to complete the configuration process.

## Before you begin

Role required: admin

After

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **Administration** &gt; **App Engine Management Center**.

2.  In the banner, select **Run Setup**.

    \[Omitted image "releaseops-trust-profile-setup-banner.png"\] Alt text: App Engine Management Center \(AEMC\) overview page displaying a warning banner that trust profile configuration is invalid and a link to Run Setup.

3.  Verify that the trust profiles are set up.

    1.  Navigate to **All** &gt; **Multi-Instance Management** &gt; **Application Trust Profiles**.

    2.  From the list, select **Trust Profile for App Engine Management Center**.

    3.  Verify that the Active Trust Profile Items list contains each instance in your ReleaseOps pipeline.

        \[Omitted image "multi-instance-management-trust-profiles.png"\] Alt text: Application Trust Profiles form showing two active trust profile items for the App Engine Management Center \(AEMC\) application.


