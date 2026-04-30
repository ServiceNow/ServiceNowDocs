---
title: Now Assist in Virtual Agent system properties
description: Use system properties to customize your assistant. Some properties are available on a system properties form, but some lesser-used properties are available only from the System Property \[sys\_properties\] table.
locale: en-US
release: xanadu
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: reference
last_updated: "2025-03-28"
reading_time_minutes: 2
breadcrumb: [Now Assist in Virtual Agent reference, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Now Assist in Virtual Agent system properties

Use system properties to customize your assistant. Some properties are available on a system properties form, but some lesser-used properties are available only from the System Property \[sys\_properties\] table.

<table id="table_fl4_c4w_v2c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_nowassist\_va.enhanced\_chat\_pin\_enabled.&lt;portal-url&gt;

</td><td>

Create a system property to enable pinning a chat window on a portal. In the system property, **&lt;portal-url&gt;** is the URL suffix for the portal application. For example, the system property for enabling a chat window in Employee Center would be **sn\_nowassist\_va.enhanced\_chat\_pin\_enabled.esc**. By default, pinning a chat window is enabled for Service Portal. For all other portals, create the system property. For a list of URL suffixes, navigate to **All** &gt; **Service Portal** &gt; **Portals**.

</td></tr><tr><td>

com.glide.cs.doc\_qna.va\_attachment.max\_attachments

</td><td>

Set the maximum number of attachments that can be attached at one time for the assistant. Default value = 3.

</td></tr><tr><td>

now\_assist\_va\_search\_results\_output\_type.list

</td><td>

Turn off regular results and only have Genius Results shown within Virtual Agent. Use the system property to access the Now Assist Search Results Output Types table. By default, regular results and Genius Results are shown for all channels \(Android device, iOS, Web Client,Now Assist Panel, and Microsoft Teams\). In the Search Results Type column, select **Genius Search Result**.![Now Assist Search Results Output table.](../image/NAinVA-results-output-table.png)

</td></tr><tr><td>

sn\_nowassist\_va.show\_view\_more\_for\_synthesized

</td><td>

Show the **Need more help** button in a standard chat conversation. The **Value** field is empty by default so the button doesn’t appear. To show the **Need more help** button, enter `regular`, `clarification`, or `regular,clarification`.

 -   `regular`: The **Need more help** button appears only for synthesized responses.
-   `clarification`: The **Need more help** button appears only for clarification responses. Clarification responses typically occur when an end user's response is too vague and clarification is needed for a more targeted response.
-   `regular,clarification`: The **Need more help** button appears for both synthesized responses and clarification responses.

</td></tr><tr><td>

sn\_ais\_assist.enable\_knowledge\_graph\_nlq

</td><td>

Enable querying using Knowledge Graph in Now Assist in Virtual Agent. The default value is `true`.

</td></tr><tr><td>

sn\_ais\_assist.kgnlq\_schema\_name

</td><td>

Control the information available to Now Assist in Virtual Agent through Knowledge Graph. The default value is `sn_kg.now_user_graph_nlq`.

</td></tr><tr><td>

sn\_vad\_genai.knowledge\_graph.enabled

</td><td>

Enable Knowledge Graph slot filling for Now Assist in Virtual Agent. The default value is `false`.

</td></tr><tr><td>

sn\_nowassist\_va.enable\_suggested\_actions

</td><td>

Enable suggested actions in Now Assist in Virtual Agent so that users are offered options for what they can do after completing a prior action. Suggested actions is applicable to standard and enhanced chat, mobile, and Microsoft Teams. These are the possible values:False = Suggested actions remain off with no background processes running.

Log only = Feature runs in the background with no suggested actions shown in the UI. The suggested actions are logged in a table that is visible to admins.

True = Shows the suggested actions in Now Assist in Virtual Agent and log only mode. Log only mode logs the actions predicted in a table that is visible to the admin.

</td></tr><tr><td>

sn\_nowassist\_va.synth\_response\_revisit\_position

</td><td>

Change the order of the fallback and revisit options in a conversation. In the **Value** field, enter `BEFORE_FALLBACK` or `AFTER_FALLBACK`, and then select **Update**.

</td></tr></tbody>
</table>View the table showing actions executed and corresponding suggested actions in the instance. The table is visible when the system property is set to `Log only` or `True`. The table location is: **sys\_now\_assist\_va\_suggested\_actions\_result\_log**.

<table id="table_esd_jrb_1fc"><tbody><tr><td>

Executing action name

</td><td>

Executing action description

</td><td>

SA1 name

</td><td>

SA1 description

</td><td>

SA1 model type

</td><td>

SA2 name

</td><td>

SA2 description

</td><td>

SA2 model type

</td></tr></tbody>
</table>