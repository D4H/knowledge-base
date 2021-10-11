# Medical Resource Requests

{% hint style="info" %}
This article is part of [sample templates](../) for Incident Management
{% endhint %}

Use the Medical Resource Requests status board to coordinate resource distribution among your health care provider agencies. Log requests for equipment and determine when they will be delivered. View a running total of your expenditures and track how many requests are approved versus denied. Record any additional notes about the requests on the forms located behind the status board rows. 

To upload this template into your account, follow the steps on our [Importing Sample Templates](../importing-sample-templates.md) page.

![](<../../../.gitbook/assets/Screen Shot 2021-09-27 at 4.01.26 PM.png>)

![](<../../../.gitbook/assets/Screen Shot 2021-09-27 at 4.00.49 PM.png>)

{% hint style="info" %}
Copy the code below to add this template to your account
{% endhint %}

```
{
  "name": "Medical Resource Requests",
  "defaultColor": null,
  "nameLabel": "Name",
  "uniq_name": "requests",
  "icon": "fa fa-inbox",
  "quickAdd": true,
  "suggestFromCollections": false,
  "layout": [
    {
      "type": "section",
      "rows": [
        {
          "type": "row",
          "items": [
            "status"
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
            "priority"
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
            "order"
          ]
        },
        {
          "type": "row",
          "items": [
            "requested_delivery_location",
            "suitable_substitutes"
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
            "requested_by",
            "requested_at"
          ]
        },
        {
          "type": "row",
          "items": [
            "delivered_by",
            "estimated_delivery"
          ]
        },
        {
          "type": "row",
          "items": [
            "cost"
          ]
        },
        {
          "type": "row",
          "items": [
            "comments"
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
            "location"
          ]
        }
      ]
    }
  ],
  "fields": {
    "requested_by": {
      "label": "Requested by",
      "type": "text"
    },
    "requested_at": {
      "label": "Requested at",
      "type": "datetime"
    },
    "delivered_by": {
      "label": "Assigned To",
      "type": "relationship",
      "thisType": "info_item~requests",
      "relName": "requests2roles",
      "otherType": "personnel_role"
    },
    "estimated_delivery": {
      "label": "Estimated delivery",
      "type": "datetime"
    },
    "location": {
      "label": "Location",
      "type": "location"
    },
    "order": {
      "label": "Order",
      "type": "table",
      "fields": {
        "qty": {
          "label": "Qty",
          "type": "text"
        },
        "kind": {
          "label": "Kind",
          "type": "text"
        },
        "type": {
          "label": "Type",
          "type": "text"
        },
        "detailed_description": {
          "label": "Detailed Description",
          "type": "text"
        },
        "arrival_requested": {
          "label": "Arrival Requested",
          "type": "text"
        },
        "estimated": {
          "label": "Estimated",
          "type": "text"
        },
        "cost": {
          "label": "Cost",
          "type": "text"
        }
      },
      "layout": {
        "columns": [
          "qty",
          "kind",
          "type",
          "detailed_description",
          "arrival_requested",
          "estimated",
          "cost"
        ]
      }
    },
    "requested_delivery_location": {
      "label": "REQUESTED DELIVERY LOCATION",
      "type": "text"
    },
    "suitable_substitutes": {
      "label": "SUITABLE SUBSTITUTES",
      "type": "text"
    },
    "cost": {
      "label": "Cost",
      "type": "number",
      "preSymbol": "$"
    },
    "status": {
      "label": "Status",
      "type": "select",
      "options": [
        {
          "label": "Requested",
          "value": "requested"
        },
        {
          "value": "approved",
          "label": "Approved"
        },
        {
          "value": "delivered",
          "label": "Delivered"
        },
        {
          "value": "denied",
          "label": "Denied"
        },
        {
          "label": "Purchase Order Placed",
          "value": "purchase_order_placed"
        },
        {
          "label": "Sourced Locally",
          "value": "sourced_locally"
        },
        {
          "label": "More Information Needed before processing",
          "value": "more_information_needed_before_processing"
        }
      ],
      "default": "requested"
    },
    "comments": {
      "label": "Comments",
      "type": "textarea"
    },
    "priority": {
      "label": "Agency Type",
      "type": "select",
      "options": [
        {
          "label": "First Responder Agency",
          "value": "first_responder_agency"
        },
        {
          "value": "hospital",
          "label": "Hospital"
        },
        {
          "value": "long_term_care",
          "label": "Long Term Care"
        },
        {
          "value": "medical_offices",
          "label": "Medical offices"
        },
        {
          "value": "volunteer_organization",
          "label": "Volunteer organization"
        },
        {
          "value": "home_health",
          "label": "Home Health"
        }
      ],
      "default": null
    }
  },
  "expressions": {
    "success": "status===\"delivered\"",
    "warning": "status===\"approved\"",
    "danger": "status===\"requested\""
  },
  "listLayout": {
    "row": [
      "requested_by",
      "priority",
      "requested_at",
      "estimated_delivery",
      "status",
      "comments"
    ]
  },
  "headerProperties": [
    "${{(items | map: 'data.cost' | add)}} Total",
    "{{(items | pick: 'data.status === \\'requested\\'').length }} Requested",
    "{{(items | pick: 'data.status === \\'approved\\'').length }} Approved",
    "{{(items | pick: 'data.status === \\'delivered\\'').length }} Delivered",
    "{{(items | pick: 'data.status === \\'denied\\'').length }} Denied",
    "{{(items | pick: 'data.status === \\'sourced_locally\\'').length }} Sourced Locally"
  ],
  "dashboardStats": [
    {
      "label": "Requested",
      "value": "{{(items | pick: 'data.status === \\'requested\\'').length }}"
    },
    {
      "label": "Delivered",
      "value": "{{(items | pick: 'data.status === \\'delivered\\'').length }}"
    },
    {
      "label": "Ordered",
      "value": "{{(items | pick: 'data.status === \\'purchase_order_placed\\'').length }}"
    },
    {
      "label": "Sourced Locally",
      "value": "{{(items | pick: 'data.status === \\'sourced_locally\\'').length }}"
    }
  ],
  "defaultSortingProperty": "created_date",
  "defaultSortingOrder": "asc",
  "defaultShowOwnItemsOnly": false,
  "defaultShowArchived": false
}
```

