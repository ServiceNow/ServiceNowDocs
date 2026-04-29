---
title: Inbound Integration for Data Loss Prevention Incident Response
description: Create single or multiple DLP incidents by using the Inbound REST API.
locale: en-US
release: australia
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Data Loss Prevention Incident Response, Security Operations]
---

# Inbound Integration for Data Loss Prevention Incident Response

Create single or multiple DLP incidents by using the Inbound REST API.

## Create a single DLP incident

Role required: sn\_dlir.api\_integration\_user.

To create a single DLP incident, define the following parameters as necessary:

<table id="table_kcx_4ch_h5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

HTTP Method

</td><td>

POST

</td></tr><tr><td>

URL

</td><td>

`https://{instance}/api/now/import/sn_dlir_incident_import`

</td></tr><tr><td>

Request Header

</td><td>

-   **Accept:**

**application/json**

-   **Content-Type:**

**application/json**


</td></tr><tr><td>

Sample Payload

</td><td>

```
{
    "application_window_title": "<value>",
    "assigned_to": "<value>",
    "attachments": "<value>",
    "data_owner_email": "<value>",
    "destination": "<value>",
    "dest_ip": "<value>",
    "dest_ip_port": "<value>",
    "detection_date": "<value>",
    "endpoint_on_corporate_net": "<value>",
    "files": "",
    "file_created": "",
    "file_created_by": "",
    "file_location": "",
    "file_modified_by": "",
    "file_name": "",
    "file_owner": "",
    "file_permissions": "",
    "ftp_user_name": "",
    "last_modified": "",
    "machine_ip": "",
    "machine_name": "",
    "match_count": "",
    "policy_id": "",
    "policy_name": "",
    "printer_name": "",
    "printer_type": "",
    "print_job_name": "",
    "recipients": "",
    "scanned_machine": "",
    "scan_source": "",
    "seen_before": "",
    "sender":"",
    "source":"",
    "source_file":"",
    "source_ip":"",
    "source_ip_port":"",
    "subject":"",
    "url":"",
    "user_justification":""
}
```

</td></tr><tr><td>

Sample Response

</td><td>

```
{
    "import_set": "ISET0010003",
    "staging_table": "sn_dlir_incident_import",
    "result": [
        {
            "transform_map": "",
            "table": "sn_dlir_incident",
            "display_name": "number",
            "display_value": "DLP0001012",
            "record_link": "https://{instance}/api/now/table/sn_dlir_incident/7cda322297c2411056a43d1e6253af1f",
            "status": "inserted",
            "sys_id": "7cda322297c2411056a43d1e6253af1f"
        }
    ]
}
```

</td></tr></tbody>
</table>## Create multiple DLP incidents

Role required: sn\_dlir.api\_integration\_user.

To create multiple DLP incidents from the same request, define the following parameters as necessary:

<table id="table_o4d_g2h_h5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

HTTP Method

</td><td>

POST

</td></tr><tr><td>

URL

</td><td>

`https://{instance}/api/now/import/sn_dlir_incident_import/insertMultiple`

</td></tr><tr><td>

Request Header

</td><td>

-   **Accept:**

**application/json**

-   **Content-Type:**

**application/json**


</td></tr><tr><td>

Sample Payload

</td><td>

```
{
    "records": [
        {
            "file_name": "<value>",
            "file_modified_by": "<value>",
            "work_notes": "<value>",
            "url": "<value>",
            "scan_source": "<value>",
            "data_owner_email": "<value>",
            "file_created_by": "<value>",
            "file_owner": "<value>",
            "policy_name": "<value>"
        },
        {
            "dest_ip": "<value>",
            "dest_ip_port": "<value>",
            "detection_date": "<value>",
            "endpoint_on_corporate_net": "<value>",
            "files": "<value>",
            "file_created": "<value>",
            "file_created_by": "<value>",
            "file_location": "<value>",
            "file_modified_by": "<value>",
            "file_name": "<value>",
            "file_owner": "<value>",
        }
    ]
}
```

</td></tr><tr><td>

Sample Response

</td><td>

```
{
    "import_set_id": "a38f69229734dd1056a43d1e6253af75",
    "multi_import_set_id": "e78f69229734dd1056a43d1e6253af75"
}
```

</td></tr></tbody>
</table>**Note:** By default, the transformation is asynchronous. To set synchronous transformation, create a new record in the REST Insert Multiples \[sys\_rest\_insert\_multiple\] table, select the source table as **sn\_dlir\_incident\_import**, and set the transformation to **synchronous**.

