---
title: Define Eligibility Questions in License and Permit Playbook
description: Configure the eligibility criteria questions for users beginning an application for a license or permit.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Eligibility in License and Permit Playbook, License and Permit Playbook, Playbooks, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Define Eligibility Questions in License and Permit Playbook

Configure the eligibility criteria questions for users beginning an application for a license or permit.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Variables** &gt; **Variables Sets**.

2.  In the Variable Set list view, select **New**.

3.  Select **Single-Row Variable Set**.

4.  Enter the desired title and internal name and select **Submit**.

5.  In the list, locate and open the newly created Variable Set.

6.  In the **Variables** related list, select **New** to create a variable for each eligibility question.

7.  Select **Yes/No** as the variable type.

8.  Repeat steps 6-7 until a variable is created for each eligibility question.

9.  Create a variable with the name **Eligible**, and enter **Yes/No** in the Question field.

10. Select **Yes/No** as the variable type.

11. In the **Catalog UI Policies** related list, select **New**.

12. Enter a short description for the policy.

13. Navigate to the **When to Apply** tab.

14. Add a catalog condition to the UI policy for each eligibility question, and set the condition to **is Yes**.

15. Navigate to the **Script** tab, and add the following scripts to the True and False conditions.

16. Select **Submit**.

17. Navigate to  **All ** &gt; **Service Catalog ** &gt; **Catalog Definition ** &gt; **Record Producers**.

18. Locate the License/Permit Record Producer and open the record.

19. Navigate to the **Variable Sets** tab and then select **Edit**.

20. Locate the Variable Set created for the eligibility criteria and move it to the variable sets list by selecting the right arrow button.

21. Select **Save**.


## Result

The eligibility criteria questions are now defined and can be used to determine if a constituent is eligible to begin a license or permit application.

