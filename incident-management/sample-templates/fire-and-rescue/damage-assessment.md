# Damage Assessment

{% hint style="info" %}
This article is part of [sample templates](../) for Incident Management
{% endhint %}

Use the Damage Assessment status board to record the impact of incidents on the structural integrity of the buildings in your area. Mark the area that the building is in and it will appear in different colors on the map depending on its status (green for no damage, orange for minor damage, and red for severe damage or destroyed). Add additional information about the damage on the form located behind the status board row. You can also attach a photo taken of the building in the field to share with command staff in base.&#x20;

To upload this template into your account, follow the steps on our [Importing Sample Templates](../importing-sample-templates.md) page.

![](<../../../.gitbook/assets/Screen Shot 2021-10-18 at 3.26.41 PM.png>)

![](<../../../.gitbook/assets/Screen Shot 2021-10-18 at 3.29.45 PM.png>)



{% hint style="info" %}
Copy the code below to add this template to your account
{% endhint %}

```
{
  "name": "Damage Assessment",
  "defaultColor": null,
  "nameLabel": "Name",
  "nameTemplate": "",
  "uniq_name": "damage_assessment",
  "icon": "fa fa-exclamation-triangle",
  "quickAdd": true,
  "suggestFromCollections": false,
  "layout": [
    {
      "type": "section",
      "rows": [
        {
          "type": "row",
          "items": [
            "area"
          ]
        },
        {
          "type": "row",
          "items": [
            "status"
          ]
        },
        {
          "type": "row",
          "items": [
            "damage_description",
            "photos"
          ]
        }
      ]
    }
  ],
  "fields": {
    "status": {
      "label": "Status",
      "type": "select",
      "options": [
        {
          "label": "No Damage",
          "value": "no_damage"
        },
        {
          "value": "minor_damage",
          "label": "Minor Damage"
        },
        {
          "value": "severe_damage",
          "label": "Severe Damage"
        },
        {
          "value": "destroyed",
          "label": "Destroyed"
        }
      ],
      "default": "",
      "allowEmpty": true
    },
    "damage_description": {
      "label": "Damage Description",
      "type": "textarea"
    },
    "photos": {
      "label": "Photos",
      "type": "file",
      "multiple": true
    },
    "area": {
      "label": "Area",
      "type": "mapArea"
    }
  },
  "expressions": {
    "success": "status==='no_damage'",
    "warning": "status==='minor_damage'",
    "danger": "status==='severe_damage' || status==='destroyed'"
  },
  "listLayout": {
    "row": [
      "status"
    ]
  },
  "defaultSortingProperty": "created_date",
  "defaultSortingOrder": "asc",
  "defaultShowOwnItemsOnly": false,
  "defaultShowArchived": false
}
```
