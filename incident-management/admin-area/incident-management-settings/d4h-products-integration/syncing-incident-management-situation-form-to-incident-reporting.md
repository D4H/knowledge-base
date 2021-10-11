# Syncing Incident Management 'Situation Form' to Incident Reporting

You can sync your [Situation](../../../situation/) form in [Incident Management](../../../getting-started.md) to a draft incident in your [Incident Reporting ](../../../../incident-reporting/getting-started.md)account. Setting up synchronization will reduce duplication of effort. Note that a subscription to both Incident Management and Incident Reporting is required to utilize this feature. 

To set up syncing, go to the [Admin Area ](../../)and follow the steps below:

* Go to **Settings** > D4H **Products Integration**
* Under **D4H Team** click **Select team **and sign into your Incident Reporting account
* Under **Incident Data Synchronization** click** Enable Synchronization**
* Enter your Incident Reporting username and password and click** Login**
* The synchronization is now enabled
* Click **IM Situation <-> IR Incident **to bring up the Situation field mapping options
* Select which fields on the Situation report will be pushed across to the corresponding Incident Reporting fields
* Click** Save**

{% hint style="info" %}
You will first need to add [custom fields](../../../../shared-services/custom-fields/) to your Incident Reporting account to be able to amp the fields across from your Situation
{% endhint %}

Only one member needs to configure the synchronization. Once field mapping has been set up, synchronization will occur automatically. There will no longer be the option to choose what to do with the data when shutting down an incident as the default is now to push it to Incident Reporting as a new draft. 

If adding test incidents to your account, you can choose to turn off the creation of a draft incident report when you initially start a new incident. Expand **Advanced Settings** and check the box to turn off this setting:

![](<../../../../.gitbook/assets/syncing incident report.png>)

Refer to the following field type equivalencies when mapping:\


| ** Incident Management Field Type** | ** Map to Incident Reporting Field Type**      |
| ----------------------------------- | ---------------------------------------------- |
|  Text (single line)                 |  Text                                          |
|  Text Area (multi-line)             |  Text Area                                     |
|  Number                             |  Numeric                                       |
|  Date                               |  Date                                          |
|  Date and Time                      |  Date and Time                                 |
|  Email                              |  Text / Text Area                              |
|  Option Selection                   |  Multiple Choice (Select One)                  |
|  Checkboxes                         |  Multiple Choice (Select Many)                 |
|  Location (map feature)             |  Text / Text Area                              |
|  Area (Map feature)                 |  Currently not possible to map                 |
|  File                               |  Will attach as a file to the incident report  |
|  Relationship                       |  Text / Text Area                              |
|  Table                              |  Currently not possible to map                 |
|  Org                                |  Will attach as a field to the incident report |

{% hint style="info" %}
If you are using the channel 'Status' field on the Situation, you will need to create a custom field for this in your Incident Reporting account. It can be mapped to a text or text area field type. 
{% endhint %}

{% embed url="https://youtu.be/RVkbmCIxPoA" %}

