---
layout: default
---
# Install the ownCloud Server
* * *
On a Linux distribution, you can use a package manager to install the server.

__Note__: Before installing ownCloud, you should install your own HTTP Server, database, and PHP. This prevents dependency conflicts with the ownCloud package. Then update the package manager.

Supported databases include SQLite, MYSQL/MariaDB, PostgreSQL, and Oracle 11g (Enterprise edition only).

## Update the Package Manager

- In a browser, go to [http://download.owncloud.org/download/repositories/10.0/owncloud/](http://download.owncloud.org/download/repositories/10.0/owncloud/).
- Select your Linux distribution.
- Follow the instructions to add the repository and install it manually.

Next, run the Installation Wizard.

## Run the Installation Wizard

Run the Installation Wizard to complete the installation.

  1. In a browser, go to [http://localhost/owncloud](http://localhost/owncloud).
  2. Enter your desired administrator’s username and password.
  3. Click __Storage and Database__ to set your data directory location and database connection.
      - Important! Your ownCloud data directory must already exist, be owned by your HTTP user, and be exclusive to ownCloud (not be modified manually by any other process or user).
  4. Click __Finish Setup__.

You can find your HTTP user in your HTTP server configuration files. For more information about your HTTP user, see [Post-Installation Steps](https://doc.owncloud.org/server/latest/admin_manual/installation/installation_wizard.html#post-installation-steps) on the ownCloud  [Installation Wizard](https://doc.owncloud.org/server/latest/admin_manual/installation/installation_wizard.html#post-installation-steps) page.

# Configure the ownCloud Server
* * *
During setup in the Installation Wizard, click __Storage and Database__ to set your data directory and database connection.

There are many additional server configuration options you can choose. See [Server Configuration](https://doc.owncloud.org/server/latest/admin_manual/configuration/server/) for more information.

## Configure User Access

On your server's Admin page, specify the host server name or the IP address.
  - To specify a port, use hostname:####.
  - To specify a Unix socket, use localhost:/path/to/socket.

This information is stored in the 'dbhost' parameter in the  config/config.php file.

    'dbhost' => '',

Learn more about config.php parameters at [Core Config.php Parameters](https://doc.owncloud.org/server/latest/admin_manual/configuration/server/config_sample_php_parameters.html).

## Create a User Account

Create a new user on the User management page of your ownCloud Web UI.

   1. Enter the username and initial password for the new user.
   2. Optionally, assign groups.
   3. Click __Create__.

# Connect to your ownCloud
* * *
You can connect to your ownCloud with a web browser, a desktop client, or a mobile client. Download clients at [https://owncloud.org/download/](https://owncloud.org/download/).

## Connect with a Browser

Connect to the server with a browser using the server's IP address or host server name. Specify a port if required by the administrator. Then enter your username and password.

## Connect with a Desktop Client

The ownCloud Desktop Client remains in the background and is visible as an icon in the system tray (Windows, KDE), menu bar (macOS), or notification area (Linux). Right-click on the icon to open a context menu and access your accounts.

## Connect with a Mobile Client

Install the ownCloud app on a mobile device and open it. Enter your ownCloud server URL, username, and password.

* * *
_All source information is from the [ownCloud 10.0.10 Server Administration Manual](https://doc.owncloud.org/server/latest/admin_manual/contents.html)_
