---
title: Tutorial part 4: Restrict data and collaborate with other developers
description: Learn how to restrict data usage with business rules and also how to add collaborators to your application.Restrict data access in your application by adding business rules with Now Assist for Code generation.Learn how to add collaborators to your app in ServiceNow Studio.
locale: en-US
release: yokohama
product: ServiceNow Studio
classification: servicenow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ServiceNow Studio tutorial, Exploring ServiceNow Studio, Building applications with ServiceNow Studio, Developing your application, Building applications]
---

# Tutorial part 4: Restrict data and collaborate with other developers

Learn how to restrict data usage with business rules and also how to add collaborators to your application.

**Parent Topic:**[ServiceNow Studio tutorial](lab-sns-lab-guide.md)

## Restrict data using business rules and code generation

Restrict data access in your application by adding business rules with Now Assist for Code generation.

### Before you begin

Role required: admin or delegated\_developer

### Procedure

1.  Navigate to the We Volunteer app dashboard, and select **Create**.

2.  Select **Create** &gt; **File**.

3.  In the Application field, enter `Global`.

4.  From the Server Development category, select **Business rule**.

5.  Select **Continue**.

6.  Enter the following data in the new business rule file:

    -   Name: Restrict Visibility
    -   Table: Location \[cmn\_location\]
    -   Advanced: true \(select the checkbox\)
    -   Query: true \(select the checkbox\)
7.  On the Advanced tab, click into the third line in the script editor.

8.  Open the Now Assist code generator by pressing **Command + Enter** \(on Mac\) or **Ctrl + Enter** \(on Windows\).

9.  Enter this text in the prompt: `check if logged in user is having x_snc_wevolunteer.user role, if yes then allow this user to show only those records from current table where type field value is event`.

10. Select the submit icon \(![submit icon](../image/sn-studio-na-submit-icon.png)\) and wait a few moments for Now Assist to generate a code snippet.

11. Select **Accept**.

12. Select **Submit**.


## Collaborate with other developers

Learn how to add collaborators to your app in ServiceNow Studio.

### Before you begin

Role required: admin or delegated\_developer

### Procedure

1.  Navigate to the We Volunteer app dashboard, and select the more options icon \(![more options icon](../image/sn-studio-more-options-icon.png)\).

2.  Select **Collaborators**.

3.  Select **Invite people by name or group**.

4.  Enter `Eva Wickson`.

5.  Select **Send**.

6.  Log out of your instance, and log back in to the ServiceNow AI Platform impersonating Eva Wickson.

7.  If you haven't made ServiceNow Studio a favorite in this instance, navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**, and select the star next to the module to favorite it.

8.  Select **ServiceNow Studio** to open it.

9.  On the Deployment tab, select **Applications**.

10. Sort the **Updated** column in descending order, and open the **We Volunteer** app.


