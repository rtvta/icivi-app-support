# iCivi App Support Documentation
The application is designed for non-profit organizations that use CiviCRM to manage their customers.
To access data from CiviCRM the application use the [REST interface](https://docs.civicrm.org/dev/en/latest/api/interfaces/#rest) of [CiviCRM API](https://docs.civicrm.org/dev/en/latest/api/).
CiviCRM administator can provide an api_key which is attached to the user that will be performing the action against the system and a site_key which is the key stored in civicrm.settings.php, base_url witch is also stored in civicrm.settings.php and API end point witch is the path to rest.php file. For Drupal installation usually:
```
/sites/all/modules/civicrm/extern/rest.php
```
There must also be a user account in the relevant content management system for the user associated with the API Key.

The application allow the user to retrieve from CiviCRM and save on device the following data: his **Contact** details (name, email etc.) and basic information about related **Contributions**, **Pledges**, **Events** and **Memberships**.

The REST interface is subject to [API Security](https://docs.civicrm.org/dev/en/latest/security/permissions/#api-permissions).
The application does not allow the user with 'View All Contacts' permission retrieve data from CiviCRM and the user will be receive the message: "You have permissions to view other contacts. Please refer to CiviCRM administator.".


## Requirements
* The CiviCRM website must be with HTTPS
* User permissions to view the contact details
    * Access CiviCRM
    * View My Contact
    * Access CiviCRM
* User permissions to view related data (**optional**). If user does not have one or more of these permissions, he can exclude the entity from request by disabling switch in the iCivi application Settings. 
    * Access CiviContribution
    * Access CiviPledge
    * Access CiviEvent
    * Access CiviMembership

## Usage
1. After installing iCivi will run on demo mode.
2. Go to Settings and enter the Base URL, API Key and Site Key. If is necessary change the API Path.
3. Choose the contact related informantion you whant to retrieve from CiviCRM: entities and the quantity of lastest records.
4. Disable demo mode.
5. Back to app and swipe down to retrieve data from CiviCRM.
6. If the record retrieved is new or has been changed it will be marked as unread.
7. The application allow to delete records of related entities from device and does not allow to delete the contact record. This action does not updates data on the server.
8. Each new request return limited count of records. Existing records will be updated, new records will be added.
9. To return to the demo mode, you need to activate the demo mode in the iCivi application Settings and swipe down to reload the demo contact.
10. There are only two contacts may be saved on the device simultaneously. The demo contact and the latest contact that has been successfully retrieved from CiviCRM. That means if, for example, API Key changed and new contact has been saved successfully the previous contact will be deleted from local database.


## App Store Description
iCivi is designed for non-profit organizations that use CiviCRM to manage their customers.

By providing a set of personal keys to users, the CiviCRM administrator allows them to access personal data as well as basic information about their Contributions, Pledges, Events and Memberships.

Key features:
* Access user data from CiviCRM for read only. 
* View latest response offline.
* It is available to determine which entities and the number of their last records to retrieve from CiviCRM.
* Simple and flexible for future extensions.

## Contact Us
For more details, complaints and suggestions, please contact me by email: 
roman.tiagni@icloud.com
