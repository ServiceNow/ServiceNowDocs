---
title: Policy list for scanning cloud accounts
description: A list of default policies provided for scanning the cloud accounts.
locale: en-US
release: yokohama
product: Cloud Account Management
classification: cloud-account-management
topic_type: reference
last_updated: "2024-08-02"
reading_time_minutes: 3
breadcrumb: [Cloud Account Management reference, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Policy list for scanning cloud accounts

A list of default policies provided for scanning the cloud accounts.

## Default policies for scan accounts

<table id="table_ard_jzj_gcc"><thead><tr><th>

Policy Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Check AWS Discovery Schedule

</td><td>

Verifies whether an AWS account has a discovery schedule attached. Running discovery regularly helps facilitate the identification and management of potential security risks.

</td></tr><tr><td>

Check AWS Account Alias

</td><td>

Verifies an AWS account has a unique alias to improve account management, reduce errors, and promote clarity and traceability within your AWS infrastructure. **Note:** Make sure you have API permission for iam: ListAccountAliases.

</td></tr><tr><td>

Check AWS Account Owner Tag

</td><td>

Verifies whether an AWS account has a designated owner to enhance accountability, streamline incident response, and facilitate communication within your AWS environment.

</td></tr><tr><td>

Check AWS Custom Password Policy

</td><td>

Verifies whether a custom password policy is set for every AWS account. A robust password requirement for all IAM users significantly increases the difficulty for attackers to crack passwords through brute-force attacks or credential theft attempts, ultimately enhancing the overall security of your AWS infrastructure.**Note:** Make sure you have API permission for iam: GetAccountPasswordPolicy.

</td></tr><tr><td>

Check AWS Failed Certification

</td><td>

Verifies the AWS account certification status. Failed certifications indicate potential security vulnerabilities because compromised credentials might not be deactivated promptly and provide a window of opportunity for attackers to exploit these weaknesses.

</td></tr><tr><td>

Check AWS Pending Certification

</td><td>

Verifies whether an AWS account certification is in a pending state to enable the prompt resolution of pending certifications and avoid potential security vulnerabilities.

</td></tr><tr><td>

Check AWS Strong Password Policy

</td><td>

Verifies whether an AWS account adheres to a strong password policy to promote security. This policy mandates robust password complexity requirements, significantly bolstering your AWS environment's defense against unauthorized access.**Note:** Make sure you have API permission for iam: GetAccountPasswordPolicy.

</td></tr><tr><td>

Check Azure Discovery Schedule

</td><td>

Verifies whether Azure account has a discovery schedule attached. This policy helps secure and up-to-date resource landscape to facilitate the identification and management of potential security risks.

</td></tr><tr><td>

Check Azure Account Owner Tag

</td><td>

Verifies if Azure account has a designated owner tag to enhance accountability and facilitate communication within your Azure environment. This policy readily identifies the responsible party for each account, promoting a culture of ownership and streamlined incident response.

</td></tr><tr><td>

Check Azure Failed Certification

</td><td>

Verifies Azure account certification status for failure to promote strong access control by proactively monitoring for any service account with a failed certification status. Failed certifications indicate potential security vulnerabilities, as compromised credentials might not be deactivated promptly. This policy minimizes the window of opportunity for attackers to exploit these weaknesses.

</td></tr><tr><td>

Check Azure Pending Certification

</td><td>

Verifies if Azure service account certification is in a pending state. This monitoring enables prompt resolution of pending certification and avoids potential security vulnerabilities.

</td></tr><tr><td>

Check GCP Discovery Schedule

</td><td>

Verifies whether GCP account has a discovery schedule attached. This policy helps secure and up-to-date resource landscape to facilitate the identification and management of potential security risks.

</td></tr><tr><td>

Check GCP Account Owner Tag

</td><td>

Verifies if GCP account has a designated owner tag to enhance accountability and facilitate communication within your GCP environment. This policy readily identifies the responsible party for each account, promoting a culture of ownership and streamlined incident response.

</td></tr><tr><td>

Check GCP Failed Certification

</td><td>

Verifies GCP account certification status for failure to promote strong access control by proactively monitoring for any service account with a failed certification status. Failed certifications indicate potential security vulnerabilities, as compromised credentials might not be deactivated promptly. This policy minimizes the window of opportunity for attackers to exploit these weaknesses.

</td></tr><tr><td>

Check GCP Pending Certification

</td><td>

Verifies if GCP account certification is in a pending state. This monitoring enables prompt resolution of pending certification and avoids potential security vulnerabilities.

</td></tr></tbody>
</table>To return to the procedure, see [Set up scan configuration for data visualization](../task/set-up-data-visualization.md).

**Parent Topic:**[Cloud Account Management reference](cam-reference.md)

