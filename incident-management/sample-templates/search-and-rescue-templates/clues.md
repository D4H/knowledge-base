# Clues

{% hint style="info" %}
This article is part of [sample templates](../) for Incident Management
{% endhint %}

Use the Clues template to track clues found in the field. Mark their location on the map, record actions taken, and upload a photo. Assign the clues a relevancy rating \(high, medium, or low\) and quickly see their priority for follow-up searches.   
  
To upload this template into your account, follow the steps on our [Importing Sample Templates](../importing-sample-templates.md) page.

![](../../../.gitbook/assets/e5f0d097-19ce-48ae-b996-294515606ec2%20%281%29.png)

![](../../../.gitbook/assets/af1b5d5c-6267-4a5e-8510-a8db9c8b7c42%20%281%29.png)

{% hint style="info" %}
Copy the code below to add this template to your account
{% endhint %}

```text
{
  "name": "Clues",
  "defaultColor": null,
  "nameLabel": "Clue Found",
  "uniq_name": "clues",
  "icon": "fa fa-star",
  "quickAdd": false,
  "layout": [
    {
      "type": "section",
      "rows": [
        {
          "type": "row",
          "items": [
            "photo",
            "location"
          ]
        },
        {
          "type": "row",
          "items": [
            "relevancy",
            "date_found"
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
            "action_taken"
          ]
        }
      ]
    }
  ],
  "fields": {
    "photo": {
      "label": "Photo",
      "type": "file"
    },
    "location": {
      "label": "Location",
      "type": "location"
    },
    "relevancy": {
      "label": "Relevancy",
      "type": "select",
      "options": [
        {
          "label": "High",
          "value": "high"
        },
        {
          "value": "medium",
          "label": "Medium"
        },
        {
          "value": "low",
          "label": "Low"
        }
      ],
      "default": null
    },
    "date_found": {
      "label": "Time Found",
      "type": "datetime"
    },
    "action_taken": {
      "label": "Action Taken With Clue",
      "type": "textarea"
    }
  },
  "expressions": {
    "danger": "relevancy==='high'",
    "success": "relevancy==='low'",
    "warning": "relevancy==='medium'"
  },
  "listLayout": {
    "row": [
      "date_found",
      "relevancy"
    ]
  }
}
```

