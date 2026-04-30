---
title: Tutorial part 1: Get to know ServiceNow Studio
description: This first section covers navigating around ServiceNow Studio, using the search features, grouping tabs by scope, and filtering the files list by app, file type, recent, and bookmarked.Learn how to use ServiceNow Studio search features.Find and bookmark your applications in the Apps tab in ServiceNow Studio.Find and bookmark files in the File Categories view.Bookmarks provide developers with a way to compile a list of files across application scopes, including global platform features.Recently opened files keeps a record of a developer’s work as they go. Use recent files in combination with bookmarks to navigate back to files quickly and keep the number of open files down to reduce clutter and increase focus.Update files as you work in ServiceNow Studio. Save and close or keep tabs open as you work.View the scope and update set for each application file in the bottom left corner of the file screen. Create new update sets here as needed.
locale: en-US
release: yokohama
product: ServiceNow Studio
classification: servicenow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [ServiceNow Studio tutorial, Exploring ServiceNow Studio, Building applications with ServiceNow Studio, Developing your application, Building applications]
---

# Tutorial part 1: Get to know ServiceNow Studio

This first section covers navigating around ServiceNow Studio, using the search features, grouping tabs by scope, and filtering the files list by app, file type, recent, and bookmarked.

**Parent Topic:**[ServiceNow Studio tutorial](lab-sns-lab-guide.md)

## Use search features in ServiceNow Studio

Learn how to use ServiceNow Studio search features.

### Before you begin

Role required: admin or delegated\_developer

### Procedure

1.  Log into your instance as Elsa Timonen.

2.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

3.  Make ServiceNow Studio a platform favorite by selecting the star next to the module name.

4.  Select the search box.

    You can use the **ctrl + /** \(or **command + /**\) keyboard shortcut to send focus to the search box.

    ![Open the search bar to find files.](../image/sn-studio-reg-search.png)

5.  Enter `employee profile`.

    You can filter the top search results by files, tables, or apps.

6.  Select **Tables**, and open the **Employee profile** table.

    The Employee Profile table definition opens in Table Builder in a new ServiceNow Studio tab.

7.  Reopen the search bar by using the **ctrl + /** \(or **command + /**\) keyboard shortcut.

8.  Enter `Incident`, and open the **Incident** table.

9.  Use the search shortcut again and open the **employee\_profile** script include.

10. View the three open tabs in ServiceNow Studio.

    -   Employee Profile table
    -   Incident table
    -   employee\_profile script include
    ServiceNow Studio has a strong focus on work organization.

11. Group these file tabs by scope by selecting your user profile picture in the top right corner of the screen.

    ![Open the user menu](../image/sn-studio-user-menu.png)

12. Select **Studio Settings**, and turn on the **Group tables by app scope** setting.

    The open files are now grouped by application scope. Each scope is represented by a different color.


## Navigate the Apps view in ServiceNow Studio

Find and bookmark your applications in the Apps tab in ServiceNow Studio.

### Before you begin

Role required: admin or delegated\_developer

### Procedure

1.  Select the **Apps** icon \(![apps icon](../image/sn-studio-apps-icon.png)\).

2.  In the filter box, enter `Employee Profile`.

3.  Using the filter icon \(![filter icon](../image/sn-studio-filter-icon.png)\), select **Store**.

    ![Use the filter to select Store](../image/sn-studio-lab-filter.png)

4.  Select the Employee Profile app to load its files.

5.  Scroll down and select the **Table** category to open it.

6.  Hover over the **Employee Profile** table and select **Add to bookmarks**.

7.  Select the more options icon \(![more options icon](../image/sn-studio-more-options-icon.png)\), and toggle on the **Show parent categories** option.

    This option organizes the file categories into groups with other similar categories. For example, **Table** and **Form** are grouped under the **Data** parent category.

8.  In the filter box, enter `Employee Profile`.

9.  Select the collapse all icon \(![collapse all](../image/sn-studio-collapse-all-icon.png)\).

10. Expand the Server Development category.

11. Locate and bookmark the **Enforce unique user for Employee Profile** business rule.


## Navigate the File Categories view in ServiceNow Studio

Find and bookmark files in the File Categories view.

### Before you begin

Role required: admin or delegated\_developer

### Procedure

1.  Select the **File Categories** icon \(![file categories icon](../image/sn-studio-files-icon.png)\).

    **Note:** In this view, until a category is selected, the filter box will search the name of file categories, not file names or metadata.

2.  In the filter box, enter `flow`.

3.  Under the Automation category, select **Flow**.

    **Note:** All flows across all application scopes are shown.

4.  In the filter navigator, select the back icon \(![back icon](../image/sn-studio-back-icon.png)\).

5.  Clear the filter box and enter `rule`.

6.  Under Server Development, select **Business Rule**.

7.  Select **Open list**.

8.  In the integrated tab that opens, open the list filter and add a new condition: **Table - is - incident**.

    You can use traditional list filtering by opening the file category list view.

    ![Traditional platform filtering is available for you in ServiceNow Studio](../image/sn-studio-tutorial-filtering.png)

9.  Select **Run**.

10. Scroll down and open the **incident autoclose** business rule.

11. Close all open files by selecting the X on each tab.


## Use bookmarks in ServiceNow Studio

Bookmarks provide developers with a way to compile a list of files across application scopes, including global platform features.

### Before you begin

Role required: admin or delegated\_developer

### Procedure

1.  Select the **Bookmarks** tab.

2.  Open the **Employee Profile** table.

3.  Remove the bookmark on the **Enforce unique user for Employee Profile** business rule by hovering over the file and selecting the X.

4.  Confirm the action by selecting **Remove**.


## Open recently used files in ServiceNow Studio

Recently opened files keeps a record of a developer’s work as they go. Use recent files in combination with bookmarks to navigate back to files quickly and keep the number of open files down to reduce clutter and increase focus.

### Before you begin

Role required: admin or delegated\_developer

### Procedure

1.  Select the **Recent** tab.

2.  Find and open the **incident autoclose** and **Enforce unique user for Employee Profile** business rules from the recent files list.


## Change a file in ServiceNow Studio

Update files as you work in ServiceNow Studio. Save and close or keep tabs open as you work.

### Before you begin

Role required: admin or delegated\_developer

### Procedure

1.  Open the **Enforce unique user for Employee Profile** business rule tab.

2.  In the When to run section, select **Insert**.

3.  Attempt to close the **Enforce unique user for Employee Profile** business rule tab.

    **Note:** There is a red dot on the tab indicating that there are unsaved changes to this file.

4.  Select **Close tab** to close the tab without saving your changes.

5.  Select **Cancel** to keep the file open.


## View scope and create a new update set in ServiceNow Studio

View the scope and update set for each application file in the bottom left corner of the file screen. Create new update sets here as needed.

### Before you begin

Role required: admin or delegated\_developer

### Procedure

1.  On the **Enforce unique user for Employee Profile** file, select the **Default** text in the Update Set widget.

2.  Select **New**, and enter `bootcamp` for the name.

3.  Select **Save**.

4.  Select **Apply**.

5.  Save the change you made to the **Enforce unique user for Employee Profile** business rule by selecting **Update**.

6.  Navigate home by selecting the **ServiceNow Studio** icon.

7.  Open the **Deployment** tab.

8.  From the list of update sets, select and open the **Application: Employee Profile** group.

9.  Open the **bootcamp** update set.

10. View the changes to the **Enforce unique user for Employee Profile** file under the **Customer Updates** related list.


