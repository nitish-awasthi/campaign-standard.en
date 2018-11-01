---
title: Understanding quarantine management
seo-title: Understanding quarantine management
description: Understanding quarantine management
seo-description: Learn how to optimize your deliverability with quarantine management.
uuid: 2904f2b0-7ef6-47af-b63d-7f8cb4567344
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/sending/using/understanding-quarantine-management
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-30T04 53 59.824-0400
cq-lastreplicated: 2018-07-23T06 02 30.472-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: monitoring-messages
cq-template: /apps/help/templates/article-3
discoiquuid: 17e16116-971f-48e3-a8c5-63d53964fce4
firstPublishExternalDate: 2018-07-23T06:02:30.437-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 01 23.575-0400
jcr-createdby: admin
jcr-description: Understanding quarantine management
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T06:02:30.437-0400
lochandoffdate: 2018-07-30T04 53 59.824-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Understanding quarantine management
publishexternaldate: 2018-07-23T06 02 30.437-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/sending/using/understanding-quarantine-management.html
sha1: 26a1f3f834f6e53725efe41f236c77c0a870560f
topicBrowsingSortDate: 2018-07-23T06:02:30.437-0400
index: y
internal: n
snippet: y
---

# Understanding quarantine management

Understanding quarantine management

## <p>About quarantines</p>

An email address or a phone number can be quarantined, for example, when the mailbox is full or if the address does not exist.

In any case, the quarantine procedure complies with specific rules described in this [section](../../sending/using/understanding-quarantine-management.md#conditions-for-sending-an-address-to-quarantine).

### <p>Optimizing your delivery through quarantines</p>

The profiles whose email addresses or phone number are in quarantine are automatically excluded during message preparation (see [Identifying quarantined addresses for a delivery](../../sending/using/understanding-quarantine-management.md#identifying-quarantined-addresses-for-a-delivery)). This will speed up deliveries, as the error rate has a significant effect on delivery speed.

Some internet access providers automatically consider emails to be spam if the rate of invalid addresses is too high. Quarantine therefore allows you to avoid blacklisting by these providers.

Moreover, quarantines help reducing SMS sending costs by excluding erroneous phone numbers from deliveries.

For more on best practices to secure and optimize your deliveries, refer to [this page](https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_DeliveryBestPractices.html).

### <p>Quarantine vs blacklisting</p>

**Quarantine** applies only to an address, not the profile itself. It means that, if two profiles have the same email address, they will both be affected if the address is quarantined.

Likewise, a profile whose email address is quarantined could update his profile and enter a new address, and could then be targeted by delivery actions again.

**Blacklisting**, on the other hand, will result in the profile no longer being targeted by any delivery, for example after an unsubscription (opt-out). For more on the blacklisting process, refer to [Managing blacklisting in Campaign](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md).

>[!NOTE]
>
>When a user replies to an SMS message with a keyword such as "STOP" in order to opt-out from SMS deliveries, his profile is not blacklisted like in the email opt-out process. The profile phone number is sent to quarantine with the **Blacklisted** status. This status refers to the phone number only, the profile is not blacklisted so that the user continues receiving email messages. For more on this, refer to [this section](../../channels/using/managing-incoming-sms.md#managing-stop-sms).

## <p>Identifying quarantined addresses</p>

Quarantined addresses can be listed for a specific delivery or for the entire platform.

>[!NOTE]
>
>If you need to remove an address from quarantine, contact your technical administrator.

### <p>Identifying quarantined addresses for a delivery</p>

Quarantined addresses for a specific delivery are listed during the delivery preparation phase, in the **Exclusion logs** tab of the delivery dashboard (see [this section](../../sending/using/monitoring-a-delivery.md#exclusion-logs)). For more on delivery preparation, refer to [this section](../../sending/using/preparing-the-send.md).

![](assets/exclusion_logs.png)

### <p>Identifying quarantined addresses for the entire platform</p>

Administrators can list the addresses in quarantine for the entire platform from the **Administration > Channels > Quarantines > Addresses** menu.

>[!NOTE]
>
>This menu lists quarantined elements for **email**, **SMS** and **Push notification** channels.

![](assets/quarantines1.png)

>[!NOTE]
>
>The increase in number of quarantines is a normal effect, related to the "wear and tear" of the database. For example, if the lifetime of an email address is considered to be three years and the recipient table increases by 50% each year, the increase in quarantines can be calculated as follows: End of Year 1: (1&#42;0.33)/(1+0.5)=22%. End of Year 2: ((1.22&#42;0.33)+0.33)/(1.5+0.75)=32.5%.

## <p>Conditions for sending an address to quarantine</p>

Adobe Campaign manages quarantine according to the delivery failure type and the reason assigned during error messages qualification (see [Delivery failure types and reasons](../../sending/using/understanding-delivery-failures.md#delivery-failure-types-and-reasons) and [Bounce mail qualification](../../sending/using/understanding-delivery-failures.md#bounce-mail-qualification)).

* **Ignored error**: ignored errors do not send an address to quarantine.
* **Hard error**: the corresponding email address is immediately sent to quarantine. 
* **Soft error**: soft errors do not send immediately an address to quarantine, but they increment an error counter. When the error counter reaches the limit threshold, the address goes into quarantine. In the default configuration, the threshold is set at five errors, where two errors are significant if they occur at least 24 hours apart. The address is placed in quarantine at the sixth error. The error counter threshold can be modified. For more on this, refer to [Retries after a delivery failure](../../sending/using/understanding-delivery-failures.md#retries-after-a-delivery-failure).

  When a delivery is successful after a retry, the error counter of the address which was prior to that quarantined is reinitialized. The address status changes to **Valid** and it is deleted from the list of quarantines after two days by the **Database cleanup** workflow.

If a user qualifies an email as a spam (**Feedback loop**), the message is automatically redirected towards a technical mailbox managed by Campaign. The user's email address is then automatically sent to quarantine with the **Blacklisted** status. This status refers to the address only, the profile is not blacklisted, so that the user continues receiving SMS messages and push notifications.

In the list of quarantined addresses (see [Identifying quarantined addresses for the entire platform](../../sending/using/understanding-quarantine-management.md#identifying-quarantined-addresses-for-the-entire-platform)), the **Error reason** field indicates why the selected address was placed in quarantine.

![](assets/quarantines2.png)
