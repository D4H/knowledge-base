# Air Monitoring

{% hint style="info" %}
This article is part of [sample templates](../) for Incident Management
{% endhint %}

Use the Air Monitoring status board to record results of air quality investigations during chemical incidents. Use the map feature to view the locations in comparison to each other. Record the name and position of the staff members responsible for that area. Import sensor readings into the table located on the form for that area. 

To upload this template into your account, follow the steps on our [Importing Sample Templates](../importing-sample-templates.md) page.

![](<../../../.gitbook/assets/Screen Shot 2021-09-27 at 4.21.49 PM.png>)

![](<../../../.gitbook/assets/Screen Shot 2021-09-27 at 4.22.29 PM.png>)

{% hint style="info" %}
Copy the code below to add this template to your account
{% endhint %}

```
{
  "name": "Air Monitoring",
  "defaultColor": null,
  "nameLabel": "Operating Area",
  "nameTemplate": "Area {counter}",
  "uniq_name": "air_monitoring",
  "icon": "fa fa-fire",
  "quickAdd": true,
  "suggestFromCollections": false,
  "layout": [
    {
      "type": "section",
      "rows": [
        {
          "type": "row",
          "items": [
            "start_time",
            "finish_time"
          ]
        },
        {
          "type": "row",
          "items": [
            "location"
          ]
        },
        {
          "type": "row",
          "items": [
            "readings"
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
            "name",
            "position"
          ]
        }
      ]
    }
  ],
  "fields": {
    "start_time": {
      "label": "Start Time",
      "type": "datetime"
    },
    "finish_time": {
      "label": "Finish Time",
      "type": "datetime"
    },
    "readings": {
      "label": "Readings",
      "type": "table",
      "fields": {
        "meter": {
          "label": "Sensor",
          "type": "select",
          "options": [
            {
              "label": "Oxygen",
              "value": "oxygen"
            },
            {
              "value": "co",
              "label": "CO"
            },
            {
              "value": "voc",
              "label": "VOC"
            },
            {
              "value": "lel",
              "label": "LEL"
            }
          ],
          "default": null
        },
        "alarm": {
          "label": "Alarm",
          "type": "select",
          "options": [
            {
              "label": "Yes",
              "value": "yes"
            },
            {
              "value": "no",
              "label": "No"
            }
          ],
          "default": null
        },
        "level": {
          "label": "Level",
          "type": "text"
        }
      },
      "layout": {
        "columns": [
          "meter",
          "alarm",
          "level"
        ]
      }
    },
    "location": {
      "label": "Location",
      "type": "location"
    },
    "status": {
      "label": "Status",
      "type": "select",
      "options": [
        {
          "label": "Normal",
          "value": "normal"
        },
        {
          "value": "reportable",
          "label": "Reportable"
        },
        {
          "value": "warning_danger",
          "label": "Warning / Danger"
        }
      ],
      "default": "",
      "allowEmpty": true
    },
    "name": {
      "label": "Name",
      "type": "text"
    },
    "position": {
      "label": "Position",
      "type": "text"
    }
  },
  "expressions": {
    "success": "status==='normal'",
    "warning": "status==='reportable'",
    "danger": "status==='warning_danger'"
  },
  "listLayout": {
    "row": [
      "start_time",
      "finish_time",
      "status"
    ]
  },
  "headerProperties": [],
  "defaultSortingProperty": "created_date",
  "defaultSortingOrder": "asc",
  "defaultShowOwnItemsOnly": false,
  "defaultShowArchived": false
}
```

