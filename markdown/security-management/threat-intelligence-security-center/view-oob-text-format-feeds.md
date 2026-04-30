---
title: View Text Feeds
description: View the text Feeds that are configured in the base system.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [View Threat Intel Feeds, Threat Intelligence Feeds, Integrate Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# View Text Feeds

View the text Feeds that are configured in the base system.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click on **Integrations** icon.

3.  Select **Text** option.

    The following lists the configured text feeds within the base system.

    |Threat Feed|Description|URL|
    |-----------|-----------|---|
    |Haley's Brute Force IPs|Provides a list of attacking machine IP addresses during the last 2 years sorted by IP address|[http://charles.the-haleys.org/ssh\_dico\_attack\_hdeny\_format.php/hostsdeny.txt](http://charles.the-haleys.org/ssh_dico_attack_hdeny_format.php/hostsdeny.txt)|
    |Blockrules Emergingthreats|Emerging Threat \(ET\) Intelligence provides actionable threat intel feeds to identify IPs involved in suspicious and malicious activity.|[https://rules.emergingthreats.net/blockrules/compromised-ips.txt](https://rules.emergingthreats.net/blockrules/compromised-ips.txt)|
    |Nuug Pop3 Groper Web|List of hosts that have tried and failed to log on to the pop3 service at bsdly.net.|[https://home.nuug.no/%7Epeter/pop3gropers.txt](https://home.nuug.no/%7Epeter/pop3gropers.txt)|
    |Tor Exit Nodes|Tor Exit Nodes can be used to detect traffic coming from the TOR network.|[https://www.dan.me.uk/torlist/?exit](https://www.dan.me.uk/torlist/?exit)|
    |Talos Intelligence IP Blacklist|Talos was formed by combining SourceFire’s Vulnerability Research Team, the Cisco Threat Research and Communications group, and the Cisco Secure Applications Group. The combined expertise is backed by a sophisticated infrastructure, and Cisco’s unrivaled telemetry of data that spans across networks, endpoints, cloud environments, virtual systems, and daily web and email traffic.|[https://www.talosintelligence.com/documents/ip-blacklist](https://www.talosintelligence.com/documents/ip-blacklist)|
    |SANS|ISC provides a free analysis and warning service to thousands of Internet users and organizations.|[https://isc.sans.edu/feeds/topips.txt](https://isc.sans.edu/feeds/topips.txt)|
    |Snort|Snort is the foremost Open Source Intrusion Prevention System \(IPS\) in the world. Snort IPS uses a series of rules that help define malicious network activity.|[https://snort.org/downloads/ip-block-list](https://snort.org/downloads/ip-block-list)|
    |CI army|The CINS Army list is a subset of the CINS Active Threat Intelligence ruleset, and consists of IP addresses that meet one of two basic criteria: 1\) The IP's recent Rogue Packet score factor is very poor, or 2\) The IP has tripped a designated number of 'trusted' alerts across a given number of their Sentinels deployed around the world.|[https://cinsscore.com/list/ci-badguys.txt](https://cinsscore.com/list/ci-badguys.txt)|
    |Proofpoint|Raw IPs for the firewall block lists. These come from: Spam nets identified by Spamhaus \(www.spamhaus.org\), Top Attackers listed by DShield \(www.dshield.org\) and Abuse.ch|[https://rules.emergingthreats.net/fwrules/emerging-Block-IPs.txt](https://rules.emergingthreats.net/fwrules/emerging-Block-IPs.txt)|
    |Blocklist Greensnow|GreenSnow is a team consisting of the best specialists in computer security, GreenSnow harvests a large number of IPs from different computers located around the world.GreenSnow is comparable with SpamHaus.org for attacks of any kind except for spam.|[https://blocklist.greensnow.co/greensnow.txt](https://blocklist.greensnow.co/greensnow.txt)|
    |CI army|The CINS Army list is a subset of the CINS Active Threat Intelligence ruleset, and consists of IP addresses that meet one of two basic criteria: 1\) The IP's recent Rogue Packet score factor is very poor, or 2\) The IP has tripped a designated number of 'trusted' alerts across a given number of their Sentinels deployed around the world.|[https://cinsscore.com/list/ci-badguys.txt](https://cinsscore.com/list/ci-badguys.txt)|
    |Blocklist|www.blocklist.de is a free and voluntary service provided by a Fraud/Abuse-specialist, whose servers are often attacked via SSH-, Mail-Login-, FTP-, Webserver- and other services.|[https://lists.blocklist.de/lists/all.txt](https://lists.blocklist.de/lists/all.txt)|
    |Tor Exit Nodes|Tor Exit Nodes can be used to detect traffic coming from the TOR network.|[https://www.dan.me.uk/torlist/?exit](https://www.dan.me.uk/torlist/?exit)|
    |Botscout BOT IPs|BotScout helps prevent automated web scripts, known as "bots", from registering on forums, polluting databases, spreading spam, and abusing forms on web sites.|[http://botscout.com/last\_caught\_cache.txt](http://botscout.com/last_caught_cache.txt)|
    |Dataplane VNC RFB|IP addresses identified as initiating VNC remote frame buffer sessions.|[https://dataplane.org/signals/vncrfb.txt](https://dataplane.org/signals/vncrfb.txt)|
    |Dataplane TELNET login|IP addresses identified as attempting login via TELNET password authentication.|[https://dataplane.org/signals/telnetlogin.txt](https://dataplane.org/signals/telnetlogin.txt)|
    |Dataplane SSH password authentication|IP addresses identified as attempting login via SSH password authentication.|[https://dataplane.org/signals/sshpwauth.txt](https://dataplane.org/signals/sshpwauth.txt)|
    |Dataplane SSH client connection|IP addresses identified as performing SSH client protocol negotiations.|[https://dataplane.org/signals/sshclient.txt](https://dataplane.org/signals/sshclient.txt)|
    |Blockrules Emergingthreats|Emerging Threat \(ET\) Intelligence provides actionable threat intel feeds to identify IPs involved in suspicious and malicious activity.|[https://rules.emergingthreats.net/blockrules/compromised-ips.txt](https://rules.emergingthreats.net/blockrules/compromised-ips.txt)|
    |Dataplane SMTP greeting|IP addresses identified as SMTP clients issuing unsolicited HELO or EHLO commands.|[https://dataplane.org/signals/smtpgreet.txt](https://dataplane.org/signals/smtpgreet.txt)|
    |Dataplane SIP query|IP addresses identified as sending SIP OPTIONS queries.|[https://dataplane.org/signals/sipquery.txt](https://dataplane.org/signals/sipquery.txt)|
    |Dataplane IP protocol 41|IP addresses identified as open IPv4 protocol 41 relay \(i.e. IPv6 over IPv4\).|[https://dataplane.org/signals/proto41.txt](https://dataplane.org/signals/proto41.txt)|
    |Dataplane SIP invitation|IP addresses identified as sending SIP INVITE operations.|[https://dataplane.org/signals/sipinvitation.txt](https://dataplane.org/signals/sipinvitation.txt)|
    |Dataplane DNS CH TXT version.bind|IP addresses identified as sending DNS CH TXT VERSION.BIND queries.|[https://dataplane.org/signals/dnsversion.txt](https://dataplane.org/signals/dnsversion.txt)|
    |Dataplane DNS TCP|IP addresses identified as sending DNS over TCP port 53 queries.|[https://dataplane.org/signals/dnstcp.txt](https://dataplane.org/signals/dnstcp.txt)|
    |Dataplane DNS recursion desired IN ANY|IP addresses identified as sending recursive DNS IN ANY queries.|[https://dataplane.org/signals/dnsrdany.txt](https://dataplane.org/signals/dnsrdany.txt)|
    |Dataplane DNS recursion desired|IP addresses identified as sending recursive DNS queries.|[https://dataplane.org/signals/dnsrd.txt](https://dataplane.org/signals/dnsrd.txt)|
    |Phishing Database from GitHub Active Phishing Links|Data source for fetching Active Phishing Links from Phishing Database available on Github.|[https://raw.githubusercontent.com/mitchellkrogza/Phishing.Database/master/phishing-links-ACTIVE.txt](https://raw.githubusercontent.com/mitchellkrogza/Phishing.Database/master/phishing-links-ACTIVE.txt)|
    |Phishing Database from GitHub Active Domains|Data source for fetching Active Domains from Phishing Database available on Github.|[https://raw.githubusercontent.com/mitchellkrogza/Phishing.Database/master/phishing-domains-ACTIVE.txt](https://raw.githubusercontent.com/mitchellkrogza/Phishing.Database/master/phishing-domains-ACTIVE.txt)|
    |Phishing Database from GitHub Active IPs|Data source for fetching Active IPs from Phishing Database available on Github.|[https://raw.githubusercontent.com/mitchellkrogza/Phishing.Database/master/phishing-IPs-ACTIVE.txt](https://raw.githubusercontent.com/mitchellkrogza/Phishing.Database/master/phishing-IPs-ACTIVE.txt)|
    |Blocklist Bots|All IP addresses which have been reported within the last 48 hours as having run attacks attacks on the RFI-Attacks, REG-Bots, IRC-Bots or BadBots.|[https://lists.blocklist.de/lists/bots.txt](https://lists.blocklist.de/lists/bots.txt)|
    |Blocklist Apache Attacks|All IP addresses which have been reported within the last 48 hours as having run attacks on the service Apache, Apache-DDOS, RFI-Attacks.|[https://lists.blocklist.de/lists/apache.txt](https://lists.blocklist.de/lists/apache.txt)|
    |Voip Blacklist By Scopserv|Retrieve list of blocklisted ips from the Voip Blacklist.|[http://voipbl.org/update/?dm=bl](http://voipbl.org/update/?dm=bl)|
    |Threatview Domain Blocklist|Malicious Domains identified for phishing/serving malware/command and control.|[https://threatview.io/Downloads/DOMAIN-High-Confidence-Feed.txt](https://threatview.io/Downloads/DOMAIN-High-Confidence-Feed.txt)|
    |Threatview MD5 Hash Blocklist|MD5 hashes of malicious files or associated with - malware, ransomware, hack tools, bots etc.|[https://threatview.io/Downloads/MD5-HASH-ALL.txt](https://threatview.io/Downloads/MD5-HASH-ALL.txt)|
    |Threatview URL Blocklist|Malicious URL's serving malware, phishing, botnets and C2.|[https://threatview.io/Downloads/URL-High-Confidence-Feed.txt](https://threatview.io/Downloads/URL-High-Confidence-Feed.txt)|
    |Threatview SHA File Hash Blocklist|SHA hashes of files known or linked with malware execution.|[https://threatview.io/Downloads/SHA-HASH-FEED.txt](https://threatview.io/Downloads/SHA-HASH-FEED.txt)|
    |Threatview IP Blocklist|Malicious IP Blocklist for known Bad IP addresses.|[https://threatview.io/Downloads/IP-High-Confidence-Feed.txt](https://threatview.io/Downloads/IP-High-Confidence-Feed.txt)|
    |Threatview C2 Hunt Feed|Infrastructure hosting Command and Control Servers found during Proactive Hunt by Threatview.io|[https://threatview.io/Downloads/High-Confidence-CobaltStrike-C2%20-Feeds.txt](https://threatview.io/Downloads/High-Confidence-CobaltStrike-C2%20-Feeds.txt)|
    |Threatview OSINT Threat Feed|Malicious indicators of compromise gathered from OSINT Source - Twitter and Pastebin.|[https://threatview.io/Downloads/Experimental-IOC-Tweets.txt](https://threatview.io/Downloads/Experimental-IOC-Tweets.txt)|

4.  Click **Edit** to edit the feed.


**Parent Topic:**[View Threat Intel Feeds](../concept/base-system-threat-intel-feeds.md)

