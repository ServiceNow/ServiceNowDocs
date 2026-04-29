---
title: Create page scripts for Work scheduler
description: Add custom page scripts for the Work scheduler so that you can update the client state through events or update transform workItem object to properties.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create a Work scheduler card using the Next Experience UI Builder, Setting up, Work scheduler, Workforce Optimization for ITSM, IT Service Management]
---

# Create page scripts for Work scheduler

Add custom page scripts for the Work scheduler so that you can update the client state through events or update transform workItem object to properties.

## Before you begin

Role required: workspace\_admin or ui\_builder\_admin​

## About this task

Add the **Handle card clicked** and the **Handle card action clicked** page scripts to handle events that are generated when the card and its actions are clicked.

Add the **Transform workItem to cardProps** page script to transform the **workItem** object in the Work queue to properties for the card components.

**Note:** If you have [customized a Work scheduler card](customize-workscheduler-card-wfo-itsm.md), you can follow the steps below to add client scripts.

## Procedure

1.  Select the Client Scripts icon \(![Client scripts icon](../image/client-scripts-icon.png)\).

2.  Create the **Handle card clicked** page script.

    1.  In the **Page scripts** section, click **+Add**.
    2.  In the **Script name** field, enter **Handle card clicked**.
    3.  In the **Script Includes** section, add the following script:

        ```
        /**
        * @param {params} params
        * @param {api} params.api
        * @param {any} params.event
        * @param {any} params.imports
        * @param {ApiHelpers} params.helpers
        */
        function handler({api, event, helpers, imports}) {
          const {workItem} = api.context.props;
          api.emit('CARD_CLICKED', {workItem});
        }
        ```

3.  Create the **Handle card action clicked** page script.

    1.  In the **Page scripts** section, click **+Add**.
    2.  In the **Script name** field, enter **Handle card action clicked**.
    3.  In the **Script Includes** section, add the following script:

        ```
        /**
        * @param {params} params
        * @param {api} params.api
        * @param {any} params.event
        * @param {any} params.imports
        * @param {ApiHelpers} params.helpers
        */
        function handler({api, event, helpers, imports}) {
          const {workItem} = api.context.props;
          const {action: actionItem} = event.payload;
          api.emit('CARD_ACTION_CLICKED', {workItem, actionItem});
        }
        
        ```

4.  Create the **Transform workItem to cardProps** page script and attach the **WorkSchedulerUIBCardUtils** script include.

    1.  In the **Page scripts** section, click **+Add**.
    2.  In the **Script name** field, enter **Transform workItem to cardProp**.
    3.  In the script editor, add the following script:

        ```
        /**
        * @param {params} params
        * @param {api} params.api
        * @param {any} params.event
        * @param {any} params.imports
        * @param {ApiHelpers} params.helpers
        */
        async function handler({api, event, helpers, imports}) {
            const {workItem} = api.context.props;
            const {mappingFields, recordFields} = workItem;
            const cardUtils = imports['sn_wfo_work_sched.WorkSchedulerUIBCardUtils']();
            const fallbackValueLabel = await helpers.translate('<not defined>');
            const dropdownItems = workItem.tableMetadata.canDelete
                ? [{id: 'delete', label: await helpers.translate('Delete')}]
                : [];
            // Fields for getContent() and getAria()
            const contentFields = [{
                name: 'assigned_to',
                label: await helpers.translate('Assigned to')
            },
            {
                name: 'assignment_group',
                label: await helpers.translate('Assignment group')
            },
            {
                name: 'start_date',
                label: await helpers.translate('Start date')
            },
            {
                name: 'end_date',
                label: await helpers.translate('End date')
            }];
            // Create cardProps
            const cardProps = {};
            cardProps.tagline = {
                label: workItem.recordFields._row_data.displayValue || null
            };
            cardProps.heading = {
                label: mappingFields.description ? mappingFields.description.displayValue : fallbackValueLabel
            };
            cardProps.dropdowns = dropdownItems.length > 0
                ? [{id: 'dropdown1', items: dropdownItems, icon: 'ellipsis-v-outline'}]
                : [];
            cardProps.content = await cardUtils.getContent(helpers, contentFields, workItem, null, null, true);
            cardProps.aria = await cardUtils.getAria(helpers, contentFields, workItem, null, true);
            cardProps.assignedTo = mappingFields.assigned_to ? mappingFields.assigned_to.displayValue : null;
            api.setState('cardProps', cardProps);
        }
        ```

    To customize the display of the fields, refer to [https://developer.servicenow.com/dev.do\#!/reference/next-experience/utah/now-components/now-label-value-stacked/overview](https://developer.servicenow.com/dev.do#!/reference/next-experience/utah/now-components/now-label-value-stacked/overview).

5.  Click **Save**.

    Here's a demo on how to create page scripts for Work scheduler.Create page scripts


## What to do next

[Define the workItem property in the Work scheduler page configuration](work-sched-create-page-properties.md)

**Parent Topic:**[Create a Work scheduler card using the Next Experience UI Builder](create-workscheduler-card-wfo-itsm.md)

**Previous topic:**[Create a client state parameter for Work scheduler](work-sched-create-client-state-params.md)

**Next topic:**[Define the workItem property in the Work scheduler page configuration](work-sched-create-page-properties.md)

**Related topics**  


[Define and bind client scripts to components](https://www.servicenow.com/docs/access?context=define-client-scripts&version=australia&pubname=australia-application-development&ft:locale=en-US)

