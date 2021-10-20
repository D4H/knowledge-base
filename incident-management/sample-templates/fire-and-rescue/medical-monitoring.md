# Medical Monitoring

{% hint style="info" %}
This article is part of [sample templates](../) for Incident Management
{% endhint %}

Use the Medical Monitoring status board to record vitals for your firefighters during rehab. Easily select symptoms from the checklist and mark whether they were released to operations, received treatment on-site, or transported to a higher level of care. Depending on what you choose, the row will change color to reflect the severity of the situation. When you are done, mark the form as complete with your signature.&#x20;

To upload this template into your account, follow the steps on our [Importing Sample Templates](../importing-sample-templates.md) page

![](<../../../.gitbook/assets/Screen Shot 2021-10-18 at 3.53.41 PM.png>)

![](<../../../.gitbook/assets/Screen Shot 2021-10-18 at 3.58.43 PM.png>)

{% hint style="info" %}
Copy the code below to add this template to your account
{% endhint %}

```
{
  "name": "Medical Monitoring",
  "nameLabel": "Firefighter Name",
  "uniq_name": "medical_monitoring",
  "icon": "fa fa-medkit",
  "quickAdd": true,
  "suggestFromCollections": false,
  "layout": [
    {
      "type": "section",
      "rows": [
        {
          "type": "row",
          "items": [
            "time_in",
            "time_out"
          ]
        },
        {
          "type": "row",
          "items": [
            "age",
            "gender"
          ]
        },
        {
          "type": "row",
          "items": [
            "vital_signs"
          ]
        },
        {
          "type": "row",
          "items": [
            "alert_and_oriented_normal_gait",
            "complaints_symptoms"
          ]
        },
        {
          "type": "row",
          "items": [
            "next_steps"
          ]
        },
        {
          "type": "row",
          "items": [
            "monitor_name",
            "monitoring_signature"
          ]
        }
      ]
    }
  ],
  "fields": {
    "time_in": {
      "label": "Time entering rehab",
      "type": "datetime"
    },
    "time_out": {
      "label": "Time exiting rehab",
      "type": "datetime"
    },
    "age": {
      "label": "Age",
      "type": "number"
    },
    "gender": {
      "label": "Gender",
      "type": "select",
      "options": [
        {
          "label": "Male",
          "value": "male"
        },
        {
          "value": "female",
          "label": "Female"
        },
        {
          "value": "other",
          "label": "Other"
        }
      ],
      "allowEmpty": true
    },
    "vital_signs": {
      "label": "Vital signs",
      "type": "table",
      "fields": {
        "kxyx0Zjq": {
          "label": "Time",
          "type": "text"
        },
        "HdV0jrMi": {
          "label": "BP",
          "type": "text"
        },
        "fgNeDK2U": {
          "label": "Pulse",
          "type": "text"
        },
        "WrmZFvee": {
          "label": "Respirations",
          "type": "text"
        },
        "rHkdjub8": {
          "label": "SpO2",
          "type": "text"
        },
        "vI6Ro86A": {
          "label": "Temperature",
          "type": "text"
        }
      },
      "layout": {
        "columns": [
          "kxyx0Zjq",
          "HdV0jrMi",
          "fgNeDK2U",
          "WrmZFvee",
          "rHkdjub8",
          "vI6Ro86A"
        ]
      }
    },
    "complaints_symptoms": {
      "label": "Complaints / Symptoms",
      "type": "checkbox",
      "options": [
        {
          "label": "Nausea",
          "value": "nausea"
        },
        {
          "value": "weakness",
          "label": "Weakness"
        },
        {
          "value": "headache",
          "label": "Headache"
        },
        {
          "value": "numbness",
          "label": "Numbness"
        },
        {
          "value": "muscle_pain",
          "label": "Muscle Pain"
        },
        {
          "value": "cramping",
          "label": "Cramping"
        },
        {
          "value": "flushed_skin",
          "label": "Flushed Skin"
        },
        {
          "value": "pale_skin",
          "label": "Pale Skin"
        },
        {
          "value": "clammy_skin",
          "label": "Clammy Skin"
        },
        {
          "value": "blisters",
          "label": "Blisters"
        },
        {
          "value": "short_of_breath",
          "label": "Short of Breath"
        },
        {
          "value": "rapid_heart_rate",
          "label": "Rapid Heart Rate"
        },
        {
          "value": "altered_mental_status",
          "label": "Altered Mental Status"
        },
        {
          "value": "weak_pulse",
          "label": "Weak Pulse"
        },
        {
          "value": "unstable_gait_walk",
          "label": "Unstable gait / walk"
        }
      ]
    },
    "alert_and_oriented_normal_gait": {
      "label": "Alert and oriented, normal gait, clear speech?",
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
      "allowEmpty": true
    },
    "next_steps": {
      "label": "Next steps",
      "type": "select",
      "options": [
        {
          "label": "Released to operations",
          "value": "released_to_operations"
        },
        {
          "value": "received_medical_treatment_on_",
          "label": "Received medical treatment on-site"
        },
        {
          "label": "Transported",
          "value": "transported"
        }
      ],
      "thisType": "info_item~medical_monitoring"
    },
    "monitor_name": {
      "label": "Monitor Name",
      "type": "text"
    },
    "monitoring_signature": {
      "label": "Monitoring signature",
      "type": "signature"
    }
  },
  "expressions": {
    "success": "next_steps==='released_to_operations'",
    "warning": "next_steps==='received_medical_treatment_on_'",
    "danger": "next_steps==='transported'"
  },
  "listLayout": {
    "row": [
      "time_in",
      "time_out",
      "next_steps"
    ]
  },
  "headerProperties": [],
  "dashboardStats": [],
  "defaultSortingProperty": "created_date",
  "defaultSortingOrder": "asc",
  "defaultShowOwnItemsOnly": false,
  "defaultShowArchived": false
}
```
