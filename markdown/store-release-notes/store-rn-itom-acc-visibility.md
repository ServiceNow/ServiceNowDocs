---
title: Agent Client Collector for Visibility release notes
description: Version history for the Agent Client Collector for Visibility on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-acc-visibility.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - ITOM Visibility release notes, ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Agent Client Collector for Visibility release notes

Version history for the Agent Client Collector for Visibility on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.15.0 - June 2026**
    -   New:
        -   Integrated Cilium with KVA to retrieve Kubernetes resource connectivity data for creating service maps
        -   Added the ability to automatically retire Kubernetes clusters and related resources when no activity is detected within a configurable time period
    -   Changed: Updated KVA licensing to an image-based model, replacing the previous container-based approach
-   **Version 3.14.1 - March 2026**
    -   Informer Version 2.5.0 - \[March 2026 Store Release\]
    -   New:
        -   Service maps now include Kubernetes and all related service resources beyond the Kubernetes environment.
        -   Kubernetes Service Maps offer more control over the CI visualization.
        -   KubeVirt VMs running in Kubernetes are being now added to the CMDB.
        -   Service mapping with KVA for micro-services is supported.
        -   KVA pod can run in an OKE \(Oracle Kubernetes Engine\) environment.
    -   Fixed: KVA now populates ObjectID in alignment with SGC for EKS, AKS and GKE cluster environments.
-   **Version 3.13.0 - December 2025**
    -   New: Additional control over the CIs displayed in Kubernetes Service MapsBring KubeVirt VMs running in Kubernetes into the CMDB
    -   Changed: Option to force TLS 1.3 connection between Informer and SN instanceDiscover External IP addresses of K8s Service using helm flag
-   **Version 3.9.0 - November 2024**
    -   New:
        -   Multi Arch support for Informer docker image\(AMD64 and ARM64\)
        -   Enhanced ability to configure OOB and additional Kubernetes resources.
-   **Version 3.8.0 - August 2024**
    -   Added support for remote upgrade of informers from ServiceNow instance
    -   The following fields will be added to table cmdb\_ci\_kubernetes\_node and will be populated by CNO. kubelet\_version kubeproxy\_version container\_runtime\_version
    -   Ability to control execution parameters from the ServiceNow instance
    -   Ability to define related records to be associated with a custom resource
    -   Bug fixes
-   **Version 3.6.2 - May 2024**

    New: You can define a number of additional Kubernetes resources that you need to bring into the CMDB. You can also define values they would like to bring beyond the out-of-box values such as name, UID and namespace the system brings automatically.

-   **Version 3.5.0 - February 2024**

    Migrated policies and scripts from Agent Client Collector for Visibility store application to Agent Client Collector for Visibility core application.

-   **Version 3.4.0 - November 2023**
    -   New:
        -   Installed Software and Software Metering: support for additional data sources:
            -   chocolatey
            -   winget
            -   click-to-run
        -   Software Metering:
            -   property to bypass reclamation rules and directly create software usage for licensable software
            -   property to rely on the computer assigned\_to attribute when the user running a process can't be mapped to a sys\_user
        -   Ease-of-Use test checks
    -   Changed: OOTB policies: software metering only extracted on Computer CIs
    -   Fixed:
        -   Hardware information on some AWS instance types
        -   'Is Virtual' flag on some hardware types
-   **Version 3.3.0 - August 2023**

    -   New
        -   Software Metering and Assigned To: Support for mapping users to the right Active Directory domain: sn\_acc\_visibility.advanced\_metering\_user\_mapping\_field
        -   SAM Advanced Metering: Support for MacOS Endpoint devices; see the notes below for activating the feature.
    -   Changed
        -   SAM Advanced Metering: Allows for additional datapoints collected by osqueryd.
    -   Fixed
        -   Filtering out invalid software versions.
        -   Fixes in installed software and logged in user modules.
        -   Storage Devices: Support for NON Microsoft disks on Windows cloud instances.
    Note on SAM Advanced Metering for MacOS: When upgrading the ACC-V plugin, apply the changes for the Installed Software + SAM Advanced policies and republish them to take effect.

-   **Version 3.1.0 - May 2023**
    -   New:
        -   Support for MacOS Ventura on ARM64 - Apple Silicon M1/M2
        -   K8S Discovery via Informer.
    -   Fixed:
        -   Installed Software policy: handling large payload.
        -   IRE identifier on persisting file systems.
-   **Version 3.0.0 - November 2022**
    -   New:
        -   cmdb\_ci\_computer.assigned\_to can be assigned via sn\_acc\_visibility.set\_assigned\_to and sn\_acc\_visibility.assigned\_to\_user\_order properties.
        -   Full support for ACC running on GCP: Object ID retrieved and CI relationship created if the VM instance record is populated via Cloud Discovery.
        -   Extended coverage on local and remote file systems.
        -   Memory Modules
        -   Support for localization on the ServiceNow instance.
    -   Changed: More flexibility in OS Users: Preference for local and/or system/special accounts collected via sn\_acc\_visibility.persist os\_user\_type sys\_property.
    -   Fixed: OS users: Data collection will not trigger the mount of user home directories when automount is enabled.
-   **Version 2.3.0 - August 2022**
    -   New:
        -   Supporting new OS Versions
            -   Windows 2022 Server
            -   macOS Monterey \(x86\)
            -   CentOS Stream 8 and 9
            -   RHEL 9
        -   Windows installer improvements
            -   Run agent service as gMSA, LocalService and Local SYSTEM accounts
            -   Additional options added to commandline agent installer
                -   ServiceNow user set with "password never expires"
                -   DenyLogicalLogin for ServiceNow user
                -   Agent installation will not automically start the service
        -   Host CI Identification
            -   Agent will use the serial number table to uniquely identify the CI through IRE
            -   Ability to choose the type of required serial number \[BIOS, Baseboard and others\] to the computer CI serial\_number attribute via the system property sn\_agent.ci\_serial\_number.pref\_order
        -   Support for DNS names \(just like using Horizontal Discovery\)
        -   Installed Software: identify portable applications installed from portableapps.com
    -   Changed:
        -   Allow List for ACC-Visibility plugins: skip\_arguments set to true
        -   Attributes collection reworked between base ACC-F scripts and ACC-V modules
    -   Fixed: Software Edition fixed for Adobe Acrobat and Microsoft SQL Server
-   **Version 2.2.3 - May 2022**
    -   New:
        -   Support for Windows 11 Professional and Enterprise
        -   Software Metering: Support for Last Accessed Time for MacOS
        -   Hardware Components: Intel vPro Platform attributes
    -   Changed:
        -   Dedicated check type for SAM policies
        -   OS Users: hide unused 'password' column
    -   Fixed:
        -   Installed Software policy not activated
        -   Storage devices rejected by IRE on some Windows systems
        -   Provided\_by value in storage\_devices and file\_systems missing on some environments
        -   File system and storage device types missing in dropdown
        -   Running osqueryi commands on systems running osquery daemon
        -   OS users records not refreshed
        -   Owns:Owned by relationship missing between network adapters and ip addresses
-   **Version 2.1.0 - February 2022**
    -   New: Support for IPv6
    -   Changed: Replaced all PowerShell commands with native Ruby and/or via OSQuery
    -   Fixed:
        -   Network Adapter and IP addresses marked as absent
        -   OS installation date time: fix timezone
        -   OSQuery hanging in some cases
        -   Updated check definitions for Enhanced Discovery
-   **Version 2.0.0 - December 2021**
    -   New:
        -   Introduced SAM Total Usage Metrics for Installed Software on Windows.
        -   Local users retrieved and stored in cmdb\_os\_user table.
    -   Changed:
        -   CI Name coming from computername vs. DNS hostname on Windows, now using the following properties:
            -   glide.discovery.hostname.wmi\_trusted
            -   glide.discovery.hostname.case
        -   Installed software moved to its own policy
    -   Fixed:
        -   Array storage devices on Windows
        -   Special file systems on Windows
        -   Collect chassis serial number
        -   Install date on MacOS
        -   Network adapters with empty name or MAC address
-   **Version 1.3.0 - September 2021**
    -   New:
        -   Support for Oracle Linux, Amazon Linux 2, and MacOS \(x86\_64 architecture only\)
        -   Exclusion lists for unwanted NICs and/or IP addresses
    -   Fixed:
        -   UTF-8 characters \(see KB0966705 for configuring the MID for UTF-8 support\)
        -   Related CI relationships in some cases with multiple NICs
        -   Disk partition name on nvme devices
-   **Version 1.2.0 - July 2021**
    -   New:
        -   Support for additional cloud providers: Azure and GCP
        -   Independent file systems \(squashfs\)
    -   Changed:
        -   The discovery source for Software Installations \(cmdb\_sam\_sw\_install\) is set to "ServiceNow" to avoid duplicate records when running both agent-based and horizontal Discovery
        -   Performance improvements at the agent registration
        -   Default serial number on Windows set to Baseboard and fallback to BIOS serial number to align with horizontal discovery behavior Interval value set to 24 hours by default on the updated discovery policy
    -   Fixed:
        -   Several gaps in data collection for installed software, chassis, storage devices and file systems Partial payload returned for updated discovery script when a sub-script fails Duplicate CI IP record cleanup Serial number input validation
-   **Version 1.0.12 - May 2021**
    -   Changed: Discovery Source for ACC-V is now "ACC-Visibility"
    -   Fixed: Minor issue on FQDN on Windows in specific cases
    -   Known Issues: Error handling in the payload for storage devices on some Windows devices. Temporary workaround: take off storage\_devices from the check definition.
-   **Version 1.0.3 - April 2021**
    -   New: Support for Ubuntu
    -   Changed: Improvements to data collection for SAM software usage
    -   Fixed:
        -   Windows Servers and SLES classified as servers instead of computers
        -   Software installations on Windows 2012 R2
        -   Timezone for software usage - last used timestamp
        -   Object ID for Windows 2019 instances on AWS
    -   Removed: DHCP enabled flag on Linux

**Parent Topic:**[ServiceNow Store - ITOM Visibility release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itom-visibility-landing.md)

