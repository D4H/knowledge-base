# Set Colors with Item Status Expressions

#### WEB APP

Item status expressions allow you to specify what color a row within a [status board](https://support.d4h.org/d4h-incident-management/status-boards) should be based on what status is selected from a drop down field.

![](../../.gitbook/assets/set-color-with-item-status-expressions.png)

To do this go to the [Admin Area](../admin-area/) and follow the steps below:

* Open up [Templates](../admin-area/templates/) and click edit on the status board you wish to edit
* If you do not already have a **Status** [field](../admin-area/templates/form-builder-and-field-types/), you will need to add one in now. 
* In this example the options for statuses are '**No Damage**', '**Minor Damage**', '**Severe Damage**' and '**Destroyed**'

![](../../.gitbook/assets/set-colors-with-item-status-expressions-2.png)

* Scroll to the bottom of the page and click ➕ **Advanced Options**
* Here you will see **Item status expressions**

![](../../.gitbook/assets/item-status-expressions.png)

{% hint style="info" %}
Success = Green

Warning = Amber

Danger = Red
{% endhint %}

* To set the colors based on the status selection, you must use the field ID/name. I.e. the field name for **No Damage** is **no\_damage**, the field name for **Destroyed** is **destroyed** and so on
* Note, the field ID for the Status field in this example is **status** which you can find by clicking on the **More Options \[⋮\]** menu on the field in the template in the admin area

![](../../.gitbook/assets/field-id-for-status.png)

If '**No Damage**' is selected I want the status board item to be **green**, enter the following in Success:

```text
status==='no_damage'

```

If '**Minor Damage**' is selected, I want the item to be **amber**, enter the following in Warning:

```text
status==='minor_damage'
```

If '**Severe Damage**' OR '**Destroyed**' is selected, I want the item to be **red**, enter the following in Danger:

```text
status==='severe_damage' || status==='destroyed'
```

* this is what it should look like in your account

![](../../.gitbook/assets/item-status-expressions-in-your-account.png)

* Click **save**

