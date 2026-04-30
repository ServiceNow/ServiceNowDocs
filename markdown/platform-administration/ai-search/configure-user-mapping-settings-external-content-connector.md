---
title: Configure user permission settings for an external content connector
description: Override the default field mappings for an external content connector's user permission crawls. Specify the fields that uniquely identify user security principals in your source system and users in your ServiceNow AI Platform instance. Optionally execute a custom script to transform security principal IDs before they're compared with the IDs of users in your instance.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-11-12"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Configure user permission settings for an external content connector

Override the default field mappings for an external content connector's user permission crawls. Specify the fields that uniquely identify user security principals in your source system and users in your ServiceNow AI Platform® instance. Optionally execute a custom script to transform security principal IDs before they're compared with the IDs of users in your instance.

## Before you begin

Role required: sn\_ext\_conn.xcc\_admin or admin

## About this task

User permission crawls for external content connectors retrieve user security principals from your source system and map them to users in your ServiceNow AI Platform instance. A user security principal from the source system should map to no more than one user in your instance.

Each external content connector specifies a predefined source system field that the connector uses as the unique identifier for user security principals in the source system. As an example, a connector might specify a username or email address field as the principal identifier for its source system. All connectors default to using the email field from the Users \[sys\_user\] table as the unique identifier for users in your ServiceNow AI Platform instance.

If you need to specify a different field as the identifier for source system principals or instance users, you can override the default field selections for the external content connector. You can optionally execute a custom script to transform source field values to make them match destination field values for users in your ServiceNow AI Platform instance.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **User permission settings**.

4.  In the Map from section, select a source system field with values that uniquely identify your user security principals.

    As an example, if your source system security principals are uniquely identified by their email addresses, you might select the source system's **email** field.

5.  Select the **Custom script** option and enter a custom script function in the code editor.

    You only need to perform this step if you want to transform source system field values before they're compared with destination field values in your ServiceNow AI Platform instance. As an example, if your source system identifies user security principals with user IDs like `beth.anglin` but your ServiceNow AI Platform instance users have email-based usernames like `beth.anglin@example.com`, you might use the script to append the @ symbol and your domain name to each user security principal ID so that it correctly matches a ServiceNow AI Platform username.

    **Warning:** The system executes your custom script for each user security principal retrieved by the external content connector's user permission crawl. A long-running script can affect performance for the user mapping crawl. Keep your scripts as simple as possible.

    The custom script must include a function that transforms the incoming field value for a user from the connector's source system to an output value that will be used to match a user in the ServiceNow AI Platform's User \[sys\_user\] table. Continuing the previous example, you might define this custom script to transform bare usernames into user email addresses in your domain:

    ```javascript
    /**
    * Maps the incoming field value of the user from the source system to an output value that will be used to match the user in the ServiceNow platform.
    * Supported return types are "string" and "number".
    */
    
    var mapSourceUser = function(sourceUserValue) {
      // Append @ symbol and domain name to source user ID
      //   Source field value format = user
      //   Destination field value format = user@example.com
    
      return sourceUserValue + "@example.com";
    }
    
    mapSourceUser(sourceUserValue);
    ```

    The default script includes several code examples that you can use as a basis for your own custom script. To revert the code in the code editor to the default script, select **Reset to default script** and then **Reset**.

    **Important:** Don't change the `mapSourceUser` function declaration at the start of the script or the subsequent call to that function. You should only edit the function body inside the curly braces to implement your desired custom field value transformation.

6.  In the Map to section, select the ServiceNow AI Platform field to use as the unique identifier for users in your instance.

    The default identifier field is the email field from the User \[sys\_user\] table.

7.  Test your user permission settings by selecting **Test** and then performing the following steps.

    1.  When prompted, enter a sample value for the external content connector's source field.

        As an example, if your source system uses email addresses to identify user security principals, you might enter `abel.tuter@example.com`.

    2.  Select **Run test** and wait for the test to complete.

        The system uses your user permission settings to look for a ServiceNow AI Platform instance user that matches the specified user security principal from the source system. You can interrupt this process and cancel the test by selecting **Cancel** or closing the modal window.

    3.  View the test results.

        -   **Match**

            This status indicates that the test successfully matched a single ServiceNow AI Platform instance user.

        -   **No match**

            This status indicates that the test did not match any ServiceNow AI Platform instance user.

        -   **Inconclusive**

            This status indicates that the test matched multiple ServiceNow AI Platform instance users, rather than a single unique user as desired.

    4.  Perform the appropriate step depending on the test's result.

    -   To return to the user permission settings editor, select **Close**.
    -   To return to the sample value entry field so you can repeat the test with different input, select **New test**. You can edit your previous input to see how different values behave.
8.  When you're done testing, select **Save**.


## Result

The external content connector is updated with your modified user permission settings.

If you configured a custom script, any script errors encountered during user permission crawls are recorded in the Alerts section of the connector's crawl details page. To learn about accessing the crawl details page from an external content connector's crawl history entry, see [Review crawl history for an external content connector](review-crawl-ext-cont-connector.md).

## What to do next

To retrieve updated user permissions from your source system using your modified settings, create and run a user permission crawl for the external content connector that you edited. To learn about creating and running user permission crawls, see [Create a user permission crawl for an external content connector](create-user-mapping-crawl-external-content-connector.md).

**Parent Topic:**[Configuring External Content Connectors](../concept/configuring-ext-cont-connectors.md)

