# Set Colors with Date Function Expressions

Manage how your [status board ](../)warnings are displayed based on time passed or time left.  For example you may have a volunteer or employee that forgot check back into the incident via the [Incident Management ](broken-reference)account.  Another example is you have a piece of equipment that needs to be checked on every 10 hours, but no-one has had time to check it in the last day.&#x20;

For these types of status boards, we have functions to automatically turn the row into warning or danger mode, without any action from the user.

#### WEB APP

Item date function expressions allow you to specify what color a row within a status board should be based on what is entered into a date and time field.

### Expressions Available

* _isToday -_ is the date same date as todays date? Gives true / false
* _isTomorrow -_ is the date same date as tomorrow? Gives true/false
* _hoursSince -_ how many hours since this date/time happened (negative => date is in the future). Gives a number. **Needs to be compared against a limit number.**
* _daysSince -_ how many days since this date/time happened (same thing with negative). Gives a number. **Needs to be compared against a limit number.**

****

To do this go to the [Admin Area](../../admin-area/) and follow the steps below:

* Open up [Templates](../../admin-area/templates/) and click edit on the status board you wish to edit
* If you do not already have a [Date and Time field](../../admin-area/templates/form-builder-and-field-types/), you will need to add one in now.&#x20;
* Take note of the Field ID under the three dots menu <img src="../../../.gitbook/assets/Three Dots.png" alt="" data-size="line"> at the top right, in the example below it is **check\_in\_time**
* Scroll down and expand **Advanced Options**
* Enter in the applicable **Item Status Expressions** based on the desired colors including the time frame requirements

### Example A of using this Expression&#x20;

An organization may create [Status Boards](../) to help track the checks of generators on a 4 hour bases during an incident to ensure good operating order.

The organization's desire is to visualize the Success, Warning and Danger colors indicated when a generator is past its' check in requirement.  Additionally, this organization has also created a [Status Option Selection field](set-colors-with-item-status-expressions.md) to indicate if during the check the generator was found Operational or Not Operational.

{% hint style="info" %}
Success = Green

Warning = Amber

Danger = Red
{% endhint %}

**Success:**

```
status === 'op' && (data_checked | hoursSince) < 4
```

"If status is operational, _and_ it has been check in the last 4 hours, show green"

**Warning:**

```
status === 'op' && (data_checked | hoursSince) >= 4
```

"If status is operational, _and_ has _not_ been checked in the last 4 hours, show orange"

**Danger:**

```
status !== 'not_op' || (data_checked | hoursSince) >= 24
```

"Is status is not operational, _or_ it has not been checked in 24 hours, show red"

<figure><img src="../../../.gitbook/assets/Screen Shot 2022-10-14 at 2.58.01 PM.png" alt=""><figcaption><p>Based on the Last Checked since it's 14:58 and the Status field</p></figcaption></figure>
