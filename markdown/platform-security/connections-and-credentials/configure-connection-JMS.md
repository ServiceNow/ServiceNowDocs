---
title: Create a JMS connection
description: Configure your system to use Java Messaging Service \(JMS\) with a custom JMS activity or action.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Get started with connections, Connections and Credentials, Access Management]
---

# Create a JMS connection

Configure your system to use Java Messaging Service \(JMS\) with a custom JMS activity or action.

## Before you begin

Role required: connection\_admin

## About this task

The MID Server must have the correct JMS connection factories for your organization. Configure those values in the **mid.property.jms.command.allowed\_factory\_names** property, found in **MID Server** &gt; **Properties**. The default values for this property can be changed to any value or comma-separated list of values that the third-party JMS provider advertises.

## Procedure

1.  Navigate to **Credentials &amp; Connections** &gt; **Connections**.

2.  Click **New**, select **JMS Connection**, fill in the form, and then click **Submit**.

<table id="choicetable_gqc_pd4_5y"><tbody><tr><td id="d201569e104">

**Name**

</td><td>

Unique name of this connection factory.

</td></tr><tr><td id="d201569e113">

**Credential**

</td><td>

Add credentials for JMS provider.

</td></tr><tr><td id="d201569e122">

**Connection Alias**

</td><td>

Select the alias record to associate with this connection. Using an alias enables you to update the connection record without having to reconfigure any actions or activities that use the alias.

</td></tr><tr><td id="d201569e134">

**Initial Context Factory**

</td><td>

Name of the JNDI class that is used to create the InitialContext. **Note:** For example, to connect to ActiveMQ V5.10 \(JMS Provider\), the value is `org.apache.activemq.jndi.ActiveMQInitialContextFactory`.

</td></tr><tr><td id="d201569e149">

**Provider URL**

</td><td>

Location of the running JMS provider installation. **Note:** For example, to connect to ActiveMQ V5.1: `tcp://ipAddressOrHostName:61616`.

</td></tr><tr><td id="d201569e165">

**Active**

</td><td>

Check the box to make this an active connection.

</td></tr><tr><td id="d201569e174">

**Domain**

</td><td>

Determine the domain the action or activity runs in.

</td></tr><tr><td id="d201569e183">

**Use MID server**

</td><td>

Check to use a MID Server for this action or activity. If selected, define fields in the Advanced MID Server Configuration section.

</td></tr><tr><td id="d201569e192">

**MID Selection**

</td><td>

Option to select a specific MID Server or MID Cluster. Choose any one of the following options. -   **Auto-Select MID Server**: Your ServiceNow instance selects the MID Server without manual input.
-   **Specific MID Server**: Your ServiceNow instance uses MID Server that you specify.
-   **Specific MID Cluster**: Your ServiceNow instance uses the MID Cluster that you specify.

A MID Cluster is a group of MID Servers that enables your ServiceNow instance to handle multiple integrations, and improve integration speed. For more information, see [Configure a MID Server cluster](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

 This field is available when **Use MID Server** is checked.

</td></tr><tr><td id="d201569e252">

**MID Cluster**

</td><td>

The specific MID Cluster you want to use. This field is available when **Use MID Server** is checked, and **Specific MID Cluster** is selected from the MID Selection list.

</td></tr><tr><td id="d201569e270">

**Capabilities**

</td><td>

The capabilities the MID Server must support to be eligible for selection. The system runs the action or activity from a MID Server that supports the selected capabilities. Only displays if **Use MID server** is selected.

 To learn more about how a MID Server is selected during runtime, see [MID Server selection](https://www.servicenow.com/docs/access?context=c_MIDServerSelector&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td id="d201569e304">

**MID Application**

</td><td>

The application the MID Server must support to be eligible for selection. The system runs the action from a MID Server that supports the selected application. Only displays if **Use MID server** is selected.

 To learn more about how a MID Server is selected during runtime, see [MID Server selection](https://www.servicenow.com/docs/access?context=c_MIDServerSelector&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr></tbody>
</table>3.  Navigate to **Connections &amp; Credentials** &gt; **Credentials**.

4.  Click **New**, select **JMS Credentials**, and then provide the user name and password the MID should use to communicate with the JMS provider.

    For more information, see [JMS credentials](../reference/r_JMSCredentialsForm.md).

5.  Click **Submit**.

    You are ready to create a custom JMS action or activity.


**Parent Topic:**[Get started with connections](../reference/connection-information.md)

