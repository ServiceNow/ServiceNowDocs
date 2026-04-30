---
title: Mobile hierarchy
description: Learn the components of ServiceNow mobile and how they work together to assist you in configuring, modifying, and creating applications.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Building mobile apps, Mobile Platform]
---

# Mobile hierarchy

Learn the components of ServiceNow® mobile and how they work together to assist you in configuring, modifying, and creating applications.

## Components of the ServiceNow mobile framework

This image represents the structure of the ServiceNow mobile framework. The next sections detail specific areas of the overall hierarchy, and descriptions of individual components.

![Diagram showing the foundation elements of mobile apps.](../image/mobile-app-core-foundation.png)

## Mobile App Configuration

![Components of the Native Client.](../image/mobile-hierarchy-callout-1.png)

-   **Mobile app**

    A part of the ServiceNow® Mobile Platform, there are 2 mobile apps: the Now Mobile app and the Mobile Agent app. Each app focuses on a persona, which means the app experiences are tailored to support the tasks of specific roles in your organization. Each mobile app can have one or more mobile app configurations. For more information, see the following "Mobile app config" section.

-   **Mobile app config**

    When users download a ServiceNow Mobile Platform application, they are prompted to log in with their credentials. When a user logs in to the instance, they are presented an experience that is created by a single mobile app config. The mobile app config that defines the user's experience depends on conditions defined in the config.

-   **Navigation bar**

    Each mobile app config has a navigation bar that appears at the bottom of the screen. A navigation bar can have up to five icons, called navigation bar tabs. By default, navigation bars have a notification and settings navigation bar tab. For information about how to create a navigation bar, see [Configure the navigation bar and navigation tabs](../task/config-sg-application-menu.md).

-   **Navigation bar tabs**

    Each tab in the navigation bar represents a screen or launcher screen. When you add more than five tabs to the navigation bar, a **More** tab appears. Tapping the **More** tab opens a list view showing additional tabs.

    For information on how to create navigation bar tabs, see [Configure the navigation bar and navigation tabs](../task/config-sg-application-menu.md).

-   **Launcher screens**

    Launcher screens serve as landing pages or home pages for your users. Launcher screens contain a configurable header, and sections to provide access to screens in several formats. You can also configure launcher screens with a search bar and quick actions, which give your users access to commonly used functions.

    For more detail on launcher screens, see [Launcher screens](sg-mobile-applet-launcher.md).

-   **Screens**

    Screens provide your users a method to view and modify data on your instance. Screens can display information as lists, maps, records, and other formats. You can find more detail on screen components in the next section.


## Screens

![List of all available mobile screens.](../image/mobile-screens.png "List of all available mobile screens")

-   **Screen segments**

    Screens contain one or more screen segments, which display information from your instances to your users. Screen segments represent the lists, calendars, maps, and records your users see within the app. If a screen has more than one screen segment, your users can switch between screen segments using a tabbed interface.

    Screen segment records for lists, calendars, and maps are located on the screen segment \[sys\_sg\_item\_stream\_segment\] table. Screen segment records for record screens are on the record screen segment \[sys\_sg\_form\_segment\] table.

-   **Icons**

    Each screen has an icon. This icon represents the screen when it is displayed in a launcher screen or the navigation bar.

    Icon records are located on the Icons \[sys\_sg\_icon\] table.

    For more information on icons, see [Mobile icons](../reference/sg-mobile-icon.md).

-   **Item streams**

    An item stream is the source for the data shown in your screen. An item stream gets its data from a single source, called a data item. You can associate more than one item stream to a screen segment to include data from multiple tables. For example, you could create two item streams to display items from both the incident \[incident\] and request item \[sc\_req\_item\] tables in a single list.

    Item streams are also associated with one or more item configurations. These item configurations provide a pattern controlling how the data appears in your screen segment.

    Item stream records are located in the item stream \[sys\_sg\_item\_stream\] table.

-   **Data items**

    Data items provide the data presented in a screen. A data item is a dataset correlated with a table in an instance. A data item can include a filter condition to restrict what data the item returns. Associate data items with screens so that the screens can transform the dataset into human-readable information.

    Data items are located on the data items \[sys\_sg\_data\_item\] table.

    For more detail on data items, see [Data items](sg-data-item.md).

-   **Item configurations**

    Item configurations provide a pattern for data in your screen, and control how your data appears within a screen segment. For more detail on how an item configuration controls the appearance of your data, see the item configuration section.

    Item configurations are located on the item configuration \[sys\_sg\_master\_item\] table.

-   **More information**

    For more information, See:


## Screen segments

![A hierarchical diagram of the available mobile launcher screens.](../image/mobile-launcher-screens.png)

-   **Screens**

    Screen types determine what a screen looks like and how your users are able to interact with it. You can create these screen types:

    -   [Calendar](calendar-screen.md)
    -   [Chart](chart-screen.md)
    -   [Form](form-screen.md)
    -   [Grouped list](grouped-list-screen.md)
    -   [List](list-screen.md)
    -   [Map](map-screen.md)
    -   [URL](url-screen.md)
    In addition to these types, you can add the following screens to segments in your record screen:

    -   Details screen
    -   Activity stream screen
    -   Related list screen
    -   Embedded list screen
-   **Functions**

    Your users can use functions to perform tasks in the mobile app such as assigning a task, or navigating between records. Actions can also interact with your mobile device to send emails, navigate using map software, or make a phone call.

    Functions are located on the Function \[sys\_sg\_button\] table.

    For more information on functions, see [Mobile functions](sg-studio-mobile-button-types.md).


