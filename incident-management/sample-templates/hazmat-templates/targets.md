# Targets

{% hint style="info" %}
This article is part of [sample templates](../) for Incident Management
{% endhint %}

Use the Targets status board to track information about the locations and items you are investigating. Connect it to your [Chemicals ](chemicals.md)status board to record which materials are involved in the incident. Use the map feature to quickly get an overview of target distribution. 

To upload this template into your account, follow the steps on our [Importing Sample Templates](../importing-sample-templates.md) page.

![](<../../../.gitbook/assets/Screen Shot 2021-09-27 at 4.38.40 PM.png>)

![](<../../../.gitbook/assets/Screen Shot 2021-09-27 at 4.39.30 PM.png>)

{% hint style="info" %}
Copy the code below to add this template to your account
{% endhint %}

```
{
  "name": "Targets",
  "nameLabel": "Description",
  "uniq_name": "targets",
  "icon": "fa fa-crosshairs",
  "quickAdd": true,
  "suggestFromCollections": false,
  "layout": [
    {
      "type": "section",
      "rows": [
        {
          "type": "row",
          "items": [
            "position",
            "type"
          ]
        },
        {
          "type": "row",
          "items": [
            "reported_at",
            "reported_by"
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
            "chemical",
            "status"
          ]
        },
        {
          "type": "row",
          "items": [
            "notes"
          ]
        }
      ],
      "name": "Investigation"
    }
  ],
  "fields": {
    "position": {
      "label": "Location",
      "type": "location"
    },
    "type": {
      "label": "Type",
      "type": "select",
      "options": [
        {
          "value": "vehicle",
          "label": "Vehicle"
        },
        {
          "value": "package",
          "label": "Package"
        },
        {
          "value": "bag",
          "label": "Bag"
        },
        {
          "value": "odour",
          "label": "Odor"
        },
        {
          "value": "person",
          "label": "Person"
        },
        {
          "value": "other",
          "label": "Other"
        }
      ]
    },
    "chemical": {
      "label": "Chemical",
      "type": "relationship",
      "relName": "chemicals2targets",
      "thisType": "info_item~targets",
      "otherType": "info_item~chemicals"
    },
    "reported_at": {
      "label": "Reported At",
      "type": "datetime"
    },
    "reported_by": {
      "label": "Reported By",
      "type": "text"
    },
    "status": {
      "label": "Status",
      "type": "select",
      "options": [
        {
          "label": "Reported",
          "value": "reported"
        },
        {
          "value": "investigating",
          "label": "Investigating"
        },
        {
          "value": "closed",
          "label": "Closed"
        }
      ],
      "default": "reported"
    },
    "notes": {
      "label": "Notes",
      "type": "textarea"
    }
  },
  "expressions": {
    "success": "status==='closed'",
    "warning": "status==='investigating'",
    "danger": "status==='reported'"
  },
  "listLayout": {
    "row": [
      "type",
      "reported_at",
      "chemical",
      "status"
    ]
  },
  "headerProperties": [
    "New {{(items: | pick: 'data.status === \\'reported\\'').length }}",
    "Investigating: {{(items | pick: 'data.status === \\'investigating\\'').length }}",
    "Closed: {{(items | pick: 'data.status === \\'closed\\'').length }} of {{items.length }}"
  ],
  "dashboardStats": [
    {
      "label": "Total",
      "value": "{{items.length }}"
    },
    {
      "label": "New",
      "value": "{{(items | pick: 'data.status === \\'reported\\'').length }}"
    },
    {
      "label": "Investigating",
      "value": "{{(items | pick: 'data.status === \\'investigating\\'').length }}"
    }
  ],
  "defaultSortingProperty": "created_date",
  "defaultSortingOrder": "asc",
  "defaultShowOwnItemsOnly": false,
  "defaultShowArchived": false
}
```

