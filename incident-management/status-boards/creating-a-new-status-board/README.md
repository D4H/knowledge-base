# Creating a new Status Board

#### WEB APP

To create a new [Status Board](../) template, navigate to the [Admin Area](../../admin-area/) in your D4H [Incident Management](../../getting-started.md) account.

* Open **Templates** > **Status Boards**
* Click on **New Status Board**
* Fill in the details and create your template using the [Form Builder](../../admin-area/templates/form-builder-and-field-types/)
* Click **Save** at the bottom of the screen

{% embed url="https://youtu.be/DxIiwJ1F8uQ" %}



## Selecting An Icon (Required)

Select an icon for the board. This icon will be used to represent the board in the menu and when [Tagged in the Log](../../updates/tagging-items-in-the-log.md). Press Show more to see more icons, and use keywords to search for the name of an icon.

![](<../../../.gitbook/assets/selecting an icon.png>)

## App Name (Required)

The app name will appear in the navigation menu and throughout the software. Choose a short name that ideally fits on a single line.

{% hint style="info" %}
Names should be unique and clear. Ideally it would be a plural describing the contents such as 'Damage Assessments' rather than 'Damage Assessment', 'Passengers' rather than 'Passenger'.
{% endhint %}

## Unique Name (Required)

The unique name is auto-generated. The unique name is used later to create relationships between modules and reference this module in custom expressions.

## Setting A Default Color (Optional)

Setting a default color for your board will change the default background color of each row from white to the color of your choice.

![](<../../../.gitbook/assets/setting a default color.png>)

## Name Field Label (Optional)

The name field is by default set to 'Name' but you could change it to anything you'd like such as 'Ref' or 'Incident Number' as examples. This is the title of each row and always displays first column in the [List Layout Columns](../../admin-area/templates/list-layout-columns.md). It's also how we reference the row in[ Relationship Fields ](../../admin-area/templates/form-builder-and-field-types/)and when you [Tag an Item in the Log](../../updates/tagging-items-in-the-log.md).

## Name Field Template (Optional)

The Name Field Template is an optional auto-generation template for the row name field. For example, you might want the name of each row to be automatically filled in with todays date. The following variables are available:\


| <p><strong>Variable</strong>  <br></p> | <p><strong>Output</strong><br></p>                |
| -------------------------------------- | ------------------------------------------------- |
| <p>{day}<br></p>                       | <p>Day of Month (DD) e.g. 23<br></p>              |
| <p>{month}<br></p>                     | <p>Month of Year (MM) e.g. 03<br></p>             |
| <p>{year}<br></p>                      | <p>Year (YYYY) e.g. 2020<br></p>                  |
| <p>{counter}<br></p>                   | <p>Incrementing Counter e.g. 1,2,3,4 etc.<br></p> |
| <p>{*}<br></p>                         | <p>Wildcard for Counter<br></p>                   |

So for example, if you wanted each row to be D1, D2, D3 etc. for Damage Assessment 1, 2, 3 etc. you could set it as:

```
D{counter}
```

If you wanted it to be the date then a free text ref you could use the template:

```
{year}{month}{day} - 
```

This would auto-fill in '0429-' if today was 29th April, and then the user can continue typing free-text e.g. '20200429 - Stuck In Mud'.\
\
If you want to use free-text with the counter, you need to use the wildcard so we can recognize the pattern to generate the next number. e.g. D1 - Stuck In Mud

```
D{counter} - {*}
```

## "Add" Behavior

Some status boards are suited to long-form entry, some are quick with just a few details. This allows you to choose which option you would like when adding a new item to a status board.&#x20;

![](<../../../.gitbook/assets/add behavior.png>)

****[**Quick Add** ](quick-add-vs-full-add-status-boards.md)- Will let you add a new row to the status board

****[**Standard**](quick-add-vs-full-add-status-boards.md) - Will open the form behind the row so you can fill in all the details
