---
title: Sightings searches on user-reported phishing and malware attacks
description: Perform sightings searches on emails or observables to determine how often certain types of attacks, such as phishing attacks or communications with a malicious IP or URL occur in your network. Each occurrence is considered a sighting. Sightings searches for observables must be configured for your log stores or security information and event management \(SIEM\).Search for users who have received phishing emails based on observables such as email subject, sender name, or message ID. You can then contain and eradicate these phishing emails from your organization.Perform sightings searches on observables to find out how many users have visited a malicious or suspicious website within a specific period.Create multiple sightings search configuration records and use them while querying multiple log stores or varying the search parameters.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Manage security threats using the Security Analyst Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Sightings searches on user-reported phishing and malware attacks

Perform sightings searches on emails or observables to determine how often certain types of attacks, such as phishing attacks or communications with a malicious IP or URL occur in your network. Each occurrence is considered a sighting. Sightings searches for observables must be configured for your log stores or security information and event management \(SIEM\).

How to use the sighting search feature to locate phished users, and track phishing and malware observables within the log store on your network.

Watch this three-minute video to learn how to use the sighting search feature to locate phished users, and track phishing and malware observables within the log store on your network.

The following terms are used to describe user-reported phishing attacks:

-   Phished user: A user who has received a phishing email.
-   Victim user: A user who has interacted with the phishing URL, typically by clicking a link in the phishing email. This action potentially exposes credentials to the attacker.

As you start analyzing a phishing incident, you can [Perform an email sightings search](sighting-searches-on-phishing-attacks.md#) or [Perform an observable sightings search](sighting-searches-on-phishing-attacks.md#) to identify other users in your organization who are impacted by the same phishing attack. Search your log stores to identify phished and victim users. After you have identified the list of affected users, create child security incidents to perform comprehensive incident response procedures using the tools available in Security Incident Response.

**Note:** You can also use the following approach to perform a sightings search:

-   Navigate to **Security Incidents** &gt; **Show All Incidents** and click on a security incident.
-   Click **Show IoC** under Related Links. A list of observables is displayed.
-   Select an observable from the list and from the **Actions** list, select either of the following options:
    -   Run Web Traffic Sightings Search
    -   Run Email Traffic Sightings Search
-   Specify the time frame and click **Search** to perform a sightings search.

## Saved sighting search configurations

Configure sighting searches and create saved configurations for SIEMs or other log stores for instances of observables to determine the presence of malicious observables in your environment.

**Note:** Saved Searches and Inplace queries are supported for Splunk Integration only.

**Related topics**  


[Create sightings search configuration records](../task/sightings-search-configurations.md)

## Perform an email sightings search for user-reported phishing attacks

Search for users who have received phishing emails based on observables such as email subject, sender name, or message ID. You can then contain and eradicate these phishing emails from your organization.

### Before you begin

Role required: sn\_si.analyst

### About this task

Search the Splunk email traffic logs to gather the list of recipients of a suspicious email. The search can be performed using the email sender, email message ID, or the email subject associated in a security incident as the criteria.

**Note:**

-   This implementation of sightings search for email-based observables has been tested only with the Splunk Enterprise log store.
-   The Splunk log events must be Common Information Model \(CIM\) compliant for the sightings search query to return accurate results.

### Procedure

1.  To see the security incidents assigned to your team, navigate to **Security Incident** &gt; **Incidents \(New UI\)**.

2.  From the **Security Incidents** list, select one of the filters, such as all **open incidents**, **all incidents assigned to you**, or **all incidents**.

    To view security incidents of a particular type, such as critical incidents or phishing emails, click one of the **Quick Filters**.

    ![Security incidents](../image/cj-sir-si-list.png)

3.  Click the security incident that you want to analyze.

    The Overview tab provides an overview of the security incident including a list of observables, affected users, and similar security incidents.

    ![Overview tab](../image/cj-sir-si-details.png)

4.  Click the **Explore** tab.

5.  Under **Incident Data**, navigate to **Investigation** &gt; **Search Email &amp; Observables**.

    ![Email search](../image/cj-sir-si-email-search.png)

6.  Expand the Search Criteria section.

7.  Select **Email Search** as the type of search that you want to run, and specify the rest of the search criteria.

<table id="table_lnw_lln_dhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integrations

</td><td>

Integrations type. Select **Log Store** from the list.**Note:** This feature is supported only with the Splunk log store.

</td></tr><tr><td>

From

</td><td>

Full email address of the sender \(for example, jane.doe@example.com\).

</td></tr><tr><td>

Message ID

</td><td>

Email message ID from the log store.

</td></tr><tr><td>

Subject

</td><td>

Subject for the phishing email.

</td></tr><tr><td>

Search Window

</td><td>

Time window for the search \(for example, the last 24 hours\).

</td></tr></tbody>
</table>8.  From the **Select Action** list, select **Search** and then click **Run**.

    The Splunk log store is searched using the criteria that you enter, and the users targeted by the phishing attack are shown on the **Email Search Results** tab. The total number of phishing emails and the details of each email, including the email date received, recipient, and message ID, are displayed.

9.  To view the list of users who received the phishing email, click the **&gt;** symbol in the Search Date column.

    ![Email search results](../image/cj-sir-si-email-results.png)

10. To view a list of users who received the email, navigate to **Users** &gt; **Affected Users**.

    The Phished User column identifies the email recipients.

    **Note:** The Affected Users page shows only the user records that are present on the ServiceNow instance.

11. To further investigate the users who are targets of the phishing attack, follow these steps:

    1.  Select the check boxes next to the user names.

    2.  From the list, select **Create Child Security Incident**, and click **Run**.

    A message is displayed to show that a child security incident has been created. To view the child security incidents associated with a parent incident, click the **Explore** tab and navigate to **Incidents** &gt; **Child Security Incidents**.


### Result

The list of phished users is displayed.

## Perform an observable sightings search for user-reported phishing and malware attacks

Perform sightings searches on observables to find out how many users have visited a malicious or suspicious website within a specific period.

### Before you begin

Role required: sn\_si.analyst

### About this task

You can perform a network traffic search on observables such as the URL, destination host, or the destination IP address associated with a security incident.

**Note:**

-   This implementation of sightings search for observables has been tested only with the Splunk Enterprise log store.
-   The Splunk log events must be Common Information Model \(CIM\) compliant for the sightings search query to return accurate results.

### Procedure

1.  To see the security incidents that are assigned to your team, navigate to **Security Incident** &gt; **Incidents \(New UI\)**.

2.  From the **Security Incidents** list, select a different filter, such as all **Incidents Assigned to Me**, **All Open Incidents**, or **All Incidents**.

    To view security incidents of a particular type, such as critical incidents or phishing emails, click one of the **Quick Filters**.

    ![Security incidents](../image/cj-sir-si-list.png)

3.  Click the security incident that you want to analyze.

    You can see an overview of the security incident including a list of observables, affected users, and similar security incidents.

    ![Overview tab](../image/cj-sir-si-details.png)

    In the Observables section, notice that the Observable column shows the email address, subject, and URL. Notice also that the Finding column shows that the URL was automatically scanned when the phishing email was submitted and determined to be a known malicious URL. The Incident Count column shows the other incidents that share the same observable. These artifacts indicate that you are likely ready to move on to containment procedures for this phishing attack, including determining how many users in the organization have been affected.

    ![Observables](../image/cj-sir-si-obs-details.png)

4.  Navigate to **Explore** &gt; **Investigation** &gt; **Search Email &amp; Observables**.

5.  Expand the Search Criteria section and click **Observable Search**.

    ![Observable search](../image/cj-sir-si-search-emobs.png)

6.  Enter the observable that you are searching for, and a time window for the search \(for example, Last 24 Hours\).

7.  From the **Select Action** list, select **Search**.

    The Splunk log store is searched using the criteria that you entered and the key users targeted by the malicious attack are shown on the **Observable Search Results** tab.![Observable search results](../image/cj-sir-si-observable_result.png)

8.  To view the users who received the email, navigate to **Users** &gt; **Affected Users**.

    The Phished User column identifies the recipients of the phishing email and the User Interaction column identifies users who clicked a phishing URL or interacted with a suspicious email address. The User Interaction column is set to true or false, depending on whether the user clicked the malicious link or IP.

    **Note:** The Affected Users page shows only the user records that are present on the ServiceNow instance.

9.  To further investigate the users who clicked the phishing email and potentially compromised their credentials:

    1.  In both the Phished User and User Interaction columns, select the check boxes next to the user names that show **true**.

    2.  Click **Create Child Security Incident** and then click **Run**.

        A message is displayed to show that a child security incident has been created. To view the child security incidents associated with a parent incident, click the **Explore** tab and navigate to **Incidents** &gt; **Child Security Incidents**.


### Result

The list of phished users is displayed.

## Create sightings search configuration records

Create multiple sightings search configuration records and use them while querying multiple log stores or varying the search parameters.

### Before you begin

Role required: sn\_si.admin

-   The CIM add-on must be installed on the Splunk instance.
-   Saved Searches and Inplace queries are supported for Splunk Integration only.

### About this task

You can also create sightings search configuration records to invoke [saved searches](https://docs.splunk.com/Splexicon:Savedsearch) on the Splunk enterprise log store.

**Note:** The search configuration queries rely on Splunk log data to be Splunk Common Information Model \(CIM\) compliant.

With saved search configurations, you can:

-   Create custom searches that combine multiple event records.
-   Design-efficient and effective searches.
-   Use parametrized inputs in the Splunk saved search.

The base system includes the sample configurations.

The saved search and Inplace configuration queries are example queries and can be substituted with appropriate parameters for your environment. Create additional saved search configurations as required. When you define a saved search configuration, the name and the parameters in the search query must match the saved configuration defined on your Splunk instance. If the name and parameters are not the same, you may not see accurate results when you perform a sightings search.

**Note:** On your Splunk instance, navigate to the Searches, Reports, and Alerts page and locate your saved search query. Select the **Permissions** link to navigate to the Permissions page. Select the **All Apps** radio button and enable the **Read Permission** option for **Everyone**. This will change the Sharing column value from Private to App for your saved search query. If this is not set, saved search query may not return any results.

To verify if the saved search configuration matches the configuration defined on your Splunk instance:

1.  Navigate to **Settings** &gt; **Searches, Reports, and Alerts**.
2.  Change **App Context** to **All**.

    A list of search reports is displayed.

3.  Confirm that the saved search query is present in the list.

For example, the Sightings Search Configuration form contains the email address and email sender as search parameters:

![Saved configuration](../image/cj-sir-si-saved-config.png "Sightings Search Configuration form")

In your Splunk instance, define the saved search with the same name, Default Saved Search - Emails, and the same search parameters for the email address and email subject. If the name and search parameters are not the same, sightings search does not generate accurate result.

### Procedure

1.  Navigate to **Security Operations** &gt; **Integrations** &gt; **Sightings Search Configuration** and create a new record \(see table for field descriptions\).

    |Field|Description|
    |-----|-----------|
    |Name|Name of the configuration.|
    |Is saved search|Saved search configuration is created if you select this option.|
    |Sightings search source|The source for the sightings search. Select the Splunk log store as the source.|
    |Active|Option for the saved search status. Only active search configurations can be used to perform a sightings search.|
    |Observable type|Observable type can be any observable type such as IP, hash value, URL, domain name, and so on.|
    |Maximum observables per search|Maximum number of observables to be returned from the search.|
    |Search|The default search string is`$(observable)`, but you can define your own search query by specifying parameters that are supported by the Splunk log store.|

2.  Select **Submit**.


### Result

You have created a sightings search configuration record.

### What to do next

After defining the search query, select **Generate Sightings Search Test Query**, and specify a list of observable values to generate a test query based on this saved search configuration.

