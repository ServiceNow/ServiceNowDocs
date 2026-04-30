---
title: Greeting feature configuration
description: Understand the configuration of the Greeting feature in the Engagement Messenger to configure the field values.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Engagement Messenger reference, Customer Service Management reference, Customer Service Management]
---

# Greeting feature configuration

Understand the configuration of the Greeting feature in the Engagement Messenger to configure the field values.

<table id="table_opq_wb1_g4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable for unauthenticated users

</td><td>

Option for enabling this feature for guest users who visit the website that hosts the messenger.

</td></tr><tr><td>

Unauthenticated user greeting

</td><td>

Text that is displayed in the header of the messenger home page to greet a guest user. For example, Hello!

</td></tr><tr><td>

Enable for authenticated users

</td><td>

Option for enabling this feature for users who sign in into the website that hosts the messenger.

</td></tr><tr><td>

Authenticated user greeting

</td><td>

Text that is displayed in the header of the messenger home page to greet a user who signs in into the website.

 This field is automatically set to **Hi, &lt;user&gt;!**, where &lt;user&gt; indicates the name of the user who has logged in.

 The other variables that you can use with &lt;user&gt; are the following:

-   &lt;title&gt; which indicates the salutation such as Mr., Ms., or Dr. as per the details in the Users \[sys\_user\] table.
-   &lt;part\_of\_day&gt; which displays the greeting based on the part of the day of the user's region. For example, Good morning, Good afternoon, or Good evening.

</td></tr><tr><td>

Greeting message

</td><td>

Tagline for the user greeting on the header of the messenger home page.

 \[\[URL\|Display Text\]\] indicates format to define URL and display text. For example, `[[https://www.example.com|Example]]`

</td></tr></tbody>
</table>![Greeting feature widget screen with a user greeting, a list of featured articles, and a search bar to search for answers.](../image/em-greeting-feature-widget.png "Greeting feature widget")

