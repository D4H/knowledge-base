---
description: >-
  This article explains how to correct the ref sequence in your Incident
  Management account if the numbers are off.
---

# Ref Sequence Error

{% hint style="info" %}
This article only applies if you have [synced](../../admin-area/incident-management-settings/d4h-products-integration/syncing-incident-management-situation-form-to-incident-reporting.md) your Incident Management account to your Incident Reporting account.&#x20;
{% endhint %}

If you notice the ref sequence in your Incident Management account is off, it may be because you have deleted incidents in your [Incident Reporting](broken-reference) account that have not been permanently deleted.&#x20;

To check this you will need to go to your Incident Reporting account and click on **Operations** > **Incidents** > **Deleted Incidents**.&#x20;

If you see deleted incidents here with the refs you want to use for your next incident, you will need to permanently delete these incidents to 'free up' those refs. To do this:

* Click on the incident you wish to permanently delete
* Select **Delete Report** on the right hand side of the page
* Enter your password to confirm the deletion

{% hint style="info" %}
If you permanently delete an incident, there is no way to recover it.&#x20;
{% endhint %}

You will now be able to set what the next ref should be. To do this:

* Go to **Settings** in your Incident Reporting account
* Select **Activities** under the **Modules** section
* Select **Sequence Numbers**
* Under **Next Numbers** you will be able to enter what the next number should be for your incident ref
* Click **Save Changes**
