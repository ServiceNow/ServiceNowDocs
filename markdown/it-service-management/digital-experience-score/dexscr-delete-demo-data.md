---
title: Delete Digital Experience Score​ demo data
description: Delete the demo data for Digital Experience Score​ when you no longer need it.
locale: en-US
release: yokohama
product: Digital Experience Score
classification: digital-experience-score
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Install Digital Experience Score​, Configuring Digital Experience Score​, Digital Experience Score​, Digital End-User Experience, IT Service Management]
---

# Delete Digital Experience Score​ demo data

Delete the demo data for Digital Experience Score​ when you no longer need it.

## Before you begin

[Install Digital Experience Score​](install-dex-score.md)

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Find and open the **DeleteAggregatedDemoDataDexScore** scheduled job.

3.  Select **Execute Now**.

    The job runs in the background.

4.  Verify the completion status of the scheduled job.

    1.  Access the Pending Scheduled Jobs and Running Scheduled Jobs tables.

        -   Pending Scheduled Jobs: Navigate to **All** &gt; **System Diagnostics** &gt; **Pending Scheduled Jobs**.
        -   Running Scheduled Jobs: Navigate to **All** &gt; **System Diagnostics** &gt; **Running Scheduled Jobs**.
    2.  Verify that the **DeleteAggregatedDemoDataDexScore** job isn’t listed in either of the tables.

5.  Navigate back to the scheduled jobs list.

6.  Find and open the **DeleteDemoDataDexScore** scheduled job.

7.  Select **Execute Now**.

    The job runs in the background.

8.  Verify that the **DeleteDemoDataDexScore** job isn’t listed in the Pending Scheduled Jobs and Running Scheduled Jobs tables.

9.  Delete records that are in the global scope.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Scripts - Background**.

    2.  Enter the deletion script in the **Run script \(JavaScript executed on server\)** field.

        ```
        var prefix = "[DEXScore Demo]";
               //Deleting computer records
               var comp = new GlideRecord('cmdb_ci_computer');
              comp.addEncodedQuery('nameSTARTSWITH' + prefix);
               comp.query();
               comp.deleteMultiple();
               //Deleting User Records
               var userGR = new GlideRecord("sys_user");
              userGR.addEncodedQuery('nameSTARTSWITH' + prefix);
               userGR.query();
               userGR.deleteMultiple();
               //Deleting CMN Location Records
               var location = new GlideRecord('cmn_location');
              location.addEncodedQuery('nameSTARTSWITH' + prefix);
               location.query();
               location.deleteMultiple();
        ```

    3.  If the default value for the **in scope** field is not set to **global**, select **global** from the drop-down list.

    4.  Select **Run Script**.


## Result

After both scheduled jobs run successfully and the script to delete records in global scope executes, the demo data is deleted from the instance.

If an error occurs during execution of the scheduled jobs, run the jobs again.

**Parent Topic:**[Install Digital Experience Score​](install-dex-score.md)

**Related topics**  


[Load Digital Experience Score​ demo data](dexscr-load-demo-data.md)

