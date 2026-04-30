---
title: Configure a custom authentication algorithm
description: Generate the custom data needed to authenticate to a web service by running script.
locale: en-US
release: yokohama
product: Connections and Credentials
classification: connections-and-credentials
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Authentication Algorithms, Connections and Credentials, Access Management]
---

# Configure a custom authentication algorithm

Generate the custom data needed to authenticate to a web service by running script.

## Before you begin

-   JavaScript knowledge
-   REST knowledge
-   Target web service API knowledge
-   Connection, credential, and alias knowledge
-   Role required: Developer

## About this task

Use a connection and credential alias and custom authentication based algorithm for authentication.

## Procedure

1.  Navigate to **All** &gt; **Credentials &amp; Connections** &gt; **Authentication Algorithms**, and click **New**.

2.  On the form, fill in the fields.

    The database selection in the **Format** field determines which fields are available.

<table id="table_dls_tpv_sx"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of this algorithm.

</td></tr><tr><td>

Algorithm

</td><td>

Outbound request type. Select **Custom Authentication**.

</td></tr><tr><td>

Description

</td><td>

Description of what your algorithm does.

</td></tr><tr><td>

Application

</td><td>

Scope that your application runs in.

</td></tr><tr><td>

Instance Authentication Script

</td><td>

Script that you select from the Script Includes table. The scripts available are as follows:-   RequestAuthAWSV4Signer
-   RequestAuthInternal
-   RequestAuthSampleCustomSigner
-   RequestAuthTwitterSigner
 **Note:**

-   To know more about the script click the information icon next to the field. The details of the script such as Name, API Name, Application, Accessible from, Script, and so on is displayed.
-   In case of custom authentication with Twitter, you can choose **RequestAuthTwitterSigner**, since it uses an OAuth 1.0a method of authentication. This requires informations such as **API key and secret** and **Access token and secret** that can be used to create signatures to pass in an authorization header. For more information, see [Authentication in Twitter](https://developer.twitter.com/en/docs/authentication/oauth-1-0a).


</td></tr><tr><td>

MID Authentication Script

</td><td>

Script that you select from the MID Server Script Includes \[Discovery view\] table. The scripts available are as follows:-   RequestAuthAWSV4Signer
-   RequestAuthInternal
-   RequestAuthSampleCustomSigner
-   RequestAuthTwitterSigner


</td></tr></tbody>
</table>    ![Twitter authentication algorithm](../image/custom-authentication-algorithm.png)

    Based on the selected scripts and authentication algorithm, the configured credentials is sent as outbound request from ServiceNow to the provider.

3.  Click **Update**.

4.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

5.  Click **New**.

6.  Create Twitter Credentials with Authentication Algorithm.

    In this case **TwitterAuthAlgo**.

7.  Specify the fields:

    -   Name
    -   Active
    -   Access token
    -   Access token secret
    -   Consumer key
    -   Consumer secret
    -   Credential alias
    -   Authentication Algorithm
    ![Twitter Credentials](../image/twitter-algorithm.png)

8.  Click **Update**.


## REST step with Twitter

In case of Twitter, you must ensure the following spokes or credentials are available:

-   Access token
-   Access token secret
-   Consumer key
-   Consumer secret
-   Authentication Algorithm

Action: TwitterAuthAlgo.

Input REST step with Twitter as follows:

-   **Credentials Alias**: The alias that is created for Twitter.
-   **Base URL**: Base URL details from Twitter.
-   **HTTPS Method**: In this case it is POST method. Posting a tweet.
-   **Query Parameters**: **Action** as **tweet**.

![Post Tweet](../image/twitter-post.png)

You can test the action. The tweet is posted on the Twitter page.

