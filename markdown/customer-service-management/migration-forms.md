---
title: Forms
description: Learn how the CSM Agent Workspace form functions with CSM Configurable Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/migration-forms.html
release: australia
topic_type: concept
last_updated: "2026-10-25"
reading_time_minutes: 1
breadcrumb: [Migrate to CSM Configurable Workspace, Migrating to CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Forms

Learn how the CSM Agent Workspace form functions with CSM Configurable Workspace.

The form is the user interface where agents do most of their work. CSM Agent Workspace form configurations work without modification in CSM Configurable Workspace, but the configurations may affect the functioning of your CSM Configurable Workspace.

The form is where agents open, update, and close cases and interactions. If form components aren't set up correctly, agents may see missing actions, activity streams, or headers when they open records in CSM Configurable Workspace.

## Form parameters

Form mapping doesn't directly correspond between CSM Agent Workspace form components and CSM Configurable Workspace form components. CSM Agent Workspace components are hard-coded with the form and incorporate everything on the form including the form header, UI action bar, Activity stream, the sidebar, etc. In CSM Configurable Workspace, these features are separate components.

## Verify form components after migration

Because each of these features is configured separately in UI Builder, open a case record in CSM Configurable Workspace and confirm that each one appears correctly. Repeat the check for interaction records and any other record types that your agents use regularly.

1.  The form header appears at the top of the record with the correct fields. If it's missing, see [Form headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migration-form-headers.md).
2.  UI action buttons appear on the form. If they're missing, see [UI Action Bar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migration-form-ui-actions.md).
3.  The activity stream appears, and agents can post work notes and communicate with customers. If it's missing, see [Activity stream](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migration-activity-stream.md).
4.  The contextual sidebar opens when agents select a record tab. If it's missing, see [Migrate the contextual side panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/migration-contextual-side-panel.md).

