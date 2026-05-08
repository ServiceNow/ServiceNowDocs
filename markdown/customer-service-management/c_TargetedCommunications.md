---
title: Targeted communications
description: The Targeted Communications application provides the ability to create and send articles and emails to internal and external customers.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Targeted communications

The Targeted Communications application provides the ability to create and send articles and emails to internal and external customers.

Users with the publications author \(sn\_publications.author\) and publications administrator \(sn\_publications.admin\) roles can use the Targeted Communications application to author publication articles and emails for employees, customer contacts and accounts, and consumers. Articles are available for viewing from the self-service portals and can also be sent out as email notifications.

Each publication article includes content and a specified list of recipients. Articles can also include optional email notification. Recipients lists can be created dynamically by using a condition builder to identify the desired conditions, by running scripts, or by manual file upload. Recipients can be added to or removed from a list manually and lists can have both dynamically generated and manually added records of the same type.

When creating an article, publication authors specify a publish date and an expiration date. The system uses these dates to automatically publish and expire the article. Authors can also request a review prior to publishing an article. Articles can include an optional email notification that is sent to all recipients in the recipients list when the article is published. In this email notification, all of the recipients are included in a **bcc** list to maintain privacy.

**Note:** Delegates of recipient list users do not receive published email notifications.

The process of publishing articles is based on workflows and two default workflows are provided: one to publish articles instantly and one that requires approval prior to publishing. Publication administrators can update workflows and add users with the publications approver \(sn\_publications.approver\) role to perform reviews. Both authors and administrators can monitor publications and see which users have received and viewed the information.

Customer contacts and consumers can view publications by logging in to the Customer Service Portal or the Consumer Service Portal and clicking the **Publications** link in the portal header. Employees can view these publications by navigating to **Targeted Communications** &gt; **Publications** in the application navigator.

**Note:** For more info see, [Components installed with additional plugins for Customer Service Management](../reference/inst-wi-cust-serv-addtl-plugins.md)

## Publication article stages

Publication articles progress through several stages which are displayed in a process flow formatter on the Publication form.

|Stage|Definition|
|-----|----------|
|Author|The initial state of the publication creation process.|
|Review|Publications that are waiting for review. A publication cannot be updated when it is in the **Review** stage.|
|Ready To Publish|Publications that have been reviewed and are ready to be published.|
|Published|Publications that that have reached their **Publish Date**.|
|Expired|Publications that have reached their **Expiry Date** or that have been manually expired.|
|Cancelled|Pending publications that have been cancelled.|

States are shown in a process flow formatter at the top of the Publication form. The current state is indicated by a blue underline. States that have been completed are indicated by a blue check mark.

## Publication lists

The Targeted Communications application menu includes several views of publication records.

<table id="table_evg_rns_51"><thead><tr><th>

State

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Active Publications

</td><td>

Includes publications in the following stages:-   Author
-   Review
-   Ready to Publish
-   Published

</td></tr><tr><td>

Draft Publications

</td><td>

Includes publications that have been created and sent for review.

</td></tr><tr><td>

Expired Publications

</td><td>

Includes publications that have reached their **Expiry Date** or have been set to **Expired**.

</td></tr></tbody>
</table>## Targeted communications workflows

Starting with the Zurich release, legacy publication workflows for the Targeted Communications \(com.sn\_publications\) application have been migrated to low code flows in Workflow Studio. The functionality of the flows remains the same.

If customers have customized the legacy workflows, a fix script deactivates the new flows and activates the legacy workflows during instance upgrade.

**Note:** The new flows are only activated if the legacy workflows have not been customized.

For more information, see [Targeted communications publication workflows](../reference/targeted-comm-publication-workflows.md).

