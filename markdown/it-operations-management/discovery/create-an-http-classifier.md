---
title: Create an HTTP classification
description: An HTTP classifier enables the horizontal discovery process to find devices via the HTTP protocol.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Discovery classifiers, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Create an HTTP classification

An HTTP classifier enables the horizontal discovery process to find devices via the HTTP protocol.

## Before you begin

Role required: discovery\_admin

## About this task

If you want to classify devices via HTTP/REST, you can create additional HTTP classifications, rather than by another protocol. Use HTTP classification for device discovery only, not for application discovery.

**Important:** Starting in YP7, the HTTP Classify probe no longer attempts credentials over the HTTP protocol by default. To override this behavior, you can enable **mid.http\_classy.allow\_credentials\_over\_http**. However, enabling this setting can expose credentials to man-in-the-middle \(MitM\) attacks. Therefore, it’s strongly recommended to keep this property set to **false** and use HTTPS whenever possible.

By default, the [F5 HTTP classifier](../concept/c_LoadBalancerF5BIGIP.md) is provided to classify F5 load balancers using REST. The **F5 LB REST** pattern is also provided to explore the device. You don’t need to create an HTTP classifier for F5 load balancers.

Of all protocols that Discovery uses \(including WMI, SSH, and SNMP\), HTTP is the lowest priority by default. Discovery uses HTTP classification only if:

-   Shazzam determines that the ports for HTTP \(80\) and HTTPS \(443\) traffic are open.
-   The horizontal discovery process fails for the higher priority port probes \(WMI, SSH, and SNMP\) if the ports for those protocols are not open, or if discovery for those protocols fail. The horizontal discovery process can fail, for example, if SSH and SNMP credentials are not configured or are incorrect.

    **Note:** See [Port Probes](../reference/r_PortProbes.md) for more details on how port scanning works and to see the priorities of the different protocols.


HTTP classification launches the **HTTP Classify** probe to classify the device. The **HTTP - Classify** probe runs a GET request for each device for each HTTP classification. The URL of the request is built as follows: `PROTOCOL://IP:PORT/PATH`, where:

## Procedure

1.  Navigate to **All** &gt; **Discovery Definition** &gt; **CI Classification** &gt; **HTTP**.

2.  Select **New**.

3.  Fill out the form fields \(see table\):

    ![HTTP classification](../image/http-classi.png "The F5 HTTP classification")

<table id="table_cyf_r1c_cdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name for the classifier.

</td></tr><tr><td>

Path

</td><td>

Enter the path for the HTTP GET request.

</td></tr><tr><td>

Headers

</td><td>

Add an option header with a value. You can use a variable in the format `${variable}` instead of a static value. Supported headers depend on the REST web service provider that you want to connect to. See the documentation for your web service provider to identify which headers are valid or required.

</td></tr><tr><td>

Port \(IP Service\)

</td><td>

If you want this classifier to use a custom port that is not already a default value in the IP Service \[cmdb\_ip\_service\] table, do the following:

 1.  Select the lookup icon to see the list of IP Services.
2.  Select **New** and create a port-to-protocol mapping.
3.  Select that port-to-protocol mapping for this **Port** field.
 Many commonly used protocols are already mapped to ports by default, such as `http` to port 80 and the `https` to port 443.

 If you want to use one of these default port-to-protocol mappings, don’t enter any values in the **Port** field. The HTTP port probe uses the correct one by default.

</td></tr><tr><td>

Order

</td><td>

Enter a number that represents the priority of this classifier. If Discovery finds more than one classifier that applies, it uses the classifier with lower **Order** number.

</td></tr><tr><td>

Protocol\[optional\]

 This field isn’t visible by default. You must configure the form to add it.

</td><td>

If you configure a unique port-to-protocol mapping for the **Port** field, enter an optional protocol override that Discovery uses with this classifier.

For example, if you want to use port 5000 and the HTTP protocol, add the 5000/HTTP port-to-protocol mapping to the **Port** field, and then choose **http** in the **Protocol** field.

</td></tr></tbody>
</table>4.  Right-click the header and select **Save**.

    A record is created in the HTTP Classifications \[discovery\_classy\_http\] table.

    The HTTP Classification Match related list appears. This related list shows criteria that you can configure to match against the body of the response to the GET Request that Discovery sends.

5.  In the HTTP Classification Match related list, define the criteria and specify the pattern to launch for this classifier.

    The criteria must be met for Discovery to use this HTTP classifier.

    1.  Select **New**.

    2.  On the HTTP Classification Match form, fill in the form fields \(see table\).

        ![HTTP classification match](../image/http-classi-match.png)

<table id="table_vjr_l3c_cdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Operator

</td><td>

Choose the operator that the system uses to evaluate the condition: -   **Contains**
-   **Equals**
-   **Regex**


</td></tr><tr><td>

Order

</td><td>

Enter a number that represents the priority of this condition. If Discovery finds more than one condition that applies, it uses the condition with lower Order number.

</td></tr><tr><td>

Pattern

</td><td>

Specify the pattern to launch upon a correct match. This pattern must use HTTP to discover the device.

</td></tr><tr><td>

Value

</td><td>

Enter the value that the body of the returned REST method must have.

</td></tr></tbody>
</table>    3.  Select **Submit**.

    4.  If there are different patterns for different versions of the device you’re trying to discover, define as many HTTP Classification Matches as necessary.


