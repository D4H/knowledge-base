# Permission Profiles

#### WEB APP

You can configure the different permission profiles and access levels for each user.\
\
Go to the [Admin Area](../)

* Open **Settings** > **Permission Profiles**
* Click **+New**
* Fill in the details and grant or deny access to the organization-level permissions and module-level policies
* Click **Save** at the bottom of the screen
* Now when you go to [Personnel](../../personnel/) in [Collections](../collections/), your new permission profile will appear in the Permission Profiles drop down which you can assign to a member

## Permission Profile Name (Required)

This is the name of the permission profile that will appear in the Permission Profiles drop down menu when creating an Incident Management account for a member

## Permission Profile description (Optional)

Give a brief description as to what level of access the member will have if assigned this permission profile

## Organization-level Permissions

You can either **Allow** or **Deny** to any of the following organization-level permissions

| <p><strong>Permission</strong><br></p>   |                                                                                                                                                                                                                                          |
| ---------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Manage Organization Settings<br></p>  | <p>Allows a user to manage the settings of an organization<br></p>                                                                                                                                                                       |
| <p>Manage collections<br></p>            | <p>Allows a user to manage the collections of the organization. Please note that this also requires that the collections editing feature is included in your product edition. Please contact sales if not. <br></p>                      |
| <p>Manage templates<br></p>              | <p>Allows a user to edit the templates of forms and status boards for the organization. Please note that this also requires that the template editing feature is included in your product edition. Please contact sales if not. <br></p> |
| <p>Manage plays<br></p>                  | <p>Allows a user to manage the plays of the organization. Please note that this also requires that this feature is included in your product edition. Please contact sales it not. <br></p>                                               |
| <p>Manage users <br></p>                 | <p>Allows a user to manage the users of the organization, including deleting and inviting new users. Please note that this also requires that this feature is included in your product edition. Please contact sales it not. <br></p>    |
| <p>Read any incident<br></p>             | <p>Allows the user to view any incident within the organization. <br></p>                                                                                                                                                                |
| <p>Write to any incident<br></p>         | <p>Allows the user to save, delete, archive the contents of any incident within the organization.<br></p>                                                                                                                                |
| <p>Read collections<br></p>              | <p>Allows a user to read the collections of the organization and import items from collections. <br></p>                                                                                                                                 |
| <p>Manage any incident<br></p>           | <p>Allows the user to manage (export, shutdown, invite users, full read/write access), any incident within the organization. This permission level overrides any module-level permission. <br></p>                                       |
| <p>Read an incident if invited<br></p>   | <p>Allows the user to read an incident only if they are invited to join that incident. <br></p>                                                                                                                                          |
| <p>Write an incident if invited<br></p>  | <p>Allows the user to write the contents of an incident only if they are invited to join that incident. <br></p>                                                                                                                         |
| <p>Manage an incident if invited<br></p> | <p>Allows the user to start new incidents as well as manage (export, shutdown, invite users, full read/write access) any incident they are invited to. This permission level overrides any module-level permissions. <br></p>            |

## Module-level Policies

{% hint style="warning" %}
Note: _Module level permissions do not apply to users who have a "Manage any incident" or "Manage an incident if invited" permissions._
{% endhint %}

You can either **Allow** or **Deny** the following access levels to any of the modules:

* Read
* Write
* Delete / Archive

|                                       | <p><strong>Module</strong><br></p>                                  |
| ------------------------------------- | ------------------------------------------------------------------- |
| <p> <strong>Defaults</strong><br></p> | <p>Default Policy<br></p>                                           |
| <p> <strong>Built-in</strong><br></p> | <p>Log<br></p>                                                      |
|                                       | <p>Situation<br></p>                                                |
|                                       | <p>Map<br></p>                                                      |
|                                       | <p>Personnel &#x26; Roles<br></p>                                   |
|                                       | <p>D4H Products Integration<br></p>                                 |
|                                       | <p>Weather<br></p>                                                  |
|                                       | <p>Forms<br></p>                                                    |
|                                       | <p>Library<br></p>                                                  |
|                                       | <p> Mass Notifications<br></p>                                      |
| <p><strong>Custom</strong> <br></p>   | <p>This will include all your Status Boards and Task Boards<br></p> |
