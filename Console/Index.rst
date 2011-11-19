TYPO3 Console Interface v0.1.0
==============================

:Rendered: 2011-11-15T14:55:13+01:00

Overview
--------
**SYNTAX**
::

	console.php [options] [command] [parameters]


**OPTIONS**

+----+-----------------+-------------------------------------+
| -v | console:version | Displays version information        |
+----+-----------------+-------------------------------------+
| -i | console:info    | Displays some developer information |
+----+-----------------+-------------------------------------+
| -h | help            | Displays help for a command         |
+----+-----------------+-------------------------------------+

**COMMANDS**

+-------------------------+-----------------------------------------------------------------------+
| `cache:clear`_          | Clears all caches of a site                                           |
+-------------------------+-----------------------------------------------------------------------+
| `configuration:get`_    | Gets a configuration property                                         |
+-------------------------+-----------------------------------------------------------------------+
| `configuration:set`_    | Sets a configuration property                                         |
+-------------------------+-----------------------------------------------------------------------+
| `configuration:equals`_ | Determines whether a property equals the provided value               |
+-------------------------+-----------------------------------------------------------------------+
| `extension`_            | Provides some basic information on the site's extension status        |
+-------------------------+-----------------------------------------------------------------------+
| `extension:info`_       | Fetches the latest (or provided) version of an extension from TER     |
+-------------------------+-----------------------------------------------------------------------+
| `extension:list`_       | Lists all available extensions of a site                              |
+-------------------------+-----------------------------------------------------------------------+
| `extension:search`_     | Searches for an extension in the TER                                  |
+-------------------------+-----------------------------------------------------------------------+
| `extension:fetch`_      | Fetches the latest (or provided) version of an extension from TER     |
+-------------------------+-----------------------------------------------------------------------+
| `extension:install`_    | Installs the latest (or provided) version of an extension             |
+-------------------------+-----------------------------------------------------------------------+
| `extension:uninstall`_  | Uninstalls an extension                                               |
+-------------------------+-----------------------------------------------------------------------+
| `extension:refresh`_    | Refreshes the local cache of all extensions available in TER          |
+-------------------------+-----------------------------------------------------------------------+
| `help`_                 | Displays help for a command                                           |
+-------------------------+-----------------------------------------------------------------------+
| `recipe:execute`_       | Executes the provided recipe file                                     |
+-------------------------+-----------------------------------------------------------------------+
| `shell`_                | Runs the interactive shell                                            |
+-------------------------+-----------------------------------------------------------------------+
| `site:info`_            | Provides some basic site status                                       |
+-------------------------+-----------------------------------------------------------------------+
| `site:install`_         | Installs a fresh TYPO3 site                                           |
+-------------------------+-----------------------------------------------------------------------+
| `site:upgrade`_         | Upgrades a TYPO3 site to the most recent release                      |
+-------------------------+-----------------------------------------------------------------------+
| `site:upgradeDatabase`_ | Executes the database compare task and executes the required changes. |
+-------------------------+-----------------------------------------------------------------------+
| `site:upgradeWizard`_   | Executes the upgrade wizards.                                         |
+-------------------------+-----------------------------------------------------------------------+
| `user:list`_            | Provides a basic list of available backend users                      |
+-------------------------+-----------------------------------------------------------------------+


.. _`cache:clear`

cache:clear
-----------
`Clears all caches of a site`

**SYNTAX**
::

	console.php cache:clear [parameters]


**COMMAND:**
*cache:clear*

**PARAMETERS:**

+-------------+-------------------------------------+
| --directory | Defines directory of TYPO3 instance |
+-------------+-------------------------------------+


.. _`configuration:get`

configuration:get
-----------------
`Gets a configuration property`

**SYNTAX**
::

	console.php configuration:get [parameters]


**COMMAND:**
*configuration:get*

**PARAMETERS:**

+-------------+-------------------------------------------------------+
| --directory | Defines directory of TYPO3 instance                   |
+-------------+-------------------------------------------------------+
| --path      | Configuration path, e.g. TYPO3_CONF_VARS/SYS/sitename |
+-------------+-------------------------------------------------------+


.. _`configuration:set`

configuration:set
-----------------
`Sets a configuration property`

**SYNTAX**
::

	console.php configuration:set [parameters]


**COMMAND:**
*configuration:set*

**PARAMETERS:**

+-------------+-------------------------------------------------------+
| --directory | Defines directory of TYPO3 instance                   |
+-------------+-------------------------------------------------------+
| --path      | Configuration path, e.g. TYPO3_CONF_VARS/SYS/sitename |
+-------------+-------------------------------------------------------+
| --value     | Value to be set                                       |
+-------------+-------------------------------------------------------+


.. _`configuration:equals`

configuration:equals
--------------------
`Determines whether a property equals the provided value`

**SYNTAX**
::

	console.php configuration:equals [parameters]


**COMMAND:**
*configuration:equals*

**PARAMETERS:**

+-------------+-------------------------------------------------------+
| --directory | Defines directory of TYPO3 instance                   |
+-------------+-------------------------------------------------------+
| --path      | Configuration path, e.g. TYPO3_CONF_VARS/SYS/sitename |
+-------------+-------------------------------------------------------+
| --value     | Value to be compared                                  |
+-------------+-------------------------------------------------------+
| --strict    | (optional) Whether to be strict on type comparison    |
+-------------+-------------------------------------------------------+


.. _`extension`

extension
---------
`Provides some basic information on the site's extension status`

**SYNTAX**
::

	console.php extension [parameters]


**COMMAND:**
*extension*

**PARAMETERS:**

+-------------+-------------------------------------+
| --directory | Defines directory of TYPO3 instance |
+-------------+-------------------------------------+


.. _`extension:info`

extension:info
--------------
`Fetches the latest (or provided) version of an extension from TER`

**SYNTAX**
::

	console.php extension:info [parameters]


**COMMAND:**
*extension:info*

**PARAMETERS:**

+-------------+-------------------------------------+
| --directory | Defines directory of TYPO3 instance |
+-------------+-------------------------------------+
| --name      | Extension key                       |
+-------------+-------------------------------------+


.. _`extension:list`

extension:list
--------------
`Lists all available extensions of a site`

**SYNTAX**
::

	console.php extension:list [parameters]


**COMMAND:**
*extension:list*

**PARAMETERS:**

+-------------+-------------------------------------+
| --directory | Defines directory of TYPO3 instance |
+-------------+-------------------------------------+


.. _`extension:search`

extension:search
----------------
`Searches for an extension in the TER`

**SYNTAX**
::

	console.php extension:search [parameters]


**COMMAND:**
*extension:search*

**PARAMETERS:**

+--------+--------------------------------------------------+
| --name | Extension key, can be regular expression as well |
+--------+--------------------------------------------------+


**DESCRIPTION:**
Performs a local search in the TYPO3 Extension Repository.
The extension key can be given as string, like *extension*,
or as regular expression, like */^extension/*.

.. _`extension:fetch`

extension:fetch
---------------
`Fetches the latest (or provided) version of an extension from TER`

**SYNTAX**
::

	console.php extension:fetch [parameters]


**COMMAND:**
*extension:fetch*

**PARAMETERS:**

+-------------+-------------------------------------+
| --directory | Defines directory of TYPO3 instance |
+-------------+-------------------------------------+
| --name      | Extension key                       |
+-------------+-------------------------------------+
| --version   | (optional) Specific version         |
+-------------+-------------------------------------+
| --force     | (optional) Force execution          |
+-------------+-------------------------------------+


.. _`extension:install`

extension:install
-----------------
`Installs the latest (or provided) version of an extension`

**SYNTAX**
::

	console.php extension:install [parameters]


**COMMAND:**
*extension:install*

**PARAMETERS:**

+-------------+-------------------------------------+
| --directory | Defines directory of TYPO3 instance |
+-------------+-------------------------------------+
| --name      | Extension key                       |
+-------------+-------------------------------------+
| --version   | (optional) Specific version         |
+-------------+-------------------------------------+
| --force     | (optional) Force execution          |
+-------------+-------------------------------------+


.. _`extension:uninstall`

extension:uninstall
-------------------
`Uninstalls an extension`

**SYNTAX**
::

	console.php extension:uninstall [parameters]


**COMMAND:**
*extension:uninstall*

**PARAMETERS:**

+-------------+-------------------------------------+
| --directory | Defines directory of TYPO3 instance |
+-------------+-------------------------------------+
| --name      | Extension key                       |
+-------------+-------------------------------------+


.. _`extension:refresh`

extension:refresh
-----------------
`Refreshes the local cache of all extensions available in TER`

**SYNTAX**
::

	console.php extension:refresh [parameters]


**COMMAND:**
*extension:refresh*

.. _`help`

help
----
`Displays help for a command`

**SYNTAX**
::

	console.php help [parameters]


**COMMAND:**
*help*

**PARAMETERS:**

+--------------+------------------------------------------------+
| --identifier | (optional) Name of the command to get help for |
+--------------+------------------------------------------------+


.. _`recipe:execute`

recipe:execute
--------------
`Executes the provided recipe file`

**SYNTAX**
::

	console.php recipe:execute [parameters]


**COMMAND:**
*recipe:execute*

**PARAMETERS:**

+--------+----------------------------+
| --file | Recipe file to be executed |
+--------+----------------------------+


**DESCRIPTION:**
Allows to execute multiple commands with different arguments
at one time. The collection of it all is called *recipe*
in the context of the TYPO3 Console.
Example recipe file content (JSON):
::

	"type": "recipe",
	"name": "ble.install.new",
	"description": "Custom - Install new BLE websites",
	"commands": [
		{
			"command": "site:install",
			"parameters": {
				"directory": "/var/www/vhosts/mydomain.com/",
				"username": "development",
				"password": "development",
				"hostname": "127.0.0.1",
				"database": "t3_mydomain_com"
			}
		}
	]


.. _`shell`

shell
-----
`Runs the interactive shell`

**SYNTAX**
::

	console.php shell [parameters]


**COMMAND:**
*shell*

**PARAMETERS:**

+-------------+-------------------------------------+
| --directory | Defines directory of TYPO3 instance |
+-------------+-------------------------------------+


**DESCRIPTION:**
The shell command runs the TYPO3 Console's interactive shell. This shell allows for entering commands like through the regular
command line interface but additionally supports autocompletion and a user-based command history.

.. _`site:info`

site:info
---------
`Provides some basic site status`

**SYNTAX**
::

	console.php site:info [parameters]


**COMMAND:**
*site:info*

**PARAMETERS:**

+-------------+-------------------------------------+
| --directory | Defines directory of TYPO3 instance |
+-------------+-------------------------------------+


.. _`site:install`

site:install
------------
`Installs a fresh TYPO3 site`

**SYNTAX**
::

	console.php site:install [parameters]


**COMMAND:**
*site:install*

**PARAMETERS:**

+-------------+-------------------------------------+
| --directory | Defines directory of TYPO3 instance |
+-------------+-------------------------------------+
| --username  | (optional) Database username        |
+-------------+-------------------------------------+
| --password  | (optional) Database password        |
+-------------+-------------------------------------+
| --hostname  | (optional) Database hostname        |
+-------------+-------------------------------------+
| --database  | (optional) Database name            |
+-------------+-------------------------------------+


**DESCRIPTION:**
Installs TYPO3, in a similar process to the browser-based 1-2-3 Install Tool.

.. _`site:upgrade`

site:upgrade
------------
`Upgrades a TYPO3 site to the most recent release`

**SYNTAX**
::

	console.php site:upgrade [parameters]


**COMMAND:**
*site:upgrade*

**PARAMETERS:**

+-------------+-------------------------------------+
| --directory | Defines directory of TYPO3 instance |
+-------------+-------------------------------------+


.. _`site:upgradeDatabase`

site:upgradeDatabase
--------------------
`Executes the database compare task and executes the required changes.`

**SYNTAX**
::

	console.php site:upgradeDatabase [parameters]


**COMMAND:**
*site:upgradeDatabase*

**PARAMETERS:**

+-------------+-------------------------------------+
| --directory | Defines directory of TYPO3 instance |
+-------------+-------------------------------------+


.. _`site:upgradeWizard`

site:upgradeWizard
------------------
`Executes the upgrade wizards.`

**SYNTAX**
::

	console.php site:upgradeWizard [parameters]


**COMMAND:**
*site:upgradeWizard*

**PARAMETERS:**

+---------------+----------------------------------------------------------------------+
| --directory   | Defines directory of TYPO3 instance                                  |
+---------------+----------------------------------------------------------------------+
| --identifier  | (optional) Identifier of the upgrade wizard task                     |
+---------------+----------------------------------------------------------------------+
| --list        | (optional) Show list of available and suggested upgrade wizard tasks |
+---------------+----------------------------------------------------------------------+
| --execute-all | (optional) Execute all available upgrade wizard tasks                |
+---------------+----------------------------------------------------------------------+


**DESCRIPTION:**
At least one out of --identifier, --list or --executeAll must be given.

.. _`user:list`

user:list
---------
`Provides a basic list of available backend users`

**SYNTAX**
::

	console.php user:list [parameters]


**COMMAND:**
*user:list*

**PARAMETERS:**

+-------------+-------------------------------------+
| --directory | Defines directory of TYPO3 instance |
+-------------+-------------------------------------+

Indices and tables
------------------

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
