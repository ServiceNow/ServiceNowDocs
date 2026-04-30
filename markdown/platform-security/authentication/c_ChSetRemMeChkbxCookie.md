---
title: Remember me
description: When the Remember me check box is selected at login, a cookie is stored on the user's computer. This cookie automatically authenticates the user upon subsequent visits.You can change the default value of the Remember me check box.You can remove the Remember me check box so users do not have access to this feature.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Local Authentication, Authentication, Access Management]
---

# Remember me

When the **Remember me** check box is selected at login, a cookie is stored on the user's computer. This cookie automatically authenticates the user upon subsequent visits.

If the user logs out, the cookie is destroyed. The default value of the **Remember me** check box is controlled by one property, and whether or not the check box appears on the login page is controlled by a different property.

Two properties, **glide.ui.user\_cookie.life\_span\_in\_days** and **glide.ui.user\_cookie.max\_life\_span\_in\_days** control the glide\_user system generated cookie expiration value. When a user accesses an instance with 'remember me' enabled, the access resets the cookie expiration period until the maximum \(glide.ui.user\_cookie.max\_life\_span\_in\_days\) life span limit is reached.

**Note:** To learn more about these properties, see the following topics in Instance Security Hardening Settings:

-   
-   

## Change the default value of the Remember me check box

You can change the default value of the **Remember me** check box.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **UI Properties**.

2.  Locate the **Default value of "Remember me" checkbox on login page** property \(**glide.ui.remember.me.default**\).

3.  To set the default value of the **Remember me** check box to **No**, clear the property check box.

4.  To restore the default value of the **Remember me** check box to **Yes**, select the property check box.


## Remove the Remember me check box

You can remove the **Remember me** check box so users do not have access to this feature.

### Before you begin

Role required: security\_admin

**Note:** To learn more about this property, see  in Instance Security Hardening Settings.

### Procedure

1.  Elevate your role to security\_admin.

2.  Navigate to **System Properties** &gt; **UI Properties**.

3.  Locate the **Remove "Remember me" checkbox from login page** property \(**glide.ui.forgetme**\).

4.  Select the property check box.

    This setting removes the **Remember me** check box, invalidates existing cookies, and disables Remember me functionality entirely.

5.  To restore the **Remember me** check box to the login page, clear the property check box.


