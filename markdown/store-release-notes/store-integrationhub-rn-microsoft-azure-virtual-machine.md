---
title: Microsoft Azure Virtual Machine spoke release notes
description: Version history for the Integration Hub Microsoft Azure Virtual Machine spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-microsoft-azure-virtual-machine.html
release: store
topic_type: reference
last_updated: "2024-11-07"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Microsoft Azure Virtual Machine spoke release notes

Version history for the Integration Hub Microsoft Azure Virtual Machine spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.0.0 - November 2024**
    -   New:
        -   Microsoft Azure Virtual Machine Spoke now makes use of the default alias for Microsoft Resource Management Spoke \(sn\_azure\_rm\_spoke.Microsoft\_Azure\_Resource\_Management\)
        -   New Actions with latest design pattern of complex object outputs, retry policy, connection &amp; credentials, and error evaluation making use of the new connection &amp; credential alias:
            -   Image Management:Create Image from Virtual Machine \(create\_image\_from\_virtual\_machine\), Delete Image \(delete\_image\_v2\), Get Images by Resource Group \(Metadata\) \(get\_images\_by\_resource\_group\_metadata\), Look up Image \(look\_up\_image\), Look up Images Stream by Resource Group \(look\_up\_images\_stream\_by\_resource\_group\), Look up Images Stream by Subscription ID \(look\_up\_images\_stream\_by\_subscription\_id\), Set Tags on Image \(set\_tags\_on\_image\)
            -   Virtual Machine Resource Image Management: Get Virtual Machine Image Offers \(Metadata\) \(get\_virtual\_machine\_image\_offers\),Get Virtual Machine Image Publishers \(Metadata\) \(get\_virtual\_machine\_image\_publishers\),Get Virtual Machine Image SKUs \(Metadata\) \(get\_virtual\_machine\_image\_skus\),Get Virtual Machine Image Versions \(Metadata\) \(get\_virtual\_machine\_image\_versions\),Look up Virtual Machine Image \(look\_up\_virtual\_machine\_image\)
            -   Virtual Machine Management: Attach Disk \(attach\_disk\_v2\),Create Virtual Machine \(create\_virtual\_machine\),Create Virtual Machine from Image \(create\_virtual\_machine\_from\_image\_v2\),Deallocate Virtual Machine \(deallocate\_virtual\_machine\),Delete Virtual Machine \(delete\_virtual\_machine\),Detach Disk \(detach\_disk\),Generalize Virtual Machine \(generalize\_virtual\_machine\),Get Disks by Virtual Machine \(Metadata\) \(get\_disks\_by\_virtual\_machine\_metadata\),Get Virtual Machines by Resource Group \(Metadata\) \(get\_virtual\_machines\_by\_resource\_group\),Look up Virtual Machine \(look\_up\_virtual\_machine\),Look up Virtual Machine Runtime Details \(look\_up\_virtual\_machine\_runtime\_details\),Look up Virtual Machines Stream by Resource Group \(look\_up\_virtual\_machines\_stream\_by\_resource\_group\),Look up Virtual Machines Stream by Subscription ID \(look\_up\_virtual\_machines\_stream\_by\_subscription\_id\),Power Off Virtual Machine \(power\_off\_virtual\_machine\),Redeploy Virtual Machine \(redeploy\_virtual\_machine\),Resize Virtual Machine \(resize\_virtual\_machine\),Restart Virtual Machine \(restart\_virtual\_machine\),Start Virtual Machine \(start\_virtual\_machine\)
            -   Virtual Machine Size Management: Get Sizes by Availability Set \(Metadata\) \(get\_sizes\_by\_availability\_set\),Get Sizes by Location \(Metadata\) \(get\_sizes\_by\_location\),Get Sizes by Virtual Machine \(Metadata\) \(get\_sizes\_by\_virtual\_machine\)
    -   Removed:
    -   -   Deprecated old credential alias Azure\_Virtual\_Network \(sn\_azure\_vn\_spoke.Azure\_Virtual\_Network\)
-   Deprecated Actions that make use of old credential alias:
    -   Image Management:Create Image From Instance \(Deprecated\) \(create\_image\_from\_existing\_instance\),Delete Image \(Deprecated\) \(delete\_image\),Get Image Information \(Deprecated\) \(get\_image\_information\),List Image Name by Resource \(Deprecated\) \(list\_image\_names\_by\_resource\),Look Up Images By Resource Group \(Deprecated\) \(list\_images\_by\_resource\), Look Up Images By Subscription ID \(Deprecated\) \(look\_up\_images\_by\_subscription\_id\), Set Tags On Image \(Deprecated\) \(update\_image\)
    -   Virtual Machine Resource Image Management: Get Image \(Deprecated\) \(new\_get\_image\),Look Up Offers \(Deprecated\) \(list\_offers\),Look Up Publishers \(Deprecated\) \(list\_publishers\),Look Up SKUs \(Deprecated\) \(list\_skus\),Look Up Versions \(Deprecated\) \(list\_versions\)
    -   Virtual Machine Management: Attach Disk \(Deprecated\) \(attach\_disk\),Create Virtual Machine \(Deprecated\) \(create\_virtual\_machine\_with\_empty\_data\_disk\),Create Virtual Machine From Image \(Deprecated\) \(create\_virtual\_machine\_from\_image\),Deallocate Instance \(Deprecated\) \(deallocate\_instance\),Delete Instance \(Deprecated\) \(delete\_instance\),Detach Disk \(Deprecated\) \(add\_data\_disk\), Generalize Instance \(Deprecated\) \(generalize\_instance\), Get VM Instance Details \(Deprecated\) \(get\_instance\_view\_of\_a\_virtual\_machine\),Get VM Runtime Details \(Deprecated\) \(get\_runtime\_state\_of\_instance\),List Instance Names by ResourceGroup \(Deprecated\) \(list\_instance\_names\_by\_resourcegroup\),List Storage Account Types \(Deprecated\) \(list\_storage\_account\_types\),Look Up Disks By Instance \(Deprecated\) \(look\_up\_disks\_by\_instance\),Look Up Instances By Resource Group \(Deprecated\) \(lists\),Look Up Instances By Subscription ID \(Deprecated\) \(list\_all\),Power Off Instance \(Deprecated\) \(power\_off\),Redeploy Instance \(Deprecated\) \(re\_deploy\),Resize Instance \(Deprecated\) \(resize\),Restart Instance \(Deprecated\) \(restart\),Start Instance \(Deprecated\) \(start\)
    -   Virtual Machine Size Management: Look Up Sizes By Availability Set \(Deprecated\) \(list\_all\_available\_sizes\_in\_availability\_set\),Look Up Sizes By Instance \(Deprecated\) \(list\_available\_sizes\),Look Up Sizes By Location \(Deprecated\) \(list\_all\_available\_sizes\_by\_region\)
-   **Version 1.0.8 - July 2024**
    -   Fixed: Defects related to post-processing script for actions:
        -   Look Up Images By ResourceGroup
        -   List Instance Names by ResourceGroup
-   **Version 1.0.6 - September 2023**

    Fixed: The license requirements.

-   **Version 1.0.4 - April 2023**

    Fixed: Improve installation performance of spoke.

-   **Version 1.0.3 - July 2020**

    Patch release of Microsoft Azure Virtual Machine Spoke for IntegrationHub. This version adds KMF modules for additional security of the password2 fields, and Rome compatibility.

-   **Version 1.0.1 - June 2020**

    Provides actions to automate instance management, virtual machine size, and image management within the Microsoft Azure Virtual Machine environment.


