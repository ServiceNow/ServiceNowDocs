---
title: Working with forms in Creator Studio
description: To add items or services to your catalog, you must create a different form for each thing being requested.
locale: en-US
release: zurich
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 9
keywords: [request form, catalog item]
breadcrumb: [Build apps, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Working with forms in Creator Studio

To add items or services to your catalog, you must create a different form for each thing being requested.

**Summary:** After reading this topic, you’ll understand:

-   How form templates get you started creating your own [forms](creator-studio-glossary.md#).
-   How to customize the layout and questions on your forms.
-   How to make a form \(AKA catalog item\) appear in your app.
-   How to make a form stop appearing in your app.

## What is a form?

A form is a list of questions that people answer to make a request. They might ask for a keyboard, a laptop, or permission to take a vacation. The answers to those questions provide the fulfiller with all the information that they need to fulfill the request. For example, if someone asks for a laptop, the fulfiller might need to know the size, the model number, the operating system, and so forth.

In addition to questions, forms can contain images, headings, and text descriptions to explain the questions.

You’ll need a different form for every type of item or request that a requester can ask for. Why? Because the questions you must ask for a keyboard differ from the questions that you must ask to give a requester permission to take a vacation. So, there’s one form for each type of request that people can make. You can think of a form as representing a catalog item.

Your app will likely have multiple forms, meaning multiple things the requester can ask for. We call a collection of forms a catalog of items.

**Key terms:**

-   **Item**

    Something a requester can ask for. Each item requires its own form.

-   **Catalog**

    A collection of items that represent all the items a requester can ask for.


## Some examples of catalogs and items

The following table shows three catalogs. The final column shows the names of the items in each catalog. If you have three items, you’ll need three forms.

<table id="table_csz_nnz_t2c"><thead><tr><th>

Service catalog

</th><th>

Example app

</th><th>

Sample catalog items

</th></tr></thead><tbody><tr><td>

HR self-service

</td><td>

Human Resources global people portal app

</td><td>

-   Benefits coverage question
-   Time off request
-   Change of address needed

</td></tr><tr><td>

Branding resources

</td><td>

Marketing and branding app

</td><td>

-   PowerPoint templates
-   Approved Zoom backgrounds
-   Logo files

</td></tr><tr><td>

IT fulfillment

</td><td>

Hardware request app

</td><td>

-   Mouse device
-   Headset
-   Replacement charging cable

</td></tr></tbody>
</table>## Let Creator Studio give you a head start

When you choose a template to start creating your form, Creator Studio builds a form with questions you might like to use. The questions and their layout make up the form.

**Key term:**

-   **Form template**

    A set of questions arranged on a form provided by Creator Studio.


The form template that Creator Studio provides is called the Creator Studio Default Template. It contains three questions to get you started. You can customize, add, and subtract questions on your form.

**Note:** You can create a form using Now Assist. To learn more, see [Generating forms with Now Assist](creator-studio-text-to-form.md).

Your administrator can delete the default template, create additional form templates, and restrict who can fill out the forms. If you're an administrator, you can read more about this topic in [Creating catalog templates for use in Creator Studio apps](creator-studio-creating-catalog-templates.md).

To store the forms that requesters fill out, Creator Studio creates a table by default. One row represents one filled-out form.

**Note:** Your application can contain as many forms as you need.

When you create a form, Creator Studio uses the app's request table to hold the submitted answers for each form. All requests from all of an app's forms are stored in the same table.

## Types of questions you can ask

You get to pick the questions to ask requesters. Creator Studio provides two types of questions you can ask:

-   **General questions** are where you give requesters an empty box to write a short answer \(think name or email\) or a list of choices to pick from \(like a dropdown menu or those little circles you fill in\).
-   **Reference-based questions** are where you provide a list of choices that you define in a table.

You can add questions to forms that have been preconfigured by your admin, and can't be edited. Adding a **Question set** element to a form enables you to select from the curated options.

You can make forms change based on how users answer questions in several ways:

-   Forms can automatically update how questions appear \(or are hidden\) based on how users answer a them. We call this [dynamic behavior](creator-studio-glossary.md#). For example, if a user says they want a T-shirt for an event they're attending, you can make a **T-shirt size** field required.
-   Forms can automatically populate answers based on answers to record choice questions. For example, a form can enable someone to select a user for the **Choose the gift box recipient** field, which retrieves its values from the User table. An additional **Preferred name** field can be automatically populated from the **First name** field of the User table selection, but then edited if someone prefers a nickname.

## Laying out the questions

Creator Studio provides an initial layout for its default form. You can use columns, images, divider lines, and more to customize the layout of the questions on the forms. There are two procedures that you can use to customize a form:

-   Changing the questions – Change the number of questions, what they’re asking, and adjust where questions appear on a form. Find information on changing questions in [Customize your form for an app in Creator Studio](../task/creator-studio-edit-form.md).

    ![Select a question to edit its details](../image/crs-edit-questions-nav.png "Editing a question on a form")

-   Changing the look and feel of the form – Add pictures, write some text to explain the questions, and even move them around to make them flow smoothly. You can read about that in [Change the layout of an app's record in Creator Studio](../task/creator-studio-work-with-record-details.md).

    ![Change the appearance of the form by changing text and images](../image/crs-form-component-style.png "Edit the look and feel of the app's tile")


## Where can I see forms?

After deployment, your app lives as forms in the Service Catalog and categories you specified when creating the forms.

Users can access those forms directly in a Service Catalog, as well as Service Portal and an Employee Center.

If you associate the app's form with one or more topics, the form will appear in the relevant, dynamically created topic pages in Employee Center. Find out more about topics in [Associate a catalog item with a taxonomy topic in Employee Center](https://www.servicenow.com/docs/access?context=associate-cat-item-taxonomy-ec&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US), and more about taxonomy, which is a categorization method, in [Unified Taxonomy for Employee Center](https://www.servicenow.com/docs/access?context=config-taxonomy&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

**Note:** If you want to check out what a form looks like and test submitting responses to it, you can try it out after it's been published. When you try a form, you submit answers, which trigger any associated automations. For more information, see [Test one of your forms for an app](../task/creator-studio-try-it.md).

## Making forms available for an app

Forms have two states:

-   Draft
-   Published

Keeping forms in a Draft state lets you work on them until you’re finished. When you’re pleased with the form, publish it by selecting the **Mark as ready** button. Only then will it appear in your application \(assuming your app has been deployed\).

A published form appears as an item in your catalog of offerings. For example, your site might enable requesters to ask for computers, mice, monitors, keyboards, technical support, and so forth. Each item requires a different form, and appears as a different catalog item in your app.

**Key terms:** Don’t confuse deploying your app with publishing a form.

-   Publishing a form means that the form will appear as a catalog item only after your app is deployed. That’s why the button label is **Mark as ready**.
-   Deploying an app is what system admins do to make your app available for people to use.

-   **[Add a form to an app in Creator Studio](../task/creator-studio-add-form.md)**  
Add a form to the app you just created. Forms contain questions that people respond to when submitting a service desk request.
-   **[Customize your form for an app in Creator Studio](../task/creator-studio-edit-form.md)**  
Forms help people ask for things they need, such as a new keyboard or permission to take time off. The default form that's added when you create an app in Creator Studio needs some changes to fit your needs. For example, you must add question labels to gather information about the request.
-   **[Generating forms with Now Assist](creator-studio-text-to-form.md)**  
Learn how the Now Assist in Creator application helps you to create forms for you in Creator Studio.
-   **[Make a form change based on responses in Creator Studio](../task/creator-studio-dynamic-behavior.md)**  
Make a form update based on how users answer a question using dynamic behavior. For example, if a user says they want a T-shirt for an event they're attending, you can make a **T-shirt size** field required.
-   **[Development states of a form in Creator Studio](creator-studio-catalog-item-states.md)**  
Think of your app as an online store that contains a catalog of items. To request something, a person needs to fill out a form. It’s your job to create and customize forms for every item in your catalog using Creator Studio.
-   **[Add more forms to an app in Creator Studio](../task/creator-studio-add-another-form.md)**  
Add as many forms as you need to create catalog items for your app. For example, you could have an office booking app with three different forms: one for requesting parking spaces, one for requesting a desk, and one for reserving conference rooms.
-   **[Edit the settings for a form in Creator Studio](../task/creator-studio-edit-form-settings.md)**  
Edit form settings if you need to change its basic attributes, such as its associated image or attachments are allowed.
-   **[Publish a form for your app in Creator Studio](../task/creator-studio-publish-form.md)**  
Publishing forms once they're ready makes them available as catalog items in the production instance for published apps.
-   **[Working with published forms](crs-working-with-published-forms.md)**  
After a form has been published, you can update it, undo changes, and hide it from being visible.
-   **[Deleting forms and questions in Creator Studio](creator-studio-delete-forms-questions.md)**  
Deleting unpublished forms and questions from Creator Studio removes them completely from the ServiceNow AI Platform.

**Parent Topic:**[Building apps with Creator Studio](building-apps-with-creator-studio.md)

