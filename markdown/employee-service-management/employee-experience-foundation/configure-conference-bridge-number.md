---
title: Configure the conference bridge numbers to join calls via phone
description: Configure the conference bridge number to allow the participants to collaborate to resolve the incidents via the conference bridge number.Reserve a conference bridge number to host the conference calls to work towards the resolution of incidents via conference bridge number.Configure the conference bridge number to be used for collaborating with the participants to resolve the major incidents.Make the conference bridge number available for the participants to join a conference call via the bridge number.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/configure-conference-bridge-number.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure Notify connector, Microsoft Teams integration for Agent Experience, Configure, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Configure the conference bridge numbers to join calls via phone

Configure the conference bridge number to allow the participants to collaborate to resolve the incidents via the conference bridge number.

**Note:** These are additional configuration, which are optional and can be used as required.

**Parent Topic:**[Configure Notify connector for Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/config-notify-ms-teams.md)

## Reserve a conference bridge number

Reserve a conference bridge number to host the conference calls to work towards the resolution of incidents via conference bridge number.

### Before you begin

Role required: Microsoft Teams admin

### Procedure

1.  Log in to Microsoft Teams admin center.

2.  Navigate to **Voice** &gt; **Phone number**.

    \[Omitted image "path-phone-numbers.png"\] Alt text: Path for phone numbers

3.  Click **Add**.

4.  On the form, fill the fields.

    1.  Add a name for your order: Provide a name for the audio service.

    2.  Country or region: Option to select a country.

    3.  Number type: Option to select the number type.

        \[Omitted image "add-phone-number-2.png"\] Alt text: Add the phne number screen

    4.  Quantity: Option to choose the number of the conference number.

    5.  Search for new numbers: Option to choose the conference numbers based on city name or by area code.

        \[Omitted image "add-phone-number-3.png"\] Alt text: Options to fill the order form

    6.  Click **Next**.

        The reserved number is displayed.

    7.  Click **Place order**.

        Upon placing the order, the conference numbers appear in the phone numbers for the tenant.

    8.  Click **Finish**.

        \[Omitted image "add-phone-number-4.png"\] Alt text: Order for conference number placed successfully

        The reserved numbers appear under Phone numbers section as depicted.

        \[Omitted image "reserved-phone-numbers.png"\] Alt text: Reserved phone numbers


## Configure conference bridge number for meetings

Configure the conference bridge number to be used for collaborating with the participants to resolve the major incidents.

### Before you begin

Role required: Microsoft Teams admin

### Procedure

1.  Log in to Microsoft Teams admin center.

2.  Navigate to **Meetings** &gt; **Conference bridges**.

3.  Click **Add**, and then select the conference bridge type.

    \[Omitted image "add-conference-bridge.png"\] Alt text: Add conference bridge type

4.  Select the conference bridge type.

    \[Omitted image "conference-bridge-type.png"\] Alt text: Conference bridge type

5.  Select the number from the drop-down option.

    This is the number that is reserved for your tenant for conference calls.

    \[Omitted image "add-number.png"\] Alt text: Add conference bridge number

6.  Click **Apply**.

    The selected number is added to the list of conference bridge numbers.


## Setup the conference bridge for the users

Make the conference bridge number available for the participants to join a conference call via the bridge number.

### Before you begin

Role required: admin

### Procedure

1.  Log in to Microsoft Teams admin center.

2.  Navigate to **Users** &gt; **Manage users**.

3.  Click **Service User**.

    \[Omitted image "manage-users.png"\] Alt text: Manage users

4.  Edit the Audio Conference details by clicking the **Edit** button.

    \[Omitted image "edit-audio-conference.png"\] Alt text: Edit audio conference

5.  Select the toll number.

    \[Omitted image "audio-conference-settings.png"\] Alt text: Audio conference settings

6.  Click **Apply**.


