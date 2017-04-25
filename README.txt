The migrate_remote_destination.settings config object needs to contain these:

migrate_remote_civicrm:
  source:
    constants:
      url: http://localhost/civicrm/sites/all/modules/civicrm/extern/rest.php?entity=contact&action=create
      api_key: example
      key: d1bfd4c475b128bc7191b8cef1abecb9

Change the url to your path but leave the part including and after extern the same, it is necessary to make it work.
Regarding api_key and key see https://wiki.civicrm.org/confluence/display/CRMDOC/REST+interface#RESTinterface-SettinguptousetheRESTAPI

Instead of saving it in the config file, the global $config overrides work as well.
https://www.drupal.org/docs/8/api/configuration-api/configuration-override-system
