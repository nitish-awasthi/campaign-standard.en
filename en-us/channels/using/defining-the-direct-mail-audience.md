---
title: Defining the direct mail audience
seo-title: Defining the direct mail audience
description: Defining the direct mail audience
seo-description: Learn how to define the target for your direct mail delivery.
uuid: ca9ba068-4102-475a-9b3d-2c758c4d16da
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/defining-the-direct-mail-audience
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-30T04 54 03.803-0400
cq-lastreplicated: 2018-07-23T06 02 56.752-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: direct-mail
cq-template: /apps/help/templates/article-3
discoiquuid: 7a8a4bd9-6f6e-42da-a949-6f69cd5d88f7
firstPublishExternalDate: 2018-07-23T06:02:56.722-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 40.462-0400
jcr-createdby: admin
jcr-description: Defining the direct mail audience
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T06:02:56.722-0400
lochandoffdate: 2018-07-30T04 54 03.803-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Defining the direct mail audience
publishexternaldate: 2018-07-23T06 02 56.722-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/channels/using/defining-the-direct-mail-audience.html
sha1: 686c28e1994d5ffd520dcceff7835cc6a890d226
topicBrowsingSortDate: 2018-07-23T06:02:56.722-0400
index: y
internal: n
snippet: y
---

# Defining the direct mail audience

Defining the direct mail audience

You can either define the audience in the creation wizard or by clicking on the **Audience** section of the delivery dashboard.

![](assets/direct_mail_15.png)

## <p>Defining the main target</p>

For direct mail, the targeted profiles are the ones that will be included in the extraction file that you will send to your direct mail provider.

For each targeted profile a new line is added in the extraction file. The amount of profile information that will be included for each recipient is defined in the [Defining the extraction](../../channels/using/defining-the-direct-mail-content.md#defining-the-extraction) screen.

>[!CAUTION]
>
>Make sure that your profiles include a postal address as this information is essential to the direct mail provider. Also make sure you have checked the **Address specified** box in your profiles' information. See [Recommendations](../../channels/using/about-direct-mail.md#recommendations).

## <p>Adding test and trap profiles</p>

Add test profiles so that you can test your file with a small number of profiles. It allows you to quickly create a file sample to test and validate the structure before preparing the actual file. Refer to [Managing test profiles and sending proofs](../../sending/using/managing-test-profiles-and-sending-proofs.md).

The use of traps is essential to direct mail deliveries. For instance, they allow you to verify that your direct mail provider is really sending the communication and that they are not sending your client list to another provider.

For direct mail deliveries, traps are added during extraction and mixed in the output document. By default, they are inserted in the sorting order of the output file, but you can choose to insert them at the end or the beginning of the file (**Trap insertion mode** tab).