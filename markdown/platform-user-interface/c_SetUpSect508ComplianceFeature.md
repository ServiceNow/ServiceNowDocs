---
title: Enabling accessibility features
description: You can configure accessibility features globally or for specific users. Users can also individually enable user preferences for themselves to meet their specific accessibility needs.Enable accessibility mode on your instance.In Core UI, administrators can enable the Contrast UI theme for users who need a greater contrast in color.When a form loads, the system automatically sends focus to the first field on the form. For accessibility reasons, you can disable this option so that focus starts on the first element on the top of the page.The accessible tooltips user preference adds a tooltip icon that users can tab to, to view a tooltip for a field.The NVDA Assistive Technology screen reader is a 32-bit application that, when the Java Access bridge has been enabled, reads aloud Java applications built to support accessibility. If you encounter a problem using NVDA to access Java applications on a 64-bit Windows host, you must configure the Java Access bridge.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Enabling accessibility features

You can configure accessibility features globally or for specific users. Users can also individually enable user preferences for themselves to meet their specific accessibility needs.

The platform includes features that support Web Content Accessibility Guidelines \(WCAG\) 2.0 AA and WCAG 2.1 AA \(for some products\) to make the interface more accessible to all users. These features improve the user experience when accessing the instance with screen readers and keyboard navigation.

Accessibility features are not enabled by default because some features are user specific. Administrators have the flexibility to enable features globally or for individual users.

All of these options can be configured globally or for specific users.

-   Enable the accessibility option.
-   Enable the high contrast theme.
-   Use skip links.
-   Turn off first field focus

**Parent Topic:**[User interface configuration](../../core-configuration/concept/p_NavigationAndUIConfiguration.md)

## Enable accessibility mode

Enable accessibility mode on your instance.

### Before you begin

Role required: none

### About this task

Administrators can enable accessibility mode for specific users by navigating to **User Administration** &gt; **User Preferences** and searching for the `glide.ui.accessibility` user preference. For more information on configuring user preferences, see [User preferences](../../navigation-and-ui/concept/c_UserPreferences.md).

### Procedure

1.  Navigate to **User Administration** &gt; **User Preferences**.

2.  Click the gear icon \(![Gear icon](../../navigation-and-ui/image/IconUI16Gear.png)\) in the banner frame to open the System Settings window.

3.  From the General tab, select the **Accessibility enabled** option.

    Accessible tooltips on forms is enabled automatically the first time you enable accessibility mode.


### What to do next

Alternatively, enable accessibility mode using the Enable Accessibility skip link. For more information on skip links, see [Use skip links](keyboard-accessibility.md#).

![Enable accessibility skip link, which is the first focusable element on the page.](../image/EnableAccessibiltySkipLink.png "Enable accessibility skip link")

## Enable the high contrast theme

In Core UI, administrators can enable the Contrast UI theme for users who need a greater contrast in color.

### Before you begin

Role required: admin

### About this task

Individual users can enable the contrast theme for themselves by navigating to the Theme tab of the [system settings](../../navigation-and-ui/reference/r_UI16BannerFrame.md) menu. From the Theme tab, select the **Contrast UI** theme.

### Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **User preferences**.

2.  Click **New** then configure the following fields.

    |Field|Description|
    |-----|-----------|
    |Name|glide.css.theme.ui16|
    |System|Make sure that the check box is cleared.|
    |User|Name of the user you want to enable the contrast UI theme for. Add a user preference for each user you want to enable the theme for.|
    |Type|string|
    |Value|The sys\_id of the contrast UI theme. You can find the sys\_id by navigating to **System UI** &gt; **Themes**. Then right-click **Contrast UI** and click **Copy sys\_id**.|

3.  Click **Submit**.

    The user may have to sign out and sign back in for the theme to take effect.


## Turn off first field focus

When a form loads, the system automatically sends focus to the first field on the form. For accessibility reasons, you can disable this option so that focus starts on the first element on the top of the page.

### Before you begin

Role required: admin

### About this task

Sending focus to the first field on a form is useful to most users however, it presents challenges for users with certain disabilities. For example, a user using the system with a screen reader may not realize there is additional content above the field that receives focus.

### Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **UI Properties**.

2.  Locate the **On form load, focus on first writable element.** **\(glide.ui.focus\_first\_element\)** property.

3.  Clear the checkbox to turn off first field focus.

    **Note:** If your instance has list v3 enabled, instead navigate to **All** &gt; **User Administration** &gt; **User Preferences** instead and update the **glide.ui.accessibility.focus\_first\_field** property to false.


## Enable the accessible form tooltips feature

The accessible tooltips user preference adds a tooltip icon that users can tab to, to view a tooltip for a field.

### Before you begin

Role required: admin

### About this task

Some fields on forms have associated tooltips that contain additional information. By default, these tooltips are accessible by pointing to the field label or mandatory indicator asterisk. However, a user who relies on keyboard navigation cannot point to the field to access the tooltip. The accessible form tooltip feature solves this problem by adding a keyboard-accessible icon next to each field that has a tooltip. Tabbing or pointing to the icon shows the tooltip.

Administrators can enable accessible form tooltips for specific users by navigating to **User Administration** &gt; **User Preferences** and searching for the `glide.ui.accessibility.accessible.tooltips` user preference. For more information on configuring user preferences, see [User preferences](../../navigation-and-ui/concept/c_UserPreferences.md).

Accessibility must be enabled for the accessible form tooltips user preference to work.

### Procedure

1.  Click the gear icon \(![Gear icon](../../navigation-and-ui/image/IconUI16Gear.png)\) in the banner frame to open the System Settings window.

2.  From the General tab, select the **Accessibility enabled** option.

    The Accessible tooltips on forms option is enabled automatically the first time you enable accessibility mode.

3.  Clear the **Accessible tooltips on forms** option to disable the accessible tooltips.

    If you disable accessibility mode and re-enable it, Accessible tooltips on forms will remain disabled.


## Configure a Windows 64-bit host to use 32-bit NVDA with Java applications

The NVDA Assistive Technology screen reader is a 32-bit application that, when the Java Access bridge has been enabled, reads aloud Java applications built to support accessibility. If you encounter a problem using NVDA to access Java applications on a 64-bit Windows host, you must configure the Java Access bridge.

### Before you begin

Role required: local or domain administrator on the host Windows machine

### About this task

The following example assumes:

-   The 32-bit and 64-bit Oracle Java jdk versions 8u171 are being installed in the default location.
-   A Windows command prompt with administrative privileges is used to execute command line utilities.
-   Executable statements are prefixed with the `PROMPT>` string.

**Note:**

-   This configuration was used on a Windows 7 VM host to test the NVDA and JAWS screen readers.
-   This example refers to Java version 8u171. If you are using a later version of Java, substitute that version.

### Procedure

1.  On the [Oracle Java SE downloads page](http://www.oracle.com/technetwork/java/javase/downloads/index.html), download the Oracle Java jdk for 32-bit and 64-bit Windows environments.

    -   32-bit: `jdk-8u171-windows-i586.exe`
    -   64-bit: `jdk-8u171-windows-x64.exe`
    To access and download the files listed in the above example, go to the [Oracle Java SE jdk download page](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html).

2.  Install the 64-bit version of the Oracle Java jdk in the default location.

    ```
    PROMPT> jdk-8u171-windows-x64.exe
    ```

    Verify that the installation process installed the following:

    -   Java 64-bit jdk in the `C:\Program Files\Java\jdk1.8.0_171` directory.
    -   `WindowsAccessBridge-64.dll` in the `C:\Windows\System32` directory.
3.  Enable the Java Access bridge for 64-bit applications using the 64-bit jabswitch application located in the 64-bit Java jdk bin directory.

    ```
    PROMPT> cd "C:\Program Files\Java\jdk1.8.0_171\bin"
    PROMPT> jabswitch -enable
    ```

4.  Copy the `WindowsAccessBridge-64.dll` located in the `C:\Windows\System32` directory to the 32-bit `C:\Windows\SysWOW64` directory.

    ```
    PROMPT> cd C:\Windows\System32
    PROMPT> copy WindowsAccessBridge-64.dll C:\Windows\SysWOW64
    ```

    Verify that the copied `WindowsAccessBridge-64.dll` exists in the 32-bit `C:\Windows\SysWOW64` directory.

5.  Install the 32-bit version of the Oracle Java jdk in the default location.

    ```
    PROMPT> jdk-8u171-windows-i586.exe
    ```

    Verify that the installation process installed the following:

    -   Java 32-bit jdk in the `C:\Program Files (x86)\Java\jdk1.8.0_171` directory.
    -   `WindowsAccessBridge-32.dll` in the `C:\Windows\SysWOW64` directory.
6.  Enable the Java Access bridge for 32-bit applications using the 32-bit jabswitch application located in the 32-bit Java jdk bin directory.

    ```
    PROMPT> cd "C:\Program Files (x86)\Java\jdk1.8.0_171\bin"
    PROMPT> jabswitch -enable
    ```

7.  Restart the NVDA Assistive Technology software through the task bar or the NVDA menu.

    -   Select the NVDA shortcut pinned to the task bar, pinned to the start menu, or located on the desktop.
    -   Navigate to the **Start** &gt; **All Programs** &gt; **NVDA** &gt; **NVDA** menu selection.
8.  On an administrative command prompt terminal, launch the Edge Encryption Interactive Installer.

    ```
    PROMPT> java -jar <edge encryption interactive file name>.jar
    ```


