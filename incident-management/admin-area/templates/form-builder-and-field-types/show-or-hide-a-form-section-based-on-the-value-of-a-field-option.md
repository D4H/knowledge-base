# Show or hide a form section based on the value of a field option

It is possible to display a section on a form based on what you chose in an [option selection](./) or [checkbox field](./) by using conditional settings. This can be done on your [Situation](../../../situation/), [Personnel](../../../personnel/), [Roles](../../../roles/), [Status Board](../../../status-boards/), [Task Board](../../../task-boards/) and Form templates. \


## Conditional settings on an Option Selection field

* Go to the [Admin Area ](../../)and [Templates    ](../)      
* Open the Situation template
* Hover your mouse over the field you will use to trigger a section to appear ('Incident Type' in this example). Click on **More Options **\[⋮] and copy the Field ID:\


![](<../../../../.gitbook/assets/show or hide a form section.png>)

* Go to the section that you want to trigger to appear on your form if 'Storm' is selected as the incident type. 
* Hover your mouse over the Section title bar. Click on **More Options** \[⋮] and **Show based on a condition...**\


![](<../../../../.gitbook/assets/show based on a condition.png>)

* Type the following into the expression box:

```
thisDocument.data.incident_type === 'storm'
```

{% hint style="info" %}
You can paste in the Field ID you have copied from the field that will trigger the section to appear, in this case incident_type. 'storm' = different_option_id; is the selection that will trigger the section to appear. 

**Expression**: thisDocument.data.field_id === 'different_option_id' 

**Expression to use when more than one selection will trigger the section to appear**: thisDocument.data.field_id === 'different_option_id' || thisDocument.data.field_id === 'different_option_id' 

**|| = OR** 

**& = AND**\

{% endhint %}

![](<../../../../.gitbook/assets/show the section based on a condition.png>)

* Click **OK**
* Click **Save** at the bottom of the page
* Now if you choose 'storm' from the 'Incident Type' drop down field, the section will appear. 

## Conditional settings on a Checkbox field

* Go to the [Admin Area](../../) and[ Templates    ](../)      
* Open the Situation template
* Hover your mouse over the field you will use to trigger a section to appear ('City Impact' in this example). Click on **More Options** \[⋮] and copy the Field ID (city_impact):\


![](<../../../../.gitbook/assets/conditional settings on a checkbox field.png>)

* You will also need the field label of the option that is checked off in the field. We will use High Impact in this example:\


![](<../../../../.gitbook/assets/high impact.png>)

* Type the following into the expression box:

```
thisDocument.data.city_impact.high_impact === true
```

{% hint style="info" %}
Field_id will be the field label you copy from the checkbox field. different_option_id will be whatever option is checked in the checkbox field that will trigger the section to appear. 

**Expression**: thisDocument.data.field_id.different_option_id === true 

**Expression to use when more than one selection will trigger the section to appear**: thisDocument.data.field_id.different_option_id === true || thisDocument.data.field_id.different_option_id === true 

**|| = OR** 

**& = AND**
{% endhint %}
