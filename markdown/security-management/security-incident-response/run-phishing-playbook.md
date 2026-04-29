---
title: Run the automated phishing response playbook flow
description: Using the flow designer, you can define and automate tasks in the playbook to analyze and resolve phishing attacks against your organization.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Playbook for Automated Phishing, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Run the automated phishing response playbook flow

Using the flow designer, you can define and automate tasks in the playbook to analyze and resolve phishing attacks against your organization.

## Before you begin

-   Role required: sn\_si.admin, flow\_designer, and action\_designer
-   Install and configure the following integrations with the right credentials:
    -   Block Request \(Security Operations Palo Alto Networks NGFW Integration\)
    -   Observable Enrichment
    -   Sighting search
    -   Threat Lookup
    -   Microsoft Office Exchange

## About this task

When employees receive a suspicious email that contains the common signs of a phishing attack \(as defined by your security policies\), they can send it as an .EML attachment to the phishing email address defined by your organization. Using the tasks defined in the automated phishing playbook flow, you can triage, analyze, contain, and eradicate a phishing threat. These tasks can be invoked as part of different incident states \(for example, Analysis, Contain, and so forth\). When a phishing security incident is created, the automated phishing flow can be automatically triggered. Using flow designer, you can view the details of the various incident response actions as they are invoked.

**Note:** The Security Incident - Automated Phishing Response Template V1 playbook flow is Read Only. You can make a copy of the flow and make changes as required.

The following steps describe how to make a copy of the phishing playbook template and walks you through some of the tasks in the flow.

## Procedure

1.  Navigate to **All** &gt; **Flow Designer** &gt; **Designer** to view the flows available with the Security Operations Spoke.

2.  Click the **Security Incident - Automated Phishing Response Template VI** link.

3.  In the Flow page, click the more icon ![More icon](../image/cj-sir-flow-more-icon.png), make a copy of the flow and open it for your use.

    You can modify the trigger conditions, add or remove actions, and make other changes to the flow.![Automated phishing playbook flow](../image/cj-sir-flow-auto.png)

    This image shows the trigger conditions, and the steps that the flow executes. The right-hand panel shows the data flow. Click an icon to expand the step and view the details.

4.  Click the **Trigger** icon.

    In the first step, you define or set the trigger for the flow. Specify the conditions for the trigger and how often you want the flow to execute the trigger.![Automated phishing playbook flow: trigger](../image/cj-sir-flow-phishing-trigger.png)

    When the conditions defined in the flow \(Category is Phishing and Source is Email\) are met in the incident record, the tasks in the automated phishing flow start executing sequentially. You can modify the trigger, add annotations, add or delete conditions, and so on.

5.  Click the **Update Security Incident Record** link.

    ![Automated phishing playbook flow: step 1](../image/cj-sir-flow-phishing-action1.png)

    The Update Security Incident Record is the first step in the flow. Click the annotation icon ![Annotation icon](../image/cj-sir-flow-annotation.png) to add a note to the security analyst indicating that a phishing incident has occurred, and the automated phishing playbook flow has begun executing.

6.  Proceed with the step 2 in the flow, and click the **Create Response Task** link.

    In this step, the flow creates an automated response task to acknowledge receipt to the submitter of the incident or the affected user.

    ![Automated phishing playbook flow: step 2](../image/cj-sir-flow-action2.png)

    Notice the **Parent Task \[Security Incident\]** field references the parent record associated with this step. You can pick any reference record by using the data pill picker icon ![Data pill picker icon](../image/cj-sir-flow-datapill-icon.png) or drag the relevant reference item from the right-hand panel. Notice the lock icon ![Lock icon](../image/cj-sir-flow-lock-icon.png). The lock icon indicates that step does not require any user intervention.

7.  In step 3, the flow collects additional details of the affected user \(typically the user who submitted the incident\) to ensure that it can send a notification successfully.

    You can specify conditions to check if the affected user's status is active and the user is able to receive notifications.![Automated phishing playbook flow: step 3](../image/cj-sir-flow-phishing-action3.png)

    Notice the conditional step icon ![Conditional step icon](../image/cj-sir-flow-condition-icon.png) in step 3. The flow executes the next step \(3.1\) only if the specified conditions are met.

    ![Automated phishing playbook flow: step 3.1](../image/cj-sir-flow-phishing-action3-1.png)

    When the conditions defined in step 3 have been met successfully, the email is sent.

8.  In step 4, after the email has been sent, the response task is marked as closed.

    ![Automated phishing playbook flow: step 4](../image/cj-sir-flow-phishing-action4.png)

9.  In step 5, all the observables involved in the incident \(such as email subject, email address from which the phishing email was sent, phishing URL\) or observables belonging a selected category \(hash, file, or domain\) are collected to perform additional automated actions in the subsequent playbook steps.

    ![Automated phishing playbook flow: step 5](../image/cj-sir-flow-phishing-action5.png)

    Click the action designer icon ![Action designer icon](../image/cj-sir-flow-actiondesign-icon.png) to see a detailed view of the action.

    To view the [Action Designer](../concept/action-phishing-playbook.md) page, expand a step in the flow and click the action designer icon.

10. In step 6, an automated response task is created.

    This task captures the beginning of process of getting the reputation of all observables and performing enrichment with configured integrations.![Automated phishing playbook flow: step 6](../image/cj-sir-flow-phishing-action6.png)

11. In step 7, two subflows are called:

    -   Run Threat Lookups for Observables: This subflow is used to get the reputation of all observables using threat look up implementations.
    -   Enrich Observables: This subflow is used perform enrichment of observables with configured implementations.
    ![Automated phishing playbook flow: step 7](../image/cj-sir-flow-phishing-action7.png)

    Notice the icons for this task. The parallel operations icon ![Parallel operations icon](../image/cj-sir-flow-paralllelops-icon.png) indicates that both the tasks will be performed in parallel and the subflow icon ![Subflow icon](../image/cj-sir-flow-subflow-icon.png) indicates that the task being performed is a subflow as shown below:

    ![Automated phishing playbook flow: step 7.1.1](../image/cj-sir-flow-phishing-action7-1.png)

    Notice the number 5 in the observables field. This indicates that the threat lookup will be run on observables retrieved in step 5. This subflow in turn calls existing workflows and actions as shown in the [Subflow Designer](../concept/subflow-phishing-playbook.md).

12. In step 8, after the subflows have been completed, the response task is marked as Closed.

    ![Automated phishing playbook flow: step 8](../image/cj-sir-flow-phishing-action8.png)

13. In step 9, the Confirm Threat from Observable Triage subflow is called.

    This subflow is used to confirm the presence of a threat indicator in the incident. If the threat is confirmed, an 'IOC Detected' flag is added to the incident.![Automated phishing playbook flow: step 9](../image/cj-sir-flow-phishing-action9.png)

14. When the threat is confirmed, in step 10, you update the security incident and add a note indicating that threat containment tasks will be launched.

    ![Automated phishing playbook flow: step 10](../image/cj-sir-flow-phishing-action10.png)

15. Step 11 is an automated response task that captures the start and completion of the task used to assess the impact of the phishing emails.

    ![Automated phishing playbook flow: step 11](../image/cj-sir-flow-phishing-action11.png)

16. In step 12, the Assess Phishing Email Impact subflow is called.

    This subflow is used to search for users who have received the phishing email using supported implementations.![Automated phishing playbook flow: step 12](../image/cj-sir-flow-phishing-action12.png)

17. In step 13, the task is marked as closed to indicate that the Assess Phishing Email Impact subflow has been executed.

    ![Automated phishing playbook flow: step 13](../image/cj-sir-flow-phishing-action13.png)

18. Step 14 is used to retrieve all observables that have been marked as malicious.

    ![Automated phishing playbook flow: step 14](../image/cj-sir-flow-phishing-action14.png)

19. Step 15 is an automated response task that captures the start and completion of the sighting search of observables task.

    ![Automated phishing playbook flow: step 15](../image/cj-sir-flow-phishing-action15.png)

20. In step 16, the Run Sightings Search on Observables subflow is called.

    This subflow performs a sightings search using the configured implementation.![Automated phishing playbook flow: step 16](../image/cj-sir-flow-phishing-action16.png)

21. In step 17, the task is marked as closed to indicate that the Run Sightings Search on Observables subflow has been completed.

    ![Automated phishing playbook flow: step 17](../image/cj-sir-flow-phishing-action17.png)

22. After you have identified the malicious observables, in step 18, you update the security incident record to indicate that the containment actions will now commence.

    ![Automated phishing playbook flow: step 18](../image/cj-sir-flow-phishing-action18.png)

23. Step 19 is an automated response task that captures the start and completion of the block requests task.

    ![Automated phishing playbook flow: step 19](../image/cj-sir-flow-phishing-action19.png)

24. In step 20, the Create Block Requests subflow is called.

    This subflow is used to block malicious observables.![Automated phishing playbook flow: step 20](../image/cj-sir-flow-phishing-action20.png)

25. In step 21, the task is marked as closed to indicate that the Create Block Requests subflow has been completed.

    ![Automated phishing playbook flow: step 21](../image/cj-sir-flow-phishing-action21.png)

26. In step 22, the Eradicate Phishing Emails subflow is called.

    This subflow is used to delete phishing emails from user mailboxes.![Automated phishing playbook flow: step 22](../image/cj-sir-flow-phishing-action22.png)

27. After the phishing emails have been deleted, in step 23, you update the security incident record to indicate that the incident status needs to be reviewed.

    ![Automated phishing playbook flow: step 23](../image/cj-sir-flow-phishing-action23.png)

28. In the last step, the flow creates an automated response task.

    This task is used to send a reminder to the security analyst to save all the incident response actions for future reviews. ![Automated phishing playbook flow: step 24](../image/cj-sir-flow-phishing-action24.png)


## What to do next

You can click **Test** to simulate the actions in the flow before you publish it. After testing the flow, click **Activate** to activate the flow and execute it.

Click **Executions** to view the execution details of the flow.

![Automated phishing flow: execution](../image/cj-sir-flow-execute.png)

-   **[View automated phishing response playbook flow action designer](../concept/action-phishing-playbook.md)**  
You can drill down to the Action Designer to view detailed information about the actions being performed for a specific step in the automated phishing response playbook flow.
-   **[View the automated phishing response playbook subflow designer](../concept/subflow-phishing-playbook.md)**  
You can drill down to the Subflow Designer to view detailed information about the subflow being executed as part of the automated phishing response playbook flow.

**Parent Topic:**[Playbook for Automated Phishing](../concept/flow-designer-and-phishing-response.md)

