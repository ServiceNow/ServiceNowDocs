---
title: Create a search configuration
description: Create a search configuration. This record connects your launcher screen with the other records used to configure search.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-12-16"
reading_time_minutes: 3
breadcrumb: [Configure search criteria, Global search for mobile, Launcher screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Create a search configuration

Create a search configuration. This record connects your launcher screen with the other records used to configure search.

## Before you begin

Role required: admin

## Procedure

1.  In the filter navigator, enter `sys_sg_global_search.list`.

2.  Click **New**.

3.  In the search configuration form, fill in the fields:

<table id="table_y5g_fv2_mkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for your search configuration.

</td></tr><tr><td>

Application

</td><td>

The scoped application for the search configuration. This field is ready only and automatically contains the name of the current application.

</td></tr><tr><td>

Placeholder

</td><td>

Text that appears in the search bar before a user enters any text.

</td></tr><tr><td>

Search Application Configuration

</td><td>

Search application configuration record used for this search configuration.**Note:** Leave this field empty. You create a search application configuration record in the following steps.

</td></tr><tr><td>

Interleave Result

</td><td>

Whether search results are interleaved. Deselect this option to display search results separated by search source.

</td></tr><tr><td>

Enable Photo Search

</td><td>

Whether photo search is available for your search bar. If the **glide.sg.image\_recognition.search.enable** system property is false, you cannot select this option. For details on this property see [Create the image search system property](sg-image-search-prop.md).

</td></tr></tbody>
</table>4.  In the **Search Application Configuration** field, click the reference icon \(![Reference icon](../image/reference-lookup-icon.png)\).

5.  In the search application configuration list, click **New**.

6.  In the Search Application Configuration form, fill in the fields. The fields displayed will change based on which search engine you choose.

    If AI Search is selected:

    |Field|Description|
    |-----|-----------|
    |Name|Name for you search application configuration.|
    |Search Engine|The search engine for this search application configuration.|
    |Search Profile|The search profile to configure.|
    |Search Results Limit|Limit for the initial results returned in the search. Scrolling down with load additional results in increments defined by this value. This field has a default value of 10.|
    |Genius Results Limit|Limit for the number of Genius Result cards included with search results.|
    |Enable Typo Handling|Enable auto-correction for the search configuration.|

    **Note:** In order to return the specific record in the search results in mobile, the entity can be added to **Search sources** in the Search Application Configuration.

    If Zing is selected:

    |Field|Description|
    |-----|-----------|
    |Name|Name for your search application configuration.|
    |Search Engine|The search engine for this search application configuration.|
    |Application|The scoped application for the search configuration. This field is ready only and automatically contains the name of the current application.|
    |Search Results Limit|Limit for the initial results returned in the search. Scrolling down with load additional results in increments defined by this value. This field has a default value of 10.|
    |Suggestions limit|Limit for search suggestions listed for the search. This field has a default value of 10.|

7.  Right-click the header of the Search Application Configuration form, and click **Save**.

    The Search Application Configuration record saves. After the save, the Application Search Sources related list appears on the form.

8.  In the Application Search Sources related list, click **New**.

9.  In the **Source** field of the Application Search Sources form, select a search source you created in the previous steps.

10. In the **Order** field, add a value to determine the order in which the search source facets appear in the search results.

    **Note:** Search sources display from the lowest order to the highest.

    A search application configuration with an associated search source. ![Example search application configuration with an associated search source](../image/scc-example.png)

11. Repeat steps 8 through 10 to add additional search sources if you created them in previous steps.

12. Click **Submit**.

13. Right-click the header of the search configuration form, and click **Save**.

14. In the **Global Search M2M Item Configuration** list, click **New**.

15. In the Global Search M2M Item Configuration form, click the reference icon \(![Reference icon](../image/reference-lookup-icon.png)\) next to the **Item Configuration** field.

16. Select the item configuration you want to use for a table that contains your desired search results.

    For example, if you want your search to return problem records, select the item configuration that has **problem** in its **Table** field.

    ![Item configuration records filtered for the problem table](../image/master-item-selection.png)

17. On the Global Search M2M Item Configuration form, click **Submit**.

18. Repeat steps 9–12 to add item configurations for additional record types if you plan to include multiple tables in your search.

19. Click **Save** when you have finished adding item configurations.


**Parent Topic:**[Configure search criteria](../concept/sg-create-custom-search.md)

