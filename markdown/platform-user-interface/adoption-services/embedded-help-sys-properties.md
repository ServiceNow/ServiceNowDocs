---
title: Embedded Help system properties
description: Embedded help is active by default on your instance. The administrator can change system properties to modify how the instance interacts with embedded help.
locale: en-US
release: zurich
product: Adoption Services
classification: adoption-services
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Embedded Help reference, Embedded Help, In-product help, Adoption services, Configure user experiences]
---

# Embedded Help system properties

Embedded help is active by default on your instance. The administrator can change system properties to modify how the instance interacts with embedded help.

The administrator navigates to **Embedded Help** &gt; **Properties** to change these properties.

<table id="table_uvm_jn2_5y"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.glide.embedded\_help.auto\_close

</td><td>

Auto-closes the help pane when the user clicks **Start a Tour** or **Back To Guided Setup**.-   Type: true \| false
-   Default value: true

</td></tr><tr><td>

com.glide.embedded\_help.cdn\_timeout

</td><td>

Duration in milliseconds at which a content pull from the Content Delivery Network \(CDN\) is timed out.-   Type: integer
-   Default value: 2000

</td></tr><tr><td>

com.glide.embedded\_help.enabled

</td><td>

Enables the embedded help plugin for activation.-   Type: true \| false
-   Default value: true

</td></tr><tr><td>

com.glide.embedded\_help.enable\_video

</td><td>

Enables users to see embedded videos in help content. The administrator can embed video and a description, but if this property is **false**, the video and description are hidden in the help pane.-   Type: true \| false
-   Default value: true

 **Note:** When you embed video content, enclose the video embed code and description inside a `<div class="video">` tag. If you disable the property, the content inside the `<div class="video">` tag is hidden when the content is displayed.

</td></tr><tr><td>

com.glide.embedded\_help.sync

</td><td>

Enables the instance to look in the CDN for updated content when a user accesses a UI page. The instance checks the **Last sync** date in the topic against the specified frequency to determine whether to look in the CDN for updated content. -   Type: true \| false
-   Default value: true

 If the property is disabled \(false\), the embedded help content is never synced with CDN topic updates.

</td></tr><tr><td>

com.glide.embedded\_help.sync\_frequency

</td><td>

Specifies how many days must pass from the **Last sync** date in the topic for the embedded help process to look for updated content in the CDN.-   Type: integer
-   Default value: 15

</td></tr><tr><td>

com.glide.embedded\_help.sync\_self\_hosted

</td><td>

Specifies whether a self-hosted instance syncs content with the CDN.-   Type: true \| false
-   Default value: false

</td></tr><tr><td>

com.glide.embedded\_help.url

</td><td>

Lists the location from where embedded help is dynamically retrieved.-   Type: string
-   Default value: varies

</td></tr><tr><td>

com.glide.embedded\_help.version

</td><td>

Specifies the instance version for which help is displayed.-   Type: string
-   Default value: Jakarta

 If blank, displays the help for the version the instance is currently running.

</td></tr></tbody>
</table>The following system property is available by navigating to the \[sys\_properties\] table.

<table id="table_fm4_lqr_t1b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.glide.embedded\_help.guided\_setup.persist\_actions

</td><td>

Enables Guided Setup actions in the embedded help panel that are based on states to display on all pages. An example is the **Mark as Complete** action. The default behavior \(false\) is to only show actions on the initial Guided Setup page.-   Type: true \| false
-   Default value: false

</td></tr></tbody>
</table>**Parent Topic:**[Embedded Help reference](../concept/embedded-help-reference.md)

