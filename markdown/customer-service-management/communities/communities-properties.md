---
title: Properties installed with Communities
description: Community administrators can use properties to configure Communities behavior.
locale: en-US
release: zurich
product: Communities
classification: communities
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 11
breadcrumb: [Communities references, Communities, Customer Service Management]
---

# Properties installed with Communities

Community administrators can use properties to configure Communities behavior.

The following properties are available for further configuration. To list the properties, enter `sys_properties.list` in the filter navigator and search for the property to configure.

**Note:** You can also view **Community Properties** and **Forum Properties** from the application navigator. These modules contain a list of the most frequently used properties that you can configure for your community.

<table id="table_qc3_qt4_p4"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_communities.adminNoReplyEmail

</td><td>

Email address for community-related notifications. When a notification for an activity is sent, this email address appears. -   Type: string
-   Default value: communityadmin@servicenow.com

</td></tr><tr><td>

sn\_communities.additional\_search\_sources

</td><td>

List of additional search sources to be included for displaying search results. -   Type: string
-   Default value: "community-forums, community-topics, community-user-profiles"

</td></tr><tr><td>

sn\_communities.scheduling.allow\_authors

</td><td>

Allow or restrict authors to schedule the content. If set to "No", only administrators will be able to schedule the content.-   Type: boolean
-   Default value: Yes

</td></tr><tr><td>

sn\_communities.attachments.max\_allowed\_size

</td><td>

Maximum file size of an attachment in the community. It works as upper-cap for system property "sn\_communities.attachments.max\_file\_size".-   Type: string
-   Default value: 5 MB

</td></tr><tr><td>

sn\_communities.attachments.document.max\_allowed\_size

</td><td>

Maximum file size of a community document. It works as upper-cap for system property "sn\_communities.attachments.document.max\_size".-   Type: string
-   Default value: 25 MB

</td></tr><tr><td>

sn\_communities.blog\_count

</td><td>

Number of blogs that a user can post per day.-   Type: integer
-   Default value: 20

</td></tr><tr><td>

sn\_communities.content.meta\_description

</td><td>

When generating SEO data for an entity, the number of characters that are fetched from the meta\_description column of the record to generate a portion of the SEO &lt;description&gt; tag for the record.

 Typically, the SEO &lt;description&gt; tag for a Community entity is the combination of ‘forum name’, ‘topics’ and ‘meta description’ of the actual record in the following format: “&lt;forum&gt; - &lt;topics&gt; - &lt;sub string of configured length of the actual description&gt;".

 -   Type: integer
-   Default value: 100

</td></tr><tr><td>

sn\_communities.content.views.count.limit

</td><td>

Number of views for content pages that are allowed per session within a time window specified by sn\_communities.content.views.time.limit.-   Type: integer
-   Default value: 50

</td></tr><tr><td>

sn\_communities.content.views.time.limit

</td><td>

Duration, in seconds, during which a specific number of views are allowed. The number of views allowed during this time is set by sn\_communities.content.views.count.limit parameter.-   Type: integer
-   Default value: 3600

</td></tr><tr><td>

sn\_communities.disable\_terms\_conditions\_role

</td><td>

Comma-separated list of roles that bypass the terms and conditions and profile name request.

</td></tr><tr><td>

sn\_communities.edit\_content\_explicit\_role

</td><td>

Comma-separated list of roles with permission to edit existing content, but not to create content.-   Type: string
-   Default value: n\_communities.community\_moderator, sn\_communities.moderation\_admin, sn\_communities.admin

</td></tr><tr><td>

sn\_communities.enable\_session\_cache

</td><td>

Enables or disables session caching.

 True: The permissions of any non-admin users of the community are stored as a part of the session. They are used to determine access to the various forums and community content. While the user is active in that particular session, any changes to the community permissions do not take effect until the user logs out.

 False: The permissions of any non-admin users of the community are not stored as a part of the session.

-   Type: boolean
-   Default value: false

 **Note:** Setting this system property to true increases the overall load time when accessing the forum for the first time in a session.

</td></tr><tr><td>

sn\_communities.enable\_topics

</td><td>

Enables or disables topics within a community. If the property is set to false and gamification is enabled, topic information does not appear on the leaderboard page.

 -   Type: true\|false
-   Default value: true

</td></tr><tr><td>

sn\_communities.enable\_user\_mentions

</td><td>

Enables or disables the user-mentions functionality in Communities content.

</td></tr><tr><td>

sn\_communities.glide.script.block.client.globals

</td><td>

Set the value to true to re-enable most of the inaccessible Client APIs in a scoped application.-   Type: boolean
-   Default value: false

</td></tr><tr><td>

sn\_communities.implicit\_access\_mapping

</td><td>

Assign access implicitly to users based on the permissions they have. For example:-   If a user is given forum\_admin access, they can automatically administer, read, write to, and moderate the forum.
-   If a user is given forum moderation rights, they can read, write to, and moderate the forum for all content types.
-   Type: string
-   Default value:

\{"forum\_admin": \["forum\_read", "forum\_write", "forum\_moderator", "forum\_admin", "content\_write"\],"forum\_moderator": \["forum\_read", "forum\_write", "forum\_moderator", "content\_write"\], "content\_write": \["content\_read", "content\_write"\]\}


</td></tr><tr><td>

sn\_communities.instance\_base\_url

</td><td>

Vanity URL for your instance to be used in email notifications to redirect users to the community pages. Set a value only if you want the URL to be different to the instance name.

 -   Type: string
-   Default value: none

</td></tr><tr><td>

sn\_communities.is\_content\_write\_allowed\_for\_guest\_user

</td><td>

Determines whether Content\_write access is allowed for a public or a guest user.

 False: Content\_write access is not given to a public or guest user.

 True: Content\_write access is given to a public or guest user.

 -   Type: boolean
-   Default value: false

</td></tr><tr><td>

sn\_communities.knowledge\_base\_id

</td><td>

All questions created in Communities are entered in this knowledge base.-   Type: string
-   Default value: a4c9fb2e6703220071b89a6617415af9

</td></tr><tr><td>

sn\_communities.logging.destination

</td><td>

Location of the log messages.-   Type: string
-   Default value: db

</td></tr><tr><td>

sn\_communities.log.verbosity

</td><td>

Code Search log verbosity for the community. Set the value as required.

-   0: Show information that may be useful while debugging the application, such as the values of queries run. It includes info, warning, and error messages.
-   1: Show progress messages as the Code Search application searches for results. It also shows warnings and error messages.
-   2: Show warning which indicates possible unexpected changes in behavior.
-   3: Show only critical errors which may prevent the search from completing.

 -   Type: choice list
-   Default value: 1

</td></tr><tr><td>

sn\_communities.logging.verbosity

</td><td>

Category for writing log messages: Debug \(0\), Info \(1\), Warning \(2\), or Error \(3\). -   Type: choice list
-   Default value: 1

</td></tr><tr><td>

sn\_communities.max\_topic\_limit

</td><td>

Maximum number of topics that can be associated to any content type. The value of this property should not be set to greater than five.-   Type: integer
-   Default value: 5

</td></tr><tr><td>

sn\_communities.minimum\_activity

</td><td>

Minimum number of activities required to make the activity feed the preferred feed.-   Type: integer
-   Default value: 5

</td></tr><tr><td>

sn\_communities.portal\_default\_config

</td><td>

Community portal default configuration. Used in community-specific widgets. It is a JSON value.-   Type: string
-   Default value: \[\{"uiPageMapping":\[\{"contentTypeId":"5a2fcaa0dbd26600b1f6f78eaf9619a8","icon\_class":"fa-question-circle","internalName":"question","contentArticle":"a","pageId":"community\_question"\},\{"contentTypeId":"57f785863b2b220085f76b4ee3efc449","icon\_class":"fa-video-camera","internalName":"video","contentArticle":"a","pageId":"community\_video"\},\{"contentTypeId":"cc3fcaa0dbd26600b1f6f78eaf96192e","icon\_class":"fa-quote-left","internalName":"blog","contentArticle":"a","pageId":"community\_blog"\},\{"contentTypeId":"0764c981dbde6600b1f6f78eaf961990","icon\_class":"","internalName":"comment","contentArticle":"a","pageId":""\},\{"contentTypeId":"8f0a215c6707220071b89a6617415aa7","icon\_class":"fa-question-circle","internalName":"answer","contentArticle":"an","pageId":"community\_question"\},\{"contentTypeId":"3f86a8db971232007a97a23363ac4a27","icon\_class":"fa-file-text","internalName":"document","contentArticle":"a","pageId":"community\_document"\},\{"contentTypeId":"4c3a995ac302320012e45cb981d3aee0","icon\_class":"fa-calendar","internalName":"event","contentArticle":"a","pageId":"community\_event"\}\]\}\]

</td></tr><tr><td>

sn\_communities.public\_forum\_user

</td><td>

**sys\_id** of the public forum user. Used to calculate access permissions to forums.

-   Type: string
-   Default value: 88ef2155931322005b963511e57ffba6

</td></tr><tr><td>

sn\_communities.registered\_forum\_user

</td><td>

**sys\_id** of the registered forum user. This value is used to calculate access permissions to forums.

-   Type: string
-   Default value: 5dce996993232200dd773511e57ffbcc

</td></tr><tr><td>

sn\_communities.video\_count

</td><td>

Number of videos a user can post per day.-   Type: integer
-   Default value: 20

</td></tr><tr><td>

sn\_communities.default\_permission\_for\_forum\_memberships

</td><td>

Sets the default permission for forum memberships. Specify a value to determine which permission is used as the default.-   Type: string
-   Default value: ff73ee9893223200a8223511e57ffb0b

</td></tr><tr><td>

sn\_communities.forumListBatchSize

</td><td>

Default number of forums to show on the topics list page on the community portal. -   Type: integer
-   Default value: 12

</td></tr><tr><td>

sn\_communities.topicListBatchSize

</td><td>

Default number of topics to show on the topics list page on the community portal. -   Type: integer
-   Default value: 12

</td></tr><tr><td>

sn\_communities.disableForumInvitesForExternalEmails

</td><td>

Determines if forum invites from the forum page can be sent to external users. **Note:** Do not change this value manually because it may affect forum email invite functionality.

 -   Type: boolean
-   Default value: true

</td></tr><tr><td>

sn\_communities.attachments.document.max\_size

</td><td>

Maximum attachment file size in MB. \(1 MB = 1024 KB\)-   string
-   Default value: 5

</td></tr><tr><td>

sn\_communities.attachments.file\_extensions

</td><td>

Supported file extensions for community attachments. -   Type: string
-   Default value: PPT,PPTX,XLS,XLSX,DOC,DOCX,TXT,PDF,PNG,BMP,JPG,JPEG,GIF,ZIP

</td></tr><tr><td>

sn\_communities.attachments.max\_attachment\_count

</td><td>

Maximum number of attachments that can be attached to community content.-   Type: string
-   Default value: 3

</td></tr><tr><td>

sn\_communities.attachments.max\_file\_size

</td><td>

Maximum attachment file size in MB. The maximum size is capped at 5 MB.-   Type: string
-   Default value: 2

</td></tr><tr><td>

sn\_communities.attachments.max\_invalid\_attempts

</td><td>

Maximum number of invalid attempts a user can make to upload an attachment.-   Type: string
-   Default value: 3

</td></tr><tr><td>

sn\_communities.attachments.max\_total\_size

</td><td>

Maximum total size \(in GB\) of attachments. \(1 GB = 1024 MB\)-   Type: string
-   Default value: 500

</td></tr><tr><td>

sn\_communities.attachments.total\_size

</td><td>

Total size \(in KB\) of attachments in the community until date. \(1 MB = 1024 KB, 1 GB = 1024 MB\)-   Type: string
-   Default value: 3680.04

</td></tr><tr><td>

sn\_communities.attachments.user.day\_limit

</td><td>

Maximum number of attachments that can be attached to community content per user per day.-   Type: string
-   Default value: 20

</td></tr><tr><td>

sn\_communities.days\_to\_keep\_search\_logs

</td><td>

Sets the number of days to keep the search log on an instance.-   Type: integer
-   Default value: 180

</td></tr><tr><td>

sn\_communities.minimum\_characters\_to\_search

</td><td>

Number of characters before a search engine starts working in a community. This number must be greater than or equal to 3. -   Type: integer
-   Default value: 3

</td></tr><tr><td>

sn\_communities.search.blog.enable\_acl

</td><td>

Sets how permissions are evaluated for blog type content.True: Permission is evaluated for that specific content type and user.

 False: Permission is evaluated at the forum and content level.

 -   Type: boolean
-   Default value: false

</td></tr><tr><td>

sn\_communities.search.discussion.enable\_acl

</td><td>

Sets how permissions are evaluated for question and answer type content.True: Permission is evaluated for that specific content type and user.

 False: Permission is evaluated at forum and content level.

 -   Type: boolean
-   Default value: false

</td></tr><tr><td>

sn\_communities.search.document.enable\_acl

</td><td>

Sets how permissions are evaluated for document type content.True: Permission is evaluated for that specific content type and user.

 False: Permission is evaluated at the forum and content level.

 -   Type: boolean
-   Default value: false

</td></tr><tr><td>

sn\_communities.search.event.enable\_acl

</td><td>

Sets how permissions are evaluated for event type content.True: Permission is evaluated for that specific content type and user.

 False: Permission is evaluated at the forum and content level.

 -   Type: boolean
-   Default value: false

</td></tr><tr><td>

sn\_communities.search.video.enable\_acl

</td><td>

Sets how permissions are evaluated for video type content.True: Permission is evaluated for that specific content type and user.

 False: Permission is evaluated at the forum and content level.

 -   Type: boolean
-   Default value: false

</td></tr><tr><td>

sn\_communities.user.document\_count

</td><td>

Number of documents a user can post per day.-   Type: integer
-   Default value: 20

</td></tr><tr><td>

sn\_communities.video\_count

</td><td>

Number of videos a user can post per day.-   Type: integer
-   Default value: 20

</td></tr><tr><td>

sn\_communities.view\_log\_sources

</td><td>

JSON string that provides a mapping of view log source to a static source type. This static string stores the view source in the View Log \[sn\_communities\_view\_log\] table.-   Type: string
-   Default value:

\{"searchResult": "search\_result", "contentFeed": "content\_feed", "activityFeed": "activity\_feed"\}


</td></tr><tr><td>

sn\_communities.knowledge.enable\_harvesting

</td><td>

Enables knowledge harvesting from communities.-   Type: string
-   Default value: true

</td></tr></tbody>
</table><table id="table_emn_h1m_vz"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.snc.actsub.activities.api.fetch.limit

</td><td>

Number of activities in the activity feed. -   Type: integer
-   Default value: 10

</td></tr><tr><td>

com.snc.actsub.activity.rate.count.limit

</td><td>

Number of activities that can be created within a certain time frame. -   Type: integer
-   Default value: 100

</td></tr><tr><td>

com.snc.actsub.activity.rate.time.limit

</td><td>

Duration, in seconds, during which activities can be created. Activities are no longer created after the limit.-   Type: integer
-   Default value: 3600

</td></tr><tr><td>

com.snc.actsub.activity.stream.user.limit

</td><td>

Enter the limit on number of activities stored for a user in the activity feed.

 The oldest activities are deleted when the limit is reached.

-   Type: integer
-   Default value: 2000

</td></tr><tr><td>

com.snc.actsub.core.disable\_plugin

</td><td>

Enable \(true\) or disable \(false\) the plugin functionality.-   Type: boolean
-   Default value: false

</td></tr><tr id="row-pull-model"><td>

com.snc.actsub.activity.stream.inactive.disabled

</td><td>

Enable pull model for activity feed so that the activity fanouts are disabled and not pushed to the inactive user streams. -   Type: boolean
-   Default value: false

 **Note:** When disabled, run the Manage Activity fanouts scheduled job for the changes to take immediate effect.

</td></tr><tr><td>

com.snc.actsub.activity.stream.inactive.duration

</td><td>

The duration after which fanouts will be disabled for inactive user streams. -   Type: integer
-   Default value: 30

</td></tr><tr><td>

com.snc.actsub.activity.stream.inactive.streams

</td><td>

Enter comma separated stream names which can be considered inactive when not accessed for a certain duration.-   Type: string
-   Default value: default

</td></tr><tr id="row-activity-fo"><td>

com.snc.actsub.activity.enable\_fanout\_config

</td><td>

Enable the property to trigger **Activity Fanouts** based on the configuration at **Activity Type**. Confirm if they are properly configured and then enable the flag.-   Type: boolean
-   Default value: false

 **Note:** For zboot, this property is enabled by default. You must create this property for upgrade scenarios.

</td></tr></tbody>
</table><table id="table_wdb_cts_r1b"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_ext\_usr\_reg.allowed\_email\_domains

</td><td>

Comma-separated list of email domains that can be used to register. By default, the value is empty, indicating that all email domains are allowed.-   Type: string
-   Default value: none

</td></tr><tr><td>

sn\_ext\_usr\_reg.captchaEnabled

</td><td>

Enables Google re-CAPTCHA on the self-registration page.-   Type: boolean
-   Default value: true

</td></tr><tr><td>

sn\_ext\_usr\_reg.eur\_user\_role

</td><td>

Adds a role when a sys\_user record is created through self-registration.

 -   Type: string
-   Default value: sn\_communities.community\_user

</td></tr><tr><td>

sn\_ext\_usr\_reg.Reg\_link\_expiration\_days

</td><td>

Number of days that the registration link remains active. Links which are older than the specified number of days are deactivated and cannot be used for completing the registration process.

 -   Type: integer
-   Default value: 3

</td></tr><tr><td>

sn\_ext\_usr\_reg.request\_count

</td><td>

Maximum number of times a registration link can be requested.-   Type: integer
-   Default value: 3

</td></tr><tr><td>

sn\_ext\_usr\_reg.Temp\_user\_record\_purge\_days

</td><td>

Number of days that a registration record is maintained in the User Registration Request \[user\_registration\_request\] table. Records older than the specified number of days are deleted.-   Type: integer
-   Default value: 30

</td></tr></tbody>
</table><table id="external-user-registration-properties"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_communities.enable\_gamification

</td><td>

Enables or disables the gamification feature for the community and controls the appearance of gamification-related widgets on the Community portal. When set to false, no gamification components are displayed. User point totals and badge assignments are not affected.

 -   Type: boolean
-   Default value: true

</td></tr><tr><td>

sn\_communities.content.show\_gamification\_level

</td><td>

Controls the gamification level that is displayed next to the Community user's name on the Content pages. -   Type: choice list
-   Choices:
    -   **none**: Do not display the user's level
    -   **sn\_gamification\_modules**: Show the user's level in the Community
    -   **sn\_communities\_forum**: Show the user's level for the forum to which the content belongs
-   Default value: sn\_gamification\_modules

</td></tr><tr><td>

sn\_gamification.days\_to\_keep\_activity\_records

</td><td>

Number of days to keep the gamification activity records in the database. Records created or updated prior to the specified number of days are purged. -   Type: integer
-   Default value: 180

</td></tr><tr><td>

sn\_gamification.enable\_debug\_logs

</td><td>

Enables the debug logs for the gamification feature. -   Type: boolean
-   Default value: false

</td></tr><tr><td>

sn\_gamification.levels\_limit

</td><td>

Maximum number of levels that can be defined for the gamification feature.-   Type: integer
-   Default value: 10

</td></tr></tbody>
</table><table id="table_ndl_51c_kdb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn.communities.enable\_csm\_case\_creation\_from\_question

</td><td>

This property provides access to the “Create Case” option on the Community Question widget and the “Question to Case” option on the Community header list menu.-   Type: true \| false
-   Default value: true

</td></tr></tbody>
</table><table id="table_m3g_2sr_trb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

sn\_kb\_social\_qa.max\_answers\_per\_user\_daily

</td><td>

Enter the maximum number of times a user can post answers to the Social Q&amp;A questions per day.-   Type: Integer
-   Default value: 500
-   Location: System Properties

</td></tr><tr><td>

Maximum number of Social Q&amp;A comments that can be posted per user per day.sn\_kb\_social\_qa.max\_comments\_per\_user\_daily

</td><td>

Enter the maximum number of times a user can post comments to the Social Q&amp;A questions or answers per day.-   Type: Integer
-   Default value: 500
-   Location: System Properties

</td></tr><tr><td>

Maximum number of Social Q&amp;A questions that can be posted per user per day.sn\_kb\_social\_qa.max\_questions\_per\_user\_daily

</td><td>

Enter the maximum number of times a user can post Social Q&amp;A questions per day. -   Type: Integer
-   Default value: 500
-   Location: System Properties

</td></tr></tbody>
</table>**Parent Topic:**[Communities references](communitie-references.md)

**Related topics**  


[Quick start tests for Communities](../../../administer/atf-quick-start-tests/reference/quick-start-tests-communities.md)

[Communities roles](communities-roles.md)

[Forum form fields](forum-form-fields.md)

[Video Configurations form fields](video-configurations-form-fields.md)

[Topic form fields](topic-form-fields.md)

