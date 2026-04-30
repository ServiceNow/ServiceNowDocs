---
title: Retry policy
description: Automatically retry failed requests when a step encounters an intermittent issue such as a network failure or request rate limit. Set a retry policy to prevent having to manually trigger the step again.Automatically retry failed requests when a step encounters an intermittent issue such as a network failure or request rate limit. Set a retry policy to prevent having to manually trigger the step again.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Create an action in Workflow Studio, Building actions, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Retry policy

Automatically retry failed requests when a step encounters an intermittent issue such as a network failure or request rate limit. Set a retry policy to prevent having to manually trigger the step again.

## Features

Retry policies can be:

-   Created to support connection timeouts or failed requests based on header, status, response body, error, and HTTP method.
-   Applied to all actions that use a given connection alias.
-   Applied directly to an action step.

Use retry policies to define:

-   The conditions that must be met to retry a step.
-   The time interval to wait before retrying a step.
-   The maximum number of retry attempts the step makes before stopping.

Associate a default retry policy to a Connection &amp; Credentials alias and apply the retry policy to all HTTP connections.

**Note:** You can only create retry policies for JDBC, REST, and SOAP steps.

**Parent Topic:**[Create an action in Workflow Studio](../task/create-action.md)

## Create a retry policy

Automatically retry failed requests when a step encounters an intermittent issue such as a network failure or request rate limit. Set a retry policy to prevent having to manually trigger the step again.

### Before you begin

-   Role required: connection\_admin or credential\_admin

### Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Retry Policy** &gt; **Create New**.

2.  On the form, fill in the fields.

<table id="table_lft_drn_jhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the retry policy.

</td></tr><tr><td>

Connection Type

</td><td>

**HTTP**

</td></tr><tr><td>

Condition

</td><td>

Conditions that must be met to trigger the retry policy. Conditions that trigger a retry policy include the **is**, **is not**, **contains**, and **contains not** operators.

</td></tr><tr><td>

Retry Strategy

</td><td>

-   **Exponential Backoff**: Option to exponentially increase the time interval for the subsequent retry attempts. The multiplier is 2.
-   **Fixed Interval**: Option to specify a fixed time interval after which a retry attempt should be made.
-   **Honor "Retry-After" Header**: Option to specify a retry attempt based on the date and time value returned in the Retry After header value of the HTTP request. For more information about the header, see [RFC 7231, section 7.1.3: Retry-After](https://tools.ietf.org/html/rfc7231#section-7.1.3).

**Note:** **Honor "Retry-After" Header** supports only REST and SOAP steps.

</td></tr><tr><td>

Interval \(seconds\)

</td><td>

Time interval in seconds after which a retry attempt should be made. This field applies only to **Exponential Backoff** and **Fixed Interval** retry strategies.**Note:** If **Retry Strategy** is **Exponential Backoff**, the time interval exponentially increases after every retry attempt till the maximum numbers of attempts is reached.

</td></tr><tr><td>

Count

</td><td>

Maximum number of retry attempts. This field applies only to **Exponential Backoff** and **Fixed Interval** retry strategies. If no value is specified, the maximum number of retry attempts is based on the value provided in the **glide.fdih.retry.max\_count** system property. Default value of the **glide.fdih.retry.max\_count** system property is 0. For more information about system properties, see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Max Elapsed Time \(seconds\)

</td><td>

Maximum cumulative time in seconds after which the retry attempts are stopped. This field appears only when **Honor "Retry-After" Header** is selected from **Retry Strategy**.**Note:** If the maximum retry time is specified in the **glide.fdih.retry.max\_time\_in\_seconds** property, the system property value takes precedence over this field value. Also, make sure that the max elapsed time is equal to or greater than the system property value.

</td></tr></tbody>
</table>3.  Create a global system property with the following attributes.

    For more information on how to create a property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US). You can use this system property to specify the maximum time in seconds for a retry policy.

    |Field|Value|
    |-----|-----|
    |Name|`glide.fdih.retry.max_time_in_seconds`|
    |Type|`integer`|
    |Value|Default value: `86400` \(seconds\) Maximum supported time: `604800` \(seconds\)|

4.  Click **Submit**.


### Retry policy with Retry Strategy as Exponential Backoff

![Sample retry policy when Retry Strategy is Exponential Backoff](../images/exponential-backoff.png "Sample retry policy")

In this example, the policy is defined to attempt retry when one of these conditions is met:

-   **HTTP Method is GET and Error is Connection Timeout**
-   **HTTP Method is GET and Status Code is 429**

When the condition is met, retry attempts are made for a maximum number of three times. The time interval between the retry attempts is exponentially increased. The time intervals in this example are 10 seconds, 20 seconds, and 40 seconds.

### What to do next

-   [Create a Connection &amp; Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US), if you do not have the required alias.
-   Assign the retry policy as **Default Retry Policy** to the required Connection &amp; Credential alias.

    **Note:** A default retry policy is provided and is selected as **Default Retry Policy**. If you have created retry policies, you can select the required policy as **Default Retry Policy**.

-   Create an HTTP\(s\) Connection in the Connections related list for the Connection &amp; Credential alias. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).
-   Verify and view the details of the retry attempts by navigating to **System Logs** &gt; **Outbound HTTP Requests**.

