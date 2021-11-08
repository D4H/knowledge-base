# Assigning a Unique Identifier to an Incident

{% hint style="info" %}
Syncing your Incident Management account to[ Incident Reporting](../../../incident-reporting/getting-started.md)? Contact us at support@d4h.org and we will set up the unique identifier feature for you.&#x20;
{% endhint %}

﻿The unique identifiers in Incident Management allow you to quickly assign reference numbers to your [channels](../). Whenever you start a new channel, a reference number will be automatically added to the [Situation](../../situation/) based on the parameters specified in the [Admin Area](../../admin-area/).

﻿To add a reference template, follow the steps below:

* Go to **Settings** in the **Admin Area**
* Select **Preferences**
* Input your reference template under **Incidents**>**Incident Ref Template**

If you have already created a reference template, you can change it by clicking Update ref sequences.\
\
**Ideas for Reference Templates:**

| Template                     | Example Result |
| ---------------------------- | -------------- |
| {sequence,0000}              | 00562          |
| #{sequence,0000}             | #00562         |
| REF#{sequence,0000}          | REF#00562      |
| #{year}-{sequenceByYear,000} | #2021-005      |

{% embed url="https://youtu.be/lwudWl0QOxo" %}

