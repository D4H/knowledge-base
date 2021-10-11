# Residents

{% hint style="info" %}
This article is part of [sample templates](../) for Incident Management
{% endhint %}

Use the Residents status board to view contact information for community members affected by the incident. Add the [Shelters](shelters.md) status board to your account as well in order to link your residents to specific shelters. \
\
To upload this template into your account, follow the steps on our [Importing Sample Templates](../importing-sample-templates.md) page.

![](<../../../.gitbook/assets/Screen Shot 2021-09-23 at 1.56.36 PM.png>)

![](<../../../.gitbook/assets/Screen Shot 2021-09-23 at 1.57.20 PM.png>)

{% hint style="info" %}
Copy the code below to add this template to your account
{% endhint %}

```
{
  "name": "Residents",
  "defaultColor": null,
  "nameLabel": "Name",
  "uniq_name": "residents",
  "icon": "fa fa-male",
  "quickAdd": true,
  "suggestFromCollections": false,
  "layout": [
    {
      "type": "section",
      "rows": [
        {
          "type": "row",
          "items": [
            "shelter"
          ]
        }
      ]
    },
    {
      "type": "section",
      "rows": [
        {
          "type": "row",
          "items": [
            "address"
          ]
        },
        {
          "type": "row",
          "items": [
            "phone_number"
          ]
        },
        {
          "type": "row",
          "items": [
            "email_address"
          ]
        }
      ],
      "name": "Contact Details"
    }
  ],
  "fields": {
    "address": {
      "label": "Address",
      "type": "textarea"
    },
    "phone_number": {
      "label": "Phone Number",
      "type": "text"
    },
    "shelter": {
      "label": "Shelter",
      "type": "relationship",
      "thisType": "info_item~residents",
      "relName": "residents2shelters",
      "otherType": "info_item~shelters"
    },
    "email_address": {
      "label": "Email address",
      "type": "email"
    }
  },
  "listLayout": {
    "row": [
      "phone_number",
      "shelter"
    ]
  },
  "defaultSortingProperty": "created_date",
  "defaultSortingOrder": "asc",
  "defaultShowOwnItemsOnly": false,
  "defaultShowArchived": false
}
```



