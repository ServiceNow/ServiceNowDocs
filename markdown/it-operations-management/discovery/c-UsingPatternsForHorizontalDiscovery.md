---
title: Patterns and horizontal discovery
description: A pattern is a series of operations that tell Discovery which CIs to find on your network, what credentials to use, and what tables to populate in the CMDB.Pattern Orchestrator is a process that allows a discovery to trigger multiple patterns related to a collection of data in a hierarchical manner. This is to help address issues with large datasets \(or large payloads\) that can cause slow discoveries and OOM \(out-of-memory\) issues on a MID Server.To use a pattern for the identification and exploration phases of horizontal discovery, you must add the Horizontal Pattern probe to the classifiers for the CIs are you trying to discover.If you want to use a new pattern, or if you already have a pattern that you were using for top-down discovery, you can use the pattern for horizontal discovery with a few modifications to the relevant classifier.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Patterns and horizontal discovery

A pattern is a series of operations that tell Discovery which CIs to find on your network, what credentials to use, and what tables to populate in the CMDB.

This topic assumes you understand the phases of horizontal discovery. If you need to review the horizontal discovery process for probes and for patterns, see the following:

-   [Horizontal discovery process flow with probes and sensors](c_DiscoProcessFlows.md)
-   [Horizontal discovery process flow with patterns](disco-process-flow-patterns.md)

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## How Discovery uses patterns

A pattern performs the same function as a probe: it identifies and explores a target CI. Discovery uses patterns only during the last two phases of discovery: Identification and Exploration.

When you kick off horizontal discovery with patterns, the Scanning and Classification phases run as they would if you were not using patterns \(only using probes and sensors\). After the Classification stage completes, Discovery looks at the trigger probes on the classifier to see which probe to launch. When the **Horizontal Pattern** probe is specified as a trigger probe, Discovery launches both the **Horizontal Pattern** probe and the pattern that it specifies.

**Important:** Discovery now enforces code signing for Horizontal Pattern probes, probe parameters, and sensors when code signing is enabled on the instance. Unsigned or tampered payloads are blocked, and signatures are validated before execution. For more information about code signing, see [Discovery on Code Signing instances](code-sign-disco-probes.md).

## Differences between probes and patterns

The main differences between using patterns for horizontal discovery and using only probes for horizontal discovery are outlined in this table:

<table id="table_zxz_nfj_h2b"><thead><tr><th>

Topic

</th><th>

Horizontal discovery with probes

</th><th>

Horizontal discovery with patterns

</th></tr></thead><tbody><tr><td>

Discovery phases

</td><td>

Probes run during all four discovery phases.

</td><td>

Patterns run only during the identification and exploration phases. Discovery still uses the Shazzam probe and port probes to kick off discovery.

</td></tr><tr><td>

Finding new CIs

</td><td>

Discovery offers several out-of-box probes and sensors.

 However, if you want to find new CIs or change the data that Discovery populates in the CMDB, you must create news probes and sensors or customize the existing ones. To do this, you need knowledge of Java and JavaScript, and you need to understand how probes work together with other probes and with sensors.

</td><td>

Discovery is offering more patterns in every major release and on the [ServiceNow App Store](https://store.servicenow.com/sn_appstore_store.do#!/store/search?apptype=servicenow&orderby=rating).

 If you want to create a new pattern or customize an existing one, you can use the pattern designer, which is a user-friendly interface that helps you construct steps and enter values.

</td></tr><tr><td>

Feature support

</td><td>

Supports all standard network, and CI discovery. Certain applications are not supported without the use of patterns. See [Detailed information on products discovered by ITOM Visibility](../../service-mapping/reference/r_SupportedApplications.md) for a full list.

</td><td>

In addition to supporting all standard discovery, patterns support: -   Cloud discovery
-   configuration file tracking
-   CI deletion strategies

</td></tr><tr><td>

The ECC queue and troubleshooting

</td><td>

Discovery creates Multiple ECC Queue records depending on how many probes are launched.

 To troubleshoot any issues with horizontal discovery, you must analyze several ECC queue records to see the data that Discovery retrieved.

</td><td>

Discovery creates only one additional ECC queue record for the pattern.

 To troubleshoot any issues with horizontal discovery during identification and exploration, you only have to analyze one ECC queue record for the pattern.

</td></tr><tr><td>

Performance

</td><td>

Depending on what type of target CI you are trying to identify and explore, Discovery might trigger multiple probes during the identification phase, and then trigger additional probes during the discovery phase. It is possible that horizontal discovery with probes can take longer because of the extra overhead in triggering and processing many probes.

</td><td>

Discovery triggers one pattern during the identification an exploration phases. All operations that Discovery needs to run are in the pattern and Discovery can execute them in order until the pattern is finished. Therefore, pattern discovery can lead to faster performance.

</td></tr></tbody>
</table>## Patterns for top-down and for horizontal discovery

Both Discovery and Service Mapping can use the same pattern for horizontal and top-down discovery. But they are edited differently. See [Create or customize patterns](../../service-mapping/task/t_CreatePatternPatDef.md) for all steps. If you take a pattern that was exclusively used for top-down discovery and you want to use it for horizontal discovery, you have to make a few modifications. See [Use a pattern for horizontal discovery](c-UsingPatternsForHorizontalDiscovery.md#) for instructions.

**Parent Topic:**[Using Discovery](using-discovery.md)

## Pattern Orchestrator

Pattern Orchestrator is a process that allows a discovery to trigger multiple patterns related to a collection of data in a hierarchical manner. This is to help address issues with large datasets \(or large payloads\) that can cause slow discoveries and OOM \(out-of-memory\) issues on a MID Server.

The Pattern Orchestrator is accessed in the **Pattern Orchestrator** tab in the **Pattern Designer**. The tab contains three new tables: **Trigger Rules**, **Orchestrator Input**, **Orchestrator Output**.

![The Pattern Orchestrator tab in the Pattern Designer.](../image/pattern-orchestrator-tab.png)

The **Trigger Rules** table specifies the parent pattern with the **Parent Pattern** field. The **Batch Size** field specifies how many items should be triggered from the parent pattern to the child pattern. **Batch Size** has the options **Count**, **All**, and **Use Parent Context Only**.

-   **Count** must specify a number for the **Batch Size Count**. The child pattern is triggered each time the parent pattern sends the specified number of CIs.
-   **All** uses every CI sent from the parent pattern and triggers the child one time.
-   **Use Parent Context Only** relies on the parent pattern's output settings to dictate which child pattern should trigger. This is useful when two patterns have the same parent, but you need one to trigger before the other.

The **Orchestrator Input** uses the **CI Type** field to accept CI types from its parent pattern or parent's parent pattern. The **Saved As** field saves the CI type's name to be used in the pattern. Service accounts are a special case and must be named service\_account. The **CI Attributes** field uses any outputs from the parent pattern to select which attributes to use.

The **Orchestrator Output** controls which data will be sent to subsequent patterns. It has the fields **CI Class Type**, which is the type of CI being discovered, and **Variable Names** which specifies the variables to be passed on as inputs to child patterns. Any variables not specified in **Variable Names** are not sent to child patterns. The variable **source\_native\_key** can be manually added by searching for it in the **Variable Names** field.

### Source Native Key

In some situations, one pattern may get partial information about a CI, while another pattern gets partial info about the same CI. Instead of creating redundant records or discarding partial information, the information is stored in the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\_list\] table. After enough patterns gather partial information, it can correlate that data to provide complete information on the CI.

### Pagination

Another way to reduce stress on the MID Server's memory is pagination. Pagination breaks a large payload up into smaller, ordered slices called pages. Pagination limits the maximum size of items received and generates a token. Once that page is processed, the token is passed to the next page, which is then processed, until all the pages are completed.

Pagination is controlled from the Custom Operations table \[sa\_custom\_operation\]. The field **Is pagination capable** is hidden by default on the form, and can be added to the form with the **Personalize Form** controls. Once that is set to true, the associated pattern in the pattern designer has the field **Paginated**. Setting the **Paginated** field to true runs that step in the pattern with pagination.

## Add the Horizontal Pattern probe to a classifier

To use a pattern for the identification and exploration phases of horizontal discovery, you must add the Horizontal Pattern probe to the classifiers for the CIs are you trying to discover.

### Before you begin

Role required: discovery\_admin

### About this task

**Warning:** This procedure is only intended for custom classifier records or those that do not include a pattern by default. However, if you have already populated your CMDB with data using probes from this classifier and then switch to use patterns, Discovery may create duplicate CIs. Therefore, only follow this procedure if you have never run Discovery with probes for this classifier type.

### Procedure

1.  Navigate to **All** &gt; **Discovery Definition** &gt; **CI Classification** &gt; **\{classifier type\}**.

2.  Open the classifier record.

3.  Click the **Triggers probe** related list.

4.  Deactivate the existing identification and exploration probes.

5.  Click **Edit**, and add the **Horizontal Pattern** probe.

    The probe appears in the related list.

6.  From the related list view, double click the field under the **Pattern** column and add the pattern you want to associate with the classification.

    ![Adding the Horizontal Pattern probe and a pattern](../image/TriggerProbe-HorizontalProbe.png)

7.  Remove or deactivate the other probes from the **Triggers probe** related list.

    **Note:** If you delete a pattern, the Horizontal Pattern probe is not automatically removed from the classifier. You must select another pattern for the Horizontal Probe, or you can switch back to using identification and exploration probes specific to the classifier. If you use the Horizontal Probe without a pattern specified, discovery stops after the classification stage.


## Use a pattern for horizontal discovery

If you want to use a new pattern, or if you already have a pattern that you were using for top-down discovery, you can use the pattern for horizontal discovery with a few modifications to the relevant classifier.

### Before you begin

Role required: discovery\_admin

### About this task

**Warning:** This procedure is only intended for custom classifier records or those that do not include a pattern by default. However, if you have already populated your CMDB with data using probes from this classifier and then switch to use patterns, Discovery may create duplicate CIs. Therefore, only follow this procedure if you have never run Discovery with probes for this classifier type.

### Procedure

1.  Verify that Discovery can use the pattern:

    1.  Navigate to **Pattern Designer** &gt; **Discovery Patterns**.

    2.  Open the pattern.

        Application patterns that Service Mapping uses are indicated as type **1-Application**.

    3.  In the **Identification Sections** on the **Basic** tab, verify that there is at least one section that allows for an entry point type of **TCP** or **All**.

        If not, create one. See the Identification steps for [creating a new pattern](../../service-mapping/task/t_CreatePatternPatDef.md).

    4.  Save the pattern.

2.  On the instance, create or modify the classification for the CI type you want to discover.

    Configure the classifier as follows:

    1.  Navigate to **Discovery Definition** &gt; **CI Classification** &gt; **\{classification type\}**.

    2.  Open the relevant classifier.

    3.  Configure the classifier as follows:

        -   **Relationship type**: Select **Runs on::Runs** \(for process classifiers only\)
        -   **Condition**: Configure the same condition you defined in the pattern.
        -   **Triggers probes** Related list: Add the Horizontal Pattern probe, and then add the pattern you are using to the **Pattern** column.
    See [Create a Discovery CI classification](../task/create-discovery-ci-classification.md) for a description of the other fields on the classifier.


### What to do next

Run the pattern in [Debug mode](../../service-mapping/task/t_CreatePatternPatDef.md) to test it. When you are sure the pattern works, you can run discovery by setting up a discovery schedule or running an on-demand discovery. See [Schedule a horizontal discovery](../task/t_CreateADiscoverySchedule.md#) for more information.

