---
title: Development states of a form in Creator Studio
description: Think of your app as an online store that contains a catalog of items. To request something, a person needs to fill out a form. It’s your job to create and customize forms for every item in your catalog using Creator Studio.
locale: en-US
release: yokohama
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Working with forms in Creator Studio, Building apps with Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Development states of a form in Creator Studio

Think of your app as an online store that contains a catalog of items. To request something, a person needs to fill out a form. It’s your job to create and customize forms for every item in your catalog using Creator Studio.

**Summary:** Forms have two states:

-   **Draft**

    The state of a form when you’re editing it. It can be a new form or a copy of a published form. Forms in this state do not appear in your catalog.

-   **Published**

    The state of a fully-designed form that appears in your catalog.


You want to publish forms only when they’re ready—not some half-baked version you’re working on. That’s why forms have states.

## Draft state for forms

Forms in the Draft state don't appear in your catalog of items. That means you can work on them without affecting your online catalog.

The forms you edit can be new, or copies of forms that have already been published. You can revise forms as much as you like in this state, but the revisions are kept behind the scenes until you publish the form. So, no worries about leaving a form unfinished when it’s in Draft state!

## Published state for forms

When you finish editing a form, you mark it as ready, which puts it in the Published state. This version of the form then appears in its specified catalog of items.

**Note:** The published form appears only on the non-production instance where you're developing your app. You must request that your admin deploy the app to production for the form to appear in the catalog on the production instance.

If you edit a form that’s been published, Creator Studio creates a copy of the form, and puts the copy in the Draft state so you can work on it. The published version of the form remains available in your online catalog until you submit the revised copy of the form, which will replace the published form.

**Parent Topic:**[Working with forms in Creator Studio](creator-studio-work-with-forms.md)

