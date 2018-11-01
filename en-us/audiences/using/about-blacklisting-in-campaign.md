---
title: About blacklisting in Campaign
seo-title: About blacklisting in Campaign
description: About blacklisting in Campaign
seo-description: Blacklisting results in a profile no longer being targeted by any delivery or by deliveries from a specific channel.
page-status-flag: never-activated
uuid: 13fd651c-defe-4227-8a04-8424de228b3f
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/audiences/using/about-blacklisting-in-campaign
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-04-11T07 13 36.599-0400
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: understanding-blacklisting-process
cq-template: /apps/help/templates/article-3
discoiquuid: 0d2880e2-74f8-4a28-a04e-e651bf8ebe7e
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 55.199-0400
jcr-createdby: admin
jcr-description: About blacklisting in Campaign
jcr-ischeckedout: true
jcr-language: en_us
lochandoffdate: 2018-04-11T07 13 36.597-0400
navTitle: About blacklisting in Campaign
publishexternaldate: 2018-03-26
sha1: 74b7e25afff8d46f071b02d44393a63c49e43868
index: y
internal: n
snippet: y
---

# About blacklisting in Campaign

About blacklisting in Campaign

Blacklisting results in a profile no longer being targeted by any delivery or by deliveries from a specific channel.

To give your recipients the ability to be blacklisted (opt-out), you have to create a dedicated landing page. For more on this, refer to [Blacklisting from a landing page](../../audiences/using/blacklisting-process.md#blacklisting-from-a-landing-page).

Recipients can also be blacklisted manually by an operator. For more on this, refer to [Blacklisting from a recipient's profile](../../audiences/using/blacklisting-process.md#blacklisting-from-a-recipient-s-profile).

The profiles whose addresses are blacklisted are automatically excluded during the delivery analysis in order to speed up deliveries (the error rate has a significant effect on delivery speed).

>[!NOTE]
>
>Blacklisting applies to **Profiles**, as opposed to quarantine which is linked to an **email address** or **phone number**. Blacklisting a profile will therefore exclude from deliveries all the addresses linked to it. If a recipient has two profiles in the database, he will still be targeted by deliveries as only one of his profiles is blacklisted. To make sure all his adresses are excluded, add them to the quarantines addresses. For more on this, refer to [this page](../../sending/using/understanding-quarantine-management.md#identifying-quarantined-addresses-for-the-entire-platform).
