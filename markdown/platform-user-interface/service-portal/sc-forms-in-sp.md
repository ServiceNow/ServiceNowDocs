---
title: Service Catalog forms in Service Portal
description: Service Catalog forms are rendered within Service Portal widgets in a two-column layout. Complex forms may not display as expected.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Supported features in Service Portal, Exploring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Service Catalog forms in Service Portal

Service Catalog forms are rendered within Service Portal widgets in a two-column layout. Complex forms may not display as expected.

## Recommendations when creating Service Catalog forms

Use the following recommendations as a guide to building scalable forms that can be used in both applications:

-   Keep forms simple. Because forms with multiple containers, variable sets, and client scripts do not always display as expected in Service Portal, keep forms short to eliminate conversion and debugging issues.
-   Think in mobile. Any support for Catalog Client Scripts or Catalog UI Policies is the same as in mobile. Review the following resource: [Mobile client GlideForm \(g form\) scripting and migration](https://www.servicenow.com/docs/access?context=r_MobilePlatformMigrationImpacts&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

## Form rendering in Service Portal

Containers and variable sets within Service Catalog forms are translated into a two-column layout when implemented in Service Portal. Service Catalog forms are rendered in Service Portal using the following rules:

-   Only the top-level container settings are honored. If there are other containers within the top-level container, they are rendered as a single column. If there are container splits or nested containers within these additional containers, they are rendered as a single column. A top-level container is not a child of any other container.
-   There can be a maximum of two columns in Service Portal. If your implementation includes forms with more than two columns, the fields are reorganized into two-columns in Service Portal.
-   Variable sets are treated as containers. All previously listed rules apply to variable sets as well as any containers within them.
-   Default variable size is not supported in Service Portal.

For other forms in the platform, the view determines how the form displays in Service Portal. For base system tables, the form opens in the Service Portal using the **Service Portal** Table form views.

## Example layout conversions

The following examples demonstrate how Service Catalog forms display in Service Portal.

-   **Single-column form**

    A Service Catalog form with:

    -   Two containers.
    -   A single-column layout.
    ![Service Catalog form displayed in the Service Catalog.](../image/1.1-SC-form.png "Service Catalog form")

    In Service Portal, the single-column layout renders as expected.

    ![Service Catalog form displayed in the Service Portal. Container 1 and container 2 display vertically.](../image/1.2-SP-form.png "Service Portal result")

-   **Two-column layout with subcontainers**

    A Service Catalog form with:

    -   A container with a two-column layout.
    -   A subcontainer with a single-column layout.
    -   A subcontainer with a two-column layout.
    ![Service Catalog form displayed in the Service Catalog. Container 2 and container 3 are side-by-side. Container 3 has two columns.](../image/3.1-SC-form.png "Service Catalog form")

    In Service Portal, the two-column layout setting of the subcontainer is ignored. The subcontainer renders as a single column.

    ![Service Catalog form displayed in the Service Portal. In container 3, all variables display in a single column.](../image/3.2-SP-form.png "Service Portal result")

-   **Two-column layout with variable sets and subcontainers**

    A Service Catalog form with:

    -   Containers with single-column and two-column layouts.
    -   Variable sets with a two-column layout within containers.
    ![Service Catalog form displayed in the Service Catalog. Variable sets have multiple columns.](../image/4.1-SC-form.png "Service Catalog form")

    In Service Portal, the two-column layout settings of the variable sets are ignored when inside a container column.

    ![Service Catalog form displayed in the Service Portal. Variable sets within containers display as single columns.](../image/4.2-SP-form.png "Service Portal result")

-   **Containers within variable sets**

    A Service Catalog form with:

    -   Variable sets with single-column layouts.
    -   A container with a single-column layout with a container split within a single-column variable set.
    -   A container with a two-column layout within a single-column variable set.
    ![Service Catalog form displayed in the Service Catalog.](../image/5.1-SC-form.png "Service Catalog form")

    In Service Portal, the container split and two-column container settings are ignored when inside a single-column variable set.

    ![Service Catalog form displayed in the Service Portal. All containers and variable sets display in a single column.](../image/5.2-SP-form.png "Service Portal result")

-   **Nested containers**

    A Service Catalog form with:

    -   Containers that contain variable sets.
    -   Variable sets that contain nested containers.
    ![Service Catalog form displayed in the Service Catalog.](../image/6.1-SC-form.png "Service Catalog form")

    In Service Portal, nested container formatting is ignored and displays as a single-column.

    ![Service Catalog form displayed in the Service Portal. All nested containers display in a single column.](../image/6.2-SP-form.png "Service Portal result")


## Render a complex form in Service Portal using an iFrame

Because complex forms do not display as expected in Service Portal, you can render catalog items, record producers, and order guides in Service Portal using an iFrame. This workaround is a temporary solution to enable your Service Portal to function as expected while you simplify any complex Service Catalog forms.

When rendering items in an iFrame in Service Portal, the following limitations apply:

-   On catalog items and record producers, the attachment icon is not visible. As a result, users cannot attach any files during the submission. As a workaround, you can add the attachment button to your form.
-   Click-through for the hover-over icon is not available.
-   Forms are not optimized for a mobile environment.

For more information, see the [Service Catalog on Service Portal](https://www.servicenow.com/community/developer-articles/service-portal-catalog-implementation-guide/ta-p/2329889) post in the ServiceNow Community.

**Note:** Be sure to make changes in a test environment before updating your production instance.

