---
title: Sitemap Generator release notes
description: Version history for the Sitemap Generator application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-seo-sitemap-generator.html
release: store
topic_type: reference
last_updated: "2025-12-04"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Other ServiceNow AI Platform Capabilities applications, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Sitemap Generator release notes

Version history for the Sitemap Generator application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.3.0 - December 2025**

    As a part of the change a new role has been introduced "sitemap\_admin" which will have all rights overall all sitemap capabilities.Change: Previously you required an "admin" role, but not we are introducing a new granular role "sitemap\_admin" for this. Users with admin role will still continue to have the same functionality as before.

-   **Version 1.2.0 - August 2025**

    Fixed minor bugs.

-   **Version 1.1.4 - May 2024**

    Fixed: Improved the instance security by adjusting the configuration of the access control list \(ACL\).

-   **Version 1.1.1 - April 2023**
    -   Fixed:
        -   Security issues.
        -   Updated the Last Modified Date to be in compliance with Google SEO standard.
        -   Removed the changefreq attribute from the sitemap index file.
-   **Version 1.1.0 - February 2023**
    -   New:
        -   Automatic validation that portal URLs are public: Avoid errors and manually validation that portal URLs are publicly accessible with built-in validation. Upon generation of the sitemap, portal URLs that are not publicly accessible are not added to the sitemap automatically. However, this does not apply for URLs with custom domains instead of the ServiceNow domain.
        -   Specify the number of URLs per sitemap page: Control how many pages are in a sitemap by configuring the number of URLs to include per page with the glide.sitemap.page.count system property. The default value is 750, and the maximum value is 5,000. Previously, the default value was 5,000.
        -   Code templates for sitemap definitions: Create sitemaps quickly with code templates and guidance included in the Script and Static XML fields where the sitemap contents are defined.
        -   Automatic inclusion of hreflang tags: Avoid manually adding hreflang tags with built-in support for automatically including hreflang tags in the generated sitemap XML for pages in multiple languages with hreflang tags configured.
-   **Version 1.0.6 - December 2022**
    -   Changed: Made the Sitemap Generator application available to activate or update from the platform with the Utah release by navigatingto All &gt; System Applications &gt; All Available Applications &gt; All.
    -   Fixed: An issue with generating the url elements in the sitemap XML.
-   **Version 1.0.2 - August 2022**

    The ServiceNow Sitemap Generator application allows admin users to define and automatically generate XML sitemaps to improve search engine optimization of their publicly accessible portals, including all public article pages, and help portal users find the information they need.


