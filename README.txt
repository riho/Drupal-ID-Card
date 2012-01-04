ID-Card module for Drupal
Drupal module that adds the option to log in using the Estonian ID-Card service 

Developed by Mekaia

Requires ID card support for Apache (or IIS) on the server.
Instructions for installation can be found at http://www.id.ee/?id=10737

Also needs ID card authentication enabled on "id_card_login" url.
Example of Apache configuration:
	<LocationMatch "/(\w\w/)?id_card_login">
		SSLOptions +StdEnvVars +ExportCertData
		SSLRequireSSL
		SSLVerifyClient require
		SSLVerifyDepth 2
	</LocationMatch>

If your Drupal installation is in a subdirectory, replace the location with the following:
	<LocationMatch "/SUBDIRECTORY/(\w\w/)?id_card_login">

TODO list:
   1. Configuration option to set the default role/group for new users created with the module
   2. Help hook for the module
   3. Create field_firstname, field_lastname fields for user
   4. Estonian localization
   5. Better README file