---
title: Define a Cloud REST Query for cloud computing devices
description: As part of creating or modifying a discovery pattern, you can use the Cloud REST Query operation to extract information from configuration items \(CIs\) of the PaaS \(Platform as a Service\) type, such as Microsoft Azure or Amazon Web Services.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Amazon DynamoDB, AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Define a Cloud REST Query for cloud computing devices

As part of creating or modifying a discovery pattern, you can use the **Cloud REST Query** operation to extract information from configuration items \(CIs\) of the PaaS \(Platform as a Service\) type, such as Microsoft Azure or Amazon Web Services.

## Before you begin

-   Verify that the operating system of the CIs for which you want to use the Cloud REST Query operation extends the Logical Data Center OS type \[cmdb\_ci\_logical\_datacenter\]:
    1.  Navigate to **Pattern Designer** &gt; **Discovery Patterns**.
    2.  Double-click the relevant pattern to open it in the Pattern Designer.
    3.  Click the **Basic** tab.
    4.  Note the operating system for this CI.
    5.  Navigate to **System Definition** &gt; **Tables**.
    6.  Set the search field to **Label** and enter the name of the operating system as stated on the **Basic** tab of the pattern.
    7.  Find the operating system in the list and verify that Logical Datacenter appears in the **Extends table** column.
-   Navigate to the relevant pattern step:

    1.  On the pattern form, select the relevant identification section for Discovery.

        Alternatively, select the relevant identification or connection section for Service Mapping.

    2.  Select the relevant pattern step or click the **Add a step above** icon to add a step.

Basic knowledge of programming is desirable.

Role required: pd\_admin

## About this task

Deploy the Cloud REST Query operation in patterns used for discovery of PaaS CIs. This Java-script based custom operation is available only after downloading patterns version 1.0.24 or later from ServiceNow Store. Use this operation instead of the Cloud REST Call operation available in the base system.

Refer to the official API-related documentation provided by manufacturers to obtain the query syntax for the device you want to query using the Cloud REST Query operation. For example:

-   [http://docs.aws.amazon.com/AWSEC2/latest/APIReference/Welcome.html](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/Welcome.html)
-   [https://docs.microsoft.com/en-us/rest/api/apimanagement/](https://docs.microsoft.com/en-us/rest/api/apimanagement/)

## Procedure

1.  Select **Cloud REST Query** from the **Operation** list.

2.  Define query parameters as necessary:

    **Note:** If you customized this operation, the query parameters may be different.

<table id="table_d3y_qhuk_sy"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

URL

</td><td>

Specify the URL as described in the official Microsoft Azure or Amazon Web Services documentation. You can use variables. You can also enter a value from the specific field in a tabular variable.

</td></tr><tr><td>

Method

</td><td>

Enter the method value as a string using all capital letters, for example "GET". Supported methods are:

 -   GET
-   POST
-   PUT
 Refer to the relevant API guide for information. If the API documentation does not specifically mention the HTTP query method, use the GET method.

</td></tr><tr><td>

Body

</td><td>

\(Optional\) Enter a request body as a string. If the string contains quotation marks, use the backslash mark in front of the quotation marks to indicate that the string does not end at the quotation marks.

</td></tr><tr><td>

Headers

</td><td>

\(Optional\) If the relevant API documentation states that HTTP headers must be sent, enter these headers in the following format: Header\_name1:header\_value1,header\_name2:header\_value2

For example, `Content-Type:xml`.

</td></tr><tr><td>

Formatted

</td><td>

Formatted JSON or not

</td></tr></tbody>
</table>3.  To save the command output in its entirety as a variable, select `NONE` from the **Define Parsing** list and define the variable.

4.  Select the parsing strategy from the **Define Parsing** list.

5.  If working in the Debug Mode, define the parsing criteria as follows:

    1.  Click **Run Operation** to see the result in the **Output** pane.

    2.  In the **Output** pane, mark text or symbols that you want a variable to contain.

    3.  In the variable name box, enter the name for the new variable, for example 'process\_name'.

        ![Defining a variable name for the string marked in the Output pane](../image/PatDefVariableFromOutput.png)

    4.  Press **Enter**.

        The new variable is added in the **Variables** pane.

6.  If you are not working in Debug Mode, define the parsing criteria as follows:

    1.  In the Variables pane, click **Add Variable** and enter the name for the new variable.

    2.  Click the **Advanced** icon.

        ![Displaying the Advanced Variables pane](../image/PatDefAdvanceVariableArea.png)

    3.  Click **Add Column Label**.

    4.  Enter the parsing query.

    5.  Enter a value for the delimiter.

    6.  Enter a value for the position.

7.  Select **Terminate** to stop discovery if no results are found.


## Example

|This operation is used in|This item|
|-------------------------|---------|
|Hierarchy|Application|
|CI Type|Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\]|
|Pattern|Amazon AWS S3|
|Section|Identification of AWS S3|
|Step number and Name|3. List buckets|

![The Cloud REST Query operation](../image/PatDefCloudRESTQueryExample.png)

Use the Cloud REST Query operation to extract information about AWS buckets, their names and creation dates.

**Parent Topic:**[AWS discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md)

