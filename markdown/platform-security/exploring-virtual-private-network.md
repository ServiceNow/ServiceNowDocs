---
title: Exploring Virtual Private Network \(VPN\)
description: Use a virtual private network \(VPN\) to integrate your instance with external data sources over the Internet.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Virtual Private Network \(VPN\)]
---

# Exploring Virtual Private Network \(VPN\)

Use a virtual private network \(VPN\) to integrate your instance with external data sources over the Internet.

My IP Information

When configuring an integration that uses an encrypted protocol, such as Lightweight Directory Access Protocol \(LDAP\) or HTTPS, it is good practice to use the Internet as a transport mechanism.

However, there may be security or network architecture requirements that dictate the use of a site-to-site Internet Protocol Security \(IPSEC\) Virtual Private Network \(VPN\) connection between the datacenters and your business networks. The VPN supports the necessary encrypted communication between the instance and your network.

**Warning:**

When a VPN tunnel is initiated, it operates as site-to-site connection. This means that the endpoint on your infrastructure receives an IP address, referred to as an encryption domain. This public IP can be accessed by any instance within the same data center.

For example, if you have an internal web service and establishes a VPN tunnel, your instance is able to reach the internal endpoint as well as all your other instances in the same data center.

## VPN connections

The ServiceNow VPN infrastructure uses pairs of Cisco adaptive security appliance \(ASA\) devices that serve as VPN termination points.

The VPN between the instance and your network utilizes your existing networking hardware to support communications. It is not necessary to install a piece of hardware. Because each customer has a unique configuration, the instance has a flexible VPN solution. the instance has built tunnels to Checkpoint, Juniper, Nortel, and other IPSEC VPN-capable devices.

The VPN connections between the instance and your network are created to support the encrypted flow of traffic into your network. Frequently, integrations that use the VPN do not have encryption as part of the underlying protocol. For example, [LDAP](../../../integrate/ldap/concept/c_LDAPIntegration.md) over the VPN versus LDAPS over the Internet and HTTP over the VPN versus HTTPS over the Internet.

The network does not allow any inbound-to-ServiceNow integration or end-user-to-ServiceNow traffic to traverse a VPN connection. This restricted communication includes end-user access to the platform, administration of the platform, web services integrations, and other integrations that are configured to use a [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US). All such inbound communication to the instance must be performed over the Internet using HTTPS. This configuration provides an encrypted communication channel. The encryption channel, along with IP access control, meets the security requirements for this traffic flow.

## Addresses for VPN communication

To prevent conflict or overlap with internal ServiceNow networks or with another internal IP address schemes in your network, all tunneled traffic in the encryption domain must use non-RFC-1918 addresses on both sides of the tunnel.

ServiceNow provides a single IP address for the source of queries into your network. You must provide Network Address Translation \(NAT\), non-RFC-1918 addresses for each host that is integrating with your instance. These public addresses need to be owned by your organization. Third-party addresses cannot be used inside tunnels. Additionally, the encryption domain must not contain the IP address of the VPN peer.

## Redundant tunnels

There are two ways to build redundancy for your tunnels:

-   Using the same encryption domain behind both of your peers. This is the preferred method.
-   Using a different encryption domain behind each peer.

With the first method, you need to provide the same NAT address behind each of your peers to create a connection path using that address to your server. The path to your server could be the same physical machine or a mirror which provides identical services. With this method, your instance would use the same IP address to connect to your servers regardless of whether your primary or secondary tunnel is active. If you have more than one server, follow this same scheme for your additional servers. This method provides the most transparency to your users and is recommended.

The second method requires configuration in your instance to provide the redundancy. When the tunnel is used for LDAP, for example, you could provide redundant LDAP servers in your instance. Note that this method requires the connection to the first configured LDAP server to timeout before the instance attempts to connect to the secondary server. Because of this additional time delay, this solution should only be implemented if the first option is unattainable. Also note that not all services can be configured for redundantly in your instance. If you are using a VPN tunnel for something other than LDAP and redundancy is required, check that your configuration can support multiple addresses, or see the first option above.

## Alternatives to using a VPN

These alternatives provide a simpler way to connect your instance to the resources in the ServiceNow data centers and provide better encryption. Additionally, you can avoid any issues that VPN downtime might cause, such as making your instance unavailable to users if there is an issue with the VPN tunnel.

-   **Single sign-on and MID server**

    Consider using a combination of Single Sign-On \(SSO\) for authentication and the MID Server for user data synchronization, rather than using a VPN to connect your LDAP server to your instance. For integrations other than LDAP, consider using certificate-based encryption.

    You can use the LDAP listener on a MID server to synchronize your user table in near real time.

    The advantage of this approach is that there are no firewall holes, routes, VPN tunnels, or other special network settings to configure and maintain. The SSO/MID-Server solution is the most flexible, secure, and cost-effective method to achieve the complete LDAP integration.

-   **LDAP over SSL**

    Another alternative to using a VPN tunnel is to configure LDAP Over SSL \(LDAPS\) directly over the Internet. You can configure a read-only domain controller and lock the instance down in your DMZ using only the instance's source addresses and the destination ports of your choice. Since the ports for LDAP are configurable in your instance, you can perform a port address translation \(PAT\) if desired. With LDAPS, you control the certificate that is uploaded over an encrypted channel to the instance, \(see [Uploading a certificate to an instance](../../general/task/t_UploadACertificateToAnInstance.md)\). The packets cannot be encrypted or decrypted without the certificate.

    The advantage of this approach is that it provides a stronger encryption and decryption mechanism. A VPN can only encrypt and decrypt the traffic between the two peers sitting on the Internet with a coordinated pre-shared key, similar to a password. LDAPS provides a longer encrypted path, end-to-end, at the application layer and with a certificate that is far more complicated than a pre-shared key that the IPSec tunnel uses.


## VPN setup

From the time that a VPN request is submitted, it typically takes one week or less to complete the VPN build. To support the redundancy requirements of your instance and your organization, a minimum of two and a maximum of four VPNs are provisioned \(from the active site to your active site or the active site to your DR site, and so on\).

It is good practice for the encryption domain to be as specific as possible. Ideally, the encryption domain would include only the specific hosts that are required for the integrations. A large encryption domain can create opportunities for routing discrepancies \(VPN versus Internet\).

To create the VPN, the instance does the following:

1.  Provides the VPN peer and host addresses from each data center.
2.  Builds the necessary VPN connectivity from two data centers into your network. To support redundancy and disaster recovery \(DR\) requirements, the VPNs can be provisioned from two data centers into two networks.

The instance does not support building multiple VPN tunnels into a customer network for the purpose of connecting to multiple geographic regions or subsidiaries. You should perform any inter-site routing, traffic distribution, or traffic shaping within your own internal network, rather than having multiple VPN tunnels.

