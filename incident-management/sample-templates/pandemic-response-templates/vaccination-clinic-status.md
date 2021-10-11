# Vaccination Clinic Status

{% hint style="info" %}
This article is part of [sample templates](../) for Incident Management
{% endhint %}

Use the Vaccination Clinic Status status board to track the daily number of doses administered at different clinics. Record how many appoints you have booked to anticipate future needs. Write comments about the daily numbers to share with your team. This template can be customized in the admin area to match the kind of outbreak to which you are responding. 

To upload this template into your account, follow the steps on our [Importing Sample Templates](../importing-sample-templates.md) page.

![](<../../../.gitbook/assets/Screen Shot 2021-09-27 at 3.45.21 PM.png>)

![](<../../../.gitbook/assets/Screen Shot 2021-09-27 at 3.49.15 PM.png>)

{% hint style="info" %}
Copy the code below to add this template to your account
{% endhint %}

```
{
  "name": "Vaccination Clinic Status",
  "defaultColor": null,
  "nameLabel": "Vaccination Centre",
  "uniq_name": "vaccination_clinic_status_board",
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
            "location",
            "total_doses_administered",
            "total_first_dose",
            "total_second_dose"
          ]
        },
        {
          "type": "row",
          "items": [
            "daily_numbers"
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
            "last_updated",
            "first_dose_booked",
            "second_dose_booked"
          ]
        }
      ],
      "name": "Appointments Booked"
    }
  ],
  "fields": {
    "location": {
      "label": "Location",
      "type": "location"
    },
    "total_doses_administered": {
      "label": "Total Doses Administered",
      "type": "text"
    },
    "total_first_dose": {
      "label": "Total First Dose Administered",
      "type": "text"
    },
    "total_second_dose": {
      "label": "Total Second Dose Administered",
      "type": "text"
    },
    "daily_numbers": {
      "label": "Daily Numbers",
      "type": "table",
      "fields": {
        "cLRX_sRu": {
          "label": "Date",
          "type": "date"
        },
        "gYRttfda": {
          "label": "First Doses",
          "type": "text"
        },
        "za2aMfWQ": {
          "label": "Second Doses",
          "type": "text"
        },
        "mEMKliv1": {
          "label": "Total Doses",
          "type": "text"
        },
        "jRB59HmK": {
          "label": "Comments",
          "type": "textarea"
        }
      },
      "layout": {
        "columns": [
          "cLRX_sRu",
          "gYRttfda",
          "za2aMfWQ",
          "mEMKliv1",
          "jRB59HmK"
        ]
      }
    },
    "last_updated": {
      "label": "Last Updated",
      "type": "datetime"
    },
    "first_dose_booked": {
      "label": "First Dose Booked",
      "type": "text"
    },
    "second_dose_booked": {
      "label": "Second Dose Booked",
      "type": "text"
    }
  },
  "listLayout": {
    "row": [
      "location",
      "total_doses_administered",
      "total_first_dose",
      "total_second_dose"
    ]
  },
  "headerProperties": [
    "Total Vaccinations Distributed: {{items | map:'data.total_doses_administered' | add}}",
    "Total First Dose Administered: {{items | map:'data.total_first_dose' | add}}",
    "Total Second Dose Administered: {{items | map:'data.total_second_dose' | add}}"
  ],
  "dashboardStats": [
    {
      "label": "Total Vaccinations Distributed",
      "value": "{{items | map:'data.total_doses_administered' | add}}",
      "successStatus": "",
      "warningStatus": ""
    },
    {
      "label": "Total First Dose Administered:",
      "value": "{{items | map:'data.total_first_dose' | add}}"
    },
    {
      "label": "Total Second Dose Administered:",
      "value": "{{items | map:'data.total_second_dose' | add}}"
    }
  ],
  "defaultSortingProperty": "created_date",
  "defaultSortingOrder": "asc",
  "defaultShowOwnItemsOnly": false,
  "defaultShowArchived": false
}
```

