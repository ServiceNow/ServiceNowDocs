---
title: Transaction Manager: Integrate Salesforce approvals
description: Integrate Salesforce approvals into Transaction Manager.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-13"
reading_time_minutes: 8
breadcrumb: [Transaction Manager, ServiceNow CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Transaction Manager: Integrate Salesforce approvals

Integrate Salesforce approvals into Transaction Manager.

![Menu](../images/cpq-txn-mgr-integrate-SF-approvals-1.png)

![Transaction](../images/cpq-txn-mgr-integrate-SF-approvals-2.png)

## Salesforce setup

Refer to these Trailheads modules and documentation:

-   Postman: [Quick Start: Connect Postman to Salesforce](https://trailhead.salesforce.com/content/learn/projects/quick-start-connect-postman-to-salesforce)
-   Submit for Approval: [Salesforce Developers](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/dome_process_approvals_submit.htm)

An approval process in Salesforce automates record approval workflows in an organization. It defines:

-   Approval Steps: The sequence of steps and approvers for a record, for example, sending a time-off request to an employee’s manager for approval.
-   Actions: Automated actions based on the approval outcome, such as updating records if approved or sending notifications if rejected.

This streamlines the approval process and ensures consistency.

![Workflow](../images/cpq-txn-mgr-integrate-SF-approvals-sf-setup-1.png)

1.  Go to Setup → Approval Processes and select the relevant object, in this case, the "Transaction" record.
2.  In Manage Approval Processes For, select Opportunity.
3.  Click **Create New Approval Process** \| Use Jump Start Wizard.

    ![Create New Approval Process](../images/cpq-txn-mgr-integrate-SF-approvals-sf-setup-2.png)

4.  Ensure the “Add the Submit for Approval and Approval History” option is checked.

    You can specify conditions, if applicable, under the "Entry-Specific Criteria" section.

5.  Choose **Automatically assign approvers** and set it to anyone with the SysAdmin role.

    ![Automatically assign approvers](../images/cpq-txn-mgr-integrate-SF-approvals-rt-flow-3.png)

6.  Create a custom picklist field on the Transaction record by navigating to Setup → Object Manager → Transaction. Ensure that the field is not set as a “multi-select” picklist.

    ![Transaction](../images/cpq-txn-mgr-integrate-SF-approvals-sf-setup-4.png)

7.  Give the picklist field three values to distinguish between Pending Approval, Approved, and Rejected.

    ![New custom field](../images/cpq-txn-mgr-integrate-SF-approvals-sf-setup-5.png)

8.  Add the custom field to the Transaction Layout.

    ![Layout](../images/cpq-txn-mgr-integrate-SF-approvals-sf-setup-6.png)

    If you skipped the previous screenshot you can add the field to the Transaction Layout like:

    ![Layout](../images/cpq-txn-mgr-integrate-SF-approvals-sf-setup-7.png)

9.  Go back to the Approval Process and click **Initial Submission Actions**, and then click Add New -&gt; Field Update. Configure it with the required values.
10. Repeat step 9 for Approval Actions, and Rejection Actions sections to ensure that the relevant fields are updated based on the outcome of the approval process: \(Status=Pending\), Approval Actions\(Status=Approved\), and Rejection actions \(Status=Rejected\). The following screenshot shows the final rejection option.

    ![Transaction](../images/cpq-txn-mgr-integration-get-retrieve-opp-8.png)

    If you included email alerts along with field updates, the approval process should resemble the following:

    ![Approval process](../images/cpq-txn-mgr-integrate-SF-approvals-sf-setup-9.png)

    If the final approval process has only field updates, it should resemble the following:

    ![Approvalprocess](../images/cpq-txn-mgr-integrate-SF-approvals-sf-setup-10.png)

11. Click **Activate**.

    ![Activate](../images/cpq-txn-mgr-integrate-SF-approvals-sf-setup-11.png)

12. Ensure that CORS includes the URL. Search for CORS in the Setup search bar. Go to Setup → Security → CORS. Verify that these are included in the CORS:

    ![Security](../images/cpq-txn-mgr-integrate-SF-approvals-sf-setup-12.png)


## Transaction Manager setup: integrations

Create two Integrations for an event that will be used to submit the record for approval through transaction manager.

**Note:** If you want to test these calls in Postman, the endpoint is the my Salesforce URL: &lt;https://logik-1e-dev-ed.develop.my.salesforce.com/&gt;.

1.  Receive the Salesforce record ID: Fetch the right Salesforce record ID using the UUID. This integration is used for filling in the custom field for the integration above.

    -   Connection: Salesforce
    -   GET

        Additional path: `/services/data/v62.0/query/?q=SELECT Id, CreatedDate, LGK__TransactionUUID__c FROM LGK__Transaction__c WHERE LGK__TransactionUUID__c = '{{http://txn.id/}}'ORDER BY CreatedDate DESC`

    Response Transformation:

    ```
    {
      "fields": [
        {
          "variableName": "txn.custom.sfRecordID",
          "value": {{#each records}}{{#if @first}}"{{this.Id}}"{{/if}}{{/each}}
        },
        {
          "variableName": "txn.custom.opportunityName",
          "value": {{#each records}}{{#if @first}}"{{this.LGK__OpportunityId__r.Name}}"{{/if}}{{/each}}
        },
        {
          "variableName": "txn.custom.accountName",
          "value": {{#each records}}{{#if @first}}"{{this.LGK__AccountId__r.Name}}"{{/if}}{{/each}}
        }
      ]
    }
    ```

    UPDATED QUERY USE THIS:

    ```
    /services/data/v62.0/query/?q=SELECT Id, CreatedDate,LGK__OpportunityId__c,LGK__OpportunityId__r.Name, LGK__AccountId__r.Name, LGK__AccountId__c,LGK__TransactionUUID__c FROM LGK__Transaction__c WHERE LGK__TransactionUUID__c ='{{txn.id}}'ORDER BY CreatedDate DESC
    ```

    The “contextActorId” refers to the system Admin Record ID in Salesforce. It can be obtained by navigating to Setup → Users, then copying the ID from the URL of the specific user page.

    ![Integrations](../images/cpq-txn-mgr-integrate-SF-approvals-integrations-1.png)

2.  Submit for approval.
    -   Connection: Salesforce
    -   POST

        Additional path: `/services/data/v62.0/process/approvals`

        ![Approval process](../images/cpq-txn-mgr-integrate-SF-approvals-integrations-2.png)


Request Transformation:

```
{
  "requests" : [{
  "actionType": "Submit",
  "contextId": "{{txn.custom.sfRecordID}}",
  "nextApproverIds": [],
  "comments":"The line item has a discount percentage of {{txn.custom.overallDealDiscount}}%",
  "contextActorId": "005bm000003SKtJ", -- SF Record ID of user highlighted above
  "processDefinitionNameOrId" : "TM_SF_Approval", --should be the unique name fro process definition detail highlighted above
  "skipEntryCriteria": "true"}]
}
```

Make sure that the transform template has these values correctly:

![Code](../images/cpq-txn-mgr-integrate-SF-approvals-integrations-3.png)

## Transaction Manager setup: creating events

The Slack Approvals Integration is implemented through headless event API calls. In this approach, we’ll use these headless API calls in a Record-Triggered flow and perform the callout through Apex Actions.

![Create events](../images/cpq-txn-mgr-integrate-SF-approvals-create-events-1.png)

Note that the two integrations created in the previous step are designed to work in sequence. The first integration receives the Salesforce record ID, and the second integration submits it for approval. Alternatively, the process of receiving the Salesforce ID can occur on the "Open Transaction" action by adding the necessary configuration at that stage.

Create two additional events that will move the stage either forward for approval or backward for revision. Be sure to note down their respective variable names for use in the API callout configuration.

![Transition stages](../images/cpq-txn-mgr-integrate-SF-approvals-create-events-2.png)

![Decline](../images/cpq-txn-mgr-integrate-SF-approvals-create-events-3.png)

## Transaction Manager setup: adding the Submit for Approval button to the layout

The button events can be added to the “default\_draft” layout using the following JSON format:

```
{
  "type": "button",
  "event": "submitForApproval",
  "label": "Revise",
  "columnOrder": 2,
  "variableName": "revise"
},
```

Make sure to add the custom field to the draft fields: \[\] section; it’s not necessary to include it in the layout.

```
{
  "type": "ReadOnlyText",
  "label": "SF Record ID",
  "variableName": "txn.custom.sfRecordID"
},
```

## Record-triggered flow

VS Code Environment Setup: Install the VS Code extensions from this document: [Sales Engineering Team Member Setup](https://logikio.atlassian.net/wiki/spaces/SE/pages/1340342294)

1.  Following the [Approval Process Trailheads](https://trailhead.salesforce.com/content/learn/modules/business_process_automation), create a picklist record on the LGK\_\_Transaction\_\_C object that has the current approval state of the transaction and ensure the process updates the record based on Approval, Rejection, and Pending Approval.

    The following image shows a custom Field that will trigger the record-triggered field: the Approval\_Status\_\_C field that you made when you created the approval process.

    ![Approval process](../images/cpq-txn-mgr-integrate-SF-approvals-rt-flow-1.png)

    The following image shows what the flow will look like when its complete \(Setup → Process Automation → Flows\)

    ![Workflow](../images/cpq-txn-mgr-integrate-SF-approvals-rt-flow-2.png)

2.  In the Start block, click **Edit**.

    Trigger on the LGK\_\_Transaction\_\_C object based on the custom field as well as ensuring a UUID is not null. Also make sure to click **Run Asynchronously** and **Only when a record is updated to meet**.

    ![Configure trigger](../images/cpq-txn-mgr-integrate-SF-approvals-rt-flow-3.png)

3.  Add a Decision block and create outcomes for when the custom field you created is approved or rejected.

    ![Decision block](../images/cpq-txn-mgr-integrate-SF-approvals-rt-flow-4.png)


## Apex Code

I deployed this Apex Class through VS Code but I’m sure you could do it in Salesforce. The first step is the create a new Project with manifest.

![Manu](../images/cpq-txn-mgr-integrate-SF-approvals-apex-code-1.png)

Next, create an Apex Class \(in the blue box\) as well as a manifest.xml file \(in the green box\) that will go into the respective files in the project directory.

![Transaction Manager](../images/cpq-txn-mgr-integrate-SF-approvals-apex-code-2.png)

Apex code:

```
global with sharing class TransactionManagerFlow {
    global class FlowInput {
        @InvocableVariable(label='Triggering Record' required=true)
        global LGK__Transaction__c triggeringRecord;
    }
    // Handle logic for Rejected status
    @InvocableMethod(label='Logik.io Transaction callout from Salesforce' description='Makes callout to transition Logik.io transaction stage.')
    global static void handleApprovalStatus(FlowInput[] requestInputs) {
        System.debug('Handling Rejected status for Record: ' + requestInputs[0].triggeringRecord.Id);
        LGK__ConfigurationTenant__c customSettings = LGK__ConfigurationTenant__c.getInstance();
        String updatedRuntimeToken = '_gdyi0w0oGu1bNk3PO5exhUGqDFcZQVLIw';
        System.debug(updatedRuntimeToken);
        String endpoint = 'https://se-txn-sandbox.test02.logik.io';
        for (FlowInput eachTxn : requestInputs) {
            // Make the API request to transfer a transaction from 'new' stage to 'rejected' stage
            // (compare with snippet from ApprovalProcessHandler.makeApiCall)
            String uuid = eachTxn.triggeringRecord.LGK__TransactionUUID__c;
            Http http = new Http();
            HttpRequest request = new HttpRequest();
            request.setHeader('Origin', endpoint);
            if (eachTxn.triggeringRecord.Approval_Status__c == 'Rejected') {    
                request.setEndpoint(endpoint + '/api/t/' + String.valueOf(uuid) + '/events/revise'); // Example endpoint
                System.debug('Endpoint set for rejection' + request.getEndpoint());
            } else if (eachTxn.triggeringRecord.Approval_Status__c == 'Approved') {
                request.setEndpoint(endpoint + '/api/t/' + String.valueOf(uuid) + '/events/proceedToApproved'); // Example endpoint
                System.debug('Endpoint set for approval' + request.getEndpoint());
            }
            request.setMethod('POST');
            request.setHeader('Authorization', 'Bearer ' + updatedRuntimeToken);
            request.setHeader('Content-Type', 'application/json');
            request.setBody('{}');  // Convert to JSON if inputs are needed
            System.debug(request);
            if (!Test.isRunningTest()) {
                HttpResponse response = http.send(request);
                if (response.getStatusCode() != 200) {
                    System.debug(LoggingLevel.ERROR, 'Error transitioning transaction: ' + response.getStatusCode());
                    System.debug(LoggingLevel.ERROR, response.getBody());
                } else {
                    System.debug('Rejected API Call Failed: ' + response.getStatusCode() + ' - ' + response.getBody());
                }
            } else {
                eachTxn.triggeringRecord.LGK__TransactionUUID__c = 'testUUID';
            }
        }
    }
}

```

XML:

```
<?xml version="1.0" encoding="UTF-8"?>
<Package xmlns="http://soap.sforce.com/2006/04/metadata">
    <types>
        <members>TransactionManagerFlow</members>
        <name>ApexClass</name>
    </types>
    <version>61.0</version>
</Package>
```

Next, if you’re not logged into the org you want to deploy to, you can do so with the `sf org login web` command, which should take you to login.salesforce.com.

When you’ve authorized CLI, the result should resemble the following:

![Script](../images/cpq-txn-mgr-integrate-SF-approvals-apex-code-3.png)

**Note:** If you’re logged into multiple orgs through CLI, use this command to switch:

`sf config set target-org=<username>`

When you’re logged in, execute this command:

`sf project deploy start --manifest manifest/package.xml`

![Deployments](../images/cpq-txn-mgr-integrate-SF-approvals-apex-code-4.png)

Add the Apex Actions, \(look for a name that matches the label parameter in the invocable method\) after the Decision Blocks and make sure your flow looks similar to the one provided in the screenshot.

Finally, Activate the Flow and test.

## Testing

After the record-triggered flow and TM Blueprint are created, you may find this SOQL query helpful for debugging your approvals process in SF.

Receiving Salesforce Approval Status \(getting the state of most recent process\)

-   Connection: Salesforce
-   GET
    -   Additional Path: \{\_endpoint\}/services/data/v61.0/query/? q=SELECT+Id,Status,TargetObjectId+FROM+ProcessInstance+WHERE+TargetObjectId=\{\{sfRecordId\}\}+ORDER+BY+CreatedDate+DESC
    -   SOQL Query

```
SELECT Id, Status, TargetObjectId 
FROM ProcessInstance 
WHERE TargetObjectId-'006bm000002IUI4AAO' -- This is the sf oppy/transaction object  id
ORDER BY CreatedDate DESC
```

