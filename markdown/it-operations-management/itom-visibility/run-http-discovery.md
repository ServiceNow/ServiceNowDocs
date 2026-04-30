---
title: Run discovery through an HTTP or HTTPS REST call
description: Discovery can classify devices using the HTTP\(S\) protocol. You can create your own HTTP classifier to find devices and access them with Basic Auth credentials, rather than using SNMP or SSH credentials.
locale: en-US
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [HTTP device, Network device discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Run discovery through an HTTP or HTTPS REST call

Discovery can classify devices using the HTTP\(S\) protocol. You can create your own HTTP classifier to find devices and access them with Basic Auth credentials, rather than using SNMP or SSH credentials.

## Before you begin

Role required: discovery\_admin

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Credentials**.

2.  Select **New**.

3.  Select **Basic Auth Credentials**.

    In most cases, you can use Basic Auth Credentials to access a device through an HTTP or HTTPS REST call.

    **Important:** The HTTP Classify probe no longer attempts credentials over the HTTP protocol by default. To override this behavior, you can enable **mid.http\_classy.allow\_credentials\_over\_http**. However, enabling this setting can expose credentials to man-in-the-middle \(MitM\) attacks. Therefore, it’s strongly recommended to keep this property set to **false** and use HTTPS whenever possible.

4.  Add the user name and password that you need to access the device.

5.  Select **Submit**.

6.  Set up an HTTP classifier by navigating to **Discovery Definition** &gt; **CI Classification** &gt; **HTTP**.

7.  Select **New**.

8.  Fill out the form fields \(see table\):

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
</table>9.  Right-click the header and select **Save**.

    The HTTP Classification Match related list appears. This related list shows criteria that you can configure to match against the body of the response to the GET Request that Discovery sent.

10. In the HTTP Classification Match related list, define the match criteria and specify the pattern to launch for this classifier:

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

    4.  Define as many HTTP Classification Matches as necessary.

        You might want to do this if there are different patterns for different versions of the device you’re trying to discover.


## Example

In this example, HTTP classification is configured to use the F5 load balancer API:

## What to do next

If you don’t have other types of credentials that can find devices, such as Linux credentials or SNMP credentials, you can see how the Discovery application processes HTTP discovery:

1.  Navigate to **Discovery** &gt; **Discovery Schedules** and run a discovery.
2.  After the discovery process completes, check the ECC Queue to see the results of the HTTP discovery.

    You should see that after the Shazzam probe was launched, and that UNIX and SNMP classification probes failed. Both the HTTP - Classify probe and the pattern that you specify in the HTTP classification record should launch.

    ![HTTP classification ECC Queue records](../image/http-classy-ecc-records.png)


**Parent Topic:**[HTTP device discovery](../concept/http-discovery.md)

