---
title: Create cleanup scripts
description: Use cleanup scripts to automate post-clone steps or to modify data after your clone.Use cleanup scripts to modify data after your clone completes.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-09-30"
reading_time_minutes: 1
breadcrumb: [Configure, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Create cleanup scripts

Use cleanup scripts to automate post-clone steps or to modify data after your clone.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Clone Admin Console** &gt; **Clone Home**.

2.  Select **Definitions** from the secondary navigation.

3.  Select the **Cleanup scripts** tab.

4.  Select **New**.

5.  Enter a name for your script.

6.  Select the order number for your script.

7.  Check **Active** when your script is ready.

8.  Enter your script in the **Script** field, and select **Save**.


## Disable emails

To create a cleanup script to disable emails, do the following.

-   Select **New** on the cleanup scripts tab.
-   Add the name `Disable emails`.
-   Check **Active**.
-   In the script field, add

    ```
    gs.setProperty("glide.email.read.active", false);gs.setProperty("glide.email.smtp.active", false);
    ```

    .

-   Select **Update**.

## Cleanup scripts \(lists and forms\)

Use cleanup scripts to modify data after your clone completes.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Instance Clone** &gt; **Clone Definition** &gt; **Cleanup scripts**.

2.  Select **New**.

3.  Select the order number for your script.

4.  Check **Active** when your script is ready.

5.  Enter your script in the **Script** field, and select **Save**.


