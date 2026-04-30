---
title: Create encryption keys and certificate
description: Create encryption keys and a certificate using terminal commands on your local environment.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring client accessible secrets, Secrets Management, Platform Security]
---

# Create encryption keys and certificate

Create encryption keys and a certificate using terminal commands on your local environment.

## Before you begin

Role required: none

## Procedure

1.  In your local environment, open Terminal \(On Mac or Linux\), or Command Line \(in Windows\).

2.  Using the terminal, use `cd` to move into the folder where you want to store your encryption keys.

3.  Using the terminal, enter the following:

    ```
    openssl req -newkey rsa:4096 -nodes -keyout sm_private_key.pem -x509 -days 365 -out sm_public_cert.pem
    ```

    **Note:** This example uses OpenSSL to generate keys and certificates. You may substitute other comparable tools based on your requirements.

    The command generates a private key and a public certificate \(with the matching public key\). A series of prompts for required information follows, starting with “Country Name.”

4.  Fill in the prompts with the requested information.

    The following prompts appear.

    -   Country Name
    -   State of Province Name
    -   Locality Name \(eg, city\)
    -   Organization Name \(eg, company\)
    -   Organizational Unit name \(eg, section\)
    -   Common Name \(eg, fully qualified host name\)
    -   Email address
    Work with your security team to ensure you enter the correct certificate information.

    ![Prompts displayed by openssl](../images/client-side-1.png)

5.  Check the folder you that chose in step 2 to verify that the private key and public certificate have been created.

    If you used the same file names as in the step 3 example, you should see the following files:

    -   sm\_private\_key.pem
    -   sm\_public\_cert.pem
6.  In the same folder, use the following command:

    **Important:** The specific command to use depends on your operating system.

<table id="table_f4s_2k2_51c"><tbody><tr><td>

For Linux:

</td><td>

```
cat sm_private_key.pem sm_public_cert.pem > sm_keypair_bundle.pem
```

</td></tr><tr><td>

For Windows:

</td><td>

```
sm_private_key.pem sm_public_cert.pem > sm_keypair_bundle.pem
```

</td></tr></tbody>
</table>    This command bundles the private key and public certificate into a single file to load into your MID Server in later steps.

7.  Check the folder again to verify that the new file containing your private key \(sm\_keypair\_bundle.pem\) and public certificate has been created.


**Parent Topic:**[Configuring client accessible secrets](../concept/client-access-secret-landing.md)

