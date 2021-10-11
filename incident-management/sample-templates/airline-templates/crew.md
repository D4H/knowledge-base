# Crew

{% hint style="info" %}
This article is part of [sample templates](../) for Incident Management
{% endhint %}

Use the Crew status board to track injuries and fatalities during an incident. Record which hospitals your crew members are being treated at by linking to a medical facilities status board. Easily access the crew member's emergency contact details to keep their family updated. \
\
To upload this template into your account, follow the steps on our [Importing Sample Templates](../importing-sample-templates.md) page.

![](<../../../.gitbook/assets/Screen Shot 2021-09-22 at 11.10.05 AM.png>)

![](<../../../.gitbook/assets/Screen Shot 2021-09-22 at 11.10.30 AM.png>)

{% hint style="info" %}
Copy the code below to add this template to your account
{% endhint %}

```
{
  "name": "Crew",
  "defaultColor": null,
  "nameLabel": "Name",
  "uniq_name": "crew",
  "icon": "fa fa-group",
  "quickAdd": false,
  "suggestFromCollections": false,
  "layout": [
    {
      "type": "section",
      "rows": [
        {
          "type": "row",
          "items": [
            "position",
            "emergency_contact_details",
            "date_of_birth"
          ]
        },
        {
          "type": "row",
          "items": [
            "photos"
          ]
        },
        {
          "type": "row",
          "items": [
            "nationality",
            "years_flying",
            "last_training_check"
          ]
        },
        {
          "type": "row",
          "items": [
            "other_information",
            "email"
          ]
        }
      ],
      "name": "Basic Details"
    },
    {
      "type": "section",
      "rows": [
        {
          "type": "row",
          "items": [
            "status",
            "location"
          ]
        },
        {
          "type": "row",
          "items": [
            "hospital",
            "notes"
          ]
        }
      ],
      "name": "Current Status"
    }
  ],
  "fields": {
    "position": {
      "label": "Position",
      "type": "select",
      "options": [
        {
          "label": "Captain",
          "value": "captain"
        },
        {
          "label": "First Officer",
          "value": "first_officer"
        },
        {
          "label": "Second Officer",
          "value": "second_officer"
        },
        {
          "label": "Cabin Crew",
          "value": "cabin_crew"
        },
        {
          "label": "Engineer",
          "value": "engineer"
        },
        {
          "value": "other",
          "label": "Other"
        }
      ],
      "default": null
    },
    "emergency_contact_details": {
      "label": "Emergency Contact Details",
      "type": "text"
    },
    "status": {
      "label": "Injuries",
      "type": "select",
      "options": [
        {
          "label": "Uninjured",
          "value": "uninjured"
        },
        {
          "label": "Minor Injuries",
          "value": "minor"
        },
        {
          "label": "Serious Injuries",
          "value": "serious"
        },
        {
          "label": "Life Threatening Injuries",
          "value": "life_threatening"
        },
        {
          "label": "Deceased",
          "value": "deceased"
        }
      ],
      "default": null
    },
    "location": {
      "label": "Current Location",
      "type": "select",
      "options": [
        {
          "label": "Aircraft",
          "value": "aircraft"
        },
        {
          "label": "Hospital",
          "value": "hospital"
        },
        {
          "label": "Airport",
          "value": "airport"
        },
        {
          "label": "Passenger Holding",
          "value": "holding"
        },
        {
          "label": "Morgue",
          "value": "morgue"
        },
        {
          "label": "Released",
          "value": "released"
        },
        {
          "label": "Hotel",
          "value": "hotel"
        }
      ],
      "default": null
    },
    "photos": {
      "label": "Photo",
      "type": "file",
      "hint": "Not-approved for media release."
    },
    "nationality": {
      "label": "Nationality",
      "type": "text"
    },
    "years_flying": {
      "label": "Years Flying",
      "type": "text"
    },
    "last_training_check": {
      "label": "Last Training Check",
      "type": "date"
    },
    "other_information": {
      "label": "Other Information",
      "type": "text"
    },
    "email": {
      "label": "Email",
      "type": "email",
      "isContact": true
    },
    "date_of_birth": {
      "label": "Date Of Birth",
      "type": "date",
      "hint": "date"
    },
    "hospital": {
      "label": "Medical Facility",
      "type": "relationship",
      "thisType": "info_item~crew",
      "relName": "crew2hospital",
      "otherType": "info_item~hospitals"
    },
    "notes": {
      "label": "Notes",
      "type": "text"
    }
  },
  "expressions": {
    "success": "status===\"uninjured\"",
    "warning": "status===\"life_threatening\" || status===\"serious\" || status===\"minor\"",
    "danger": "status===\"deceased\""
  },
  "listLayout": {
    "row": [
      "position",
      "status",
      "location",
      "hospital",
      "notes"
    ]
  },
  "cardLayout": {},
  "headerProperties": [
    "Deceased: {{(items | pick: 'data.status === \\'deceased\\'').length }}",
    "Life Threat: {{(items | pick: 'data.status === \\'life_threatening\\'').length }}",
    "Serious Injuries: {{(items | pick: 'data.status === \\'serious\\'').length }}",
    "Minor Injuries: {{(items | pick: 'data.status === \\'minor\\'').length }}",
    "Total: {{ items.length }}"
  ],
  "dashboardStats": [
    {
      "label": "Deceased",
      "value": "{{(items | pick: 'data.status === \\'deceased\\'').length }}",
      "dangerStatus": "(items | pick: 'data.status === \\'deceased\\'').length > 0"
    },
    {
      "label": "Life Threat",
      "value": "{{(items | pick: 'data.status === \\'life_threatening\\'').length }}",
      "warningStatus": "(items | pick: 'data.status === \\'life_threatening\\'').length > 0"
    },
    {
      "label": "Serious Injuries",
      "value": "{{(items | pick: 'data.status === \\'serious\\'').length }}",
      "warningStatus": "(items | pick: 'data.status === \\'serious\\'').length > 0"
    },
    {
      "label": "Minor Injuries",
      "value": "{{(items | pick: 'data.status === \\'minor\\'').length }}",
      "warningStatus": "(items | pick: 'data.status === \\'minor\\'').length > 0"
    },
    {
      "label": "Uninjured",
      "value": "{{(items | pick: 'data.status === \\'uninjured\\'').length }}",
      "successStatus": "(items | pick: 'data.status === \\'uninjured\\'').length > 0"
    }
  ],
  "dashboardStatus": {
    "success": "(items | pick:'data.status===\\'\\'').length>0",
    "warning": "(items | pick:'data.status!=\\'\\'').length>0",
    "danger": "(items | pick:'data.status===\\'deceased\\'').length>0"
  },
  "defaultSortingProperty": "created_date",
  "defaultSortingOrder": "asc",
  "defaultShowOwnItemsOnly": false,
  "defaultShowArchived": false
}
```
