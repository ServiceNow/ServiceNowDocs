---
title: Enforce Strict User Image Upload
description: Use the glide.security.strict.user\_image\_upload property to enable Access Control for the upload/update of a profile picture when performed on a user record.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce Strict User Image Upload

Use the **glide.security.strict.user\_image\_upload** property to enable Access Control for the upload/update of a profile picture when performed on a user record.

This setting opens the possibility of an unauthorized user uploading an image to another user's profile.

-   When you set this property to **true**, the table ACLs are enforced when uploading photos, only allowing authorized users to upload an image.
-   When you set it to **false**, ACLs are not enforced on image uploads to the Photo field.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.security.strict.user\_image\_upload**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Access control](sc-access-control.md)|
|Purpose|To restrict uploading of user image only to authorized users.|
|Recommended value|true|
|Security risk rating|3.7|
|Functional impact|No functionality impact as authorized users are still able to upload images to their user profile.|
|Security risk|\(Low\) When you set this property to **false**, an authenticated user could upload an image to another user's account without authorization.|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Access control](sc-access-control.md)

