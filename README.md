Remote PHPUnit commands
=======================

Originally forked from https://github.com/m0nah/SimplePHPUnit-for-Sublime-Text


This plugin allows you the run the PHPUnit on a remote server tests using the Sublime Text interface, without having to open and use the command line.

### Available commands:

- `Remote PHPUnit: Run all`
- `Remote PHPUnit: Run unit tests`
- `Remote PHPUnit: Run functional tests`
- `Remote PHPUnit: Run tests in current file`

### Coloring output

![Coloring output](https://raw.github.com/m0nah/SimplePHPUnit-for-Sublime-Text/master/Screen%20Shot.png)

### Installation:
Use Package Controller or create a the directory `RemotePHPUnit` in your Sublime Text Packages directory, and you're ready to go.

### Configuration:

The server_address configuration is mandatory.

An example for a Symfony2 Vagrant setup looks as follows:

```
{
	"phpunit_path": "/usr/bin/phpunit",
    "phpunit_xml_path": "app/",
    "root_folder": "/vagrant",
    "server_user": "vagrant",
    "server_address": "172.84.98.23",
    "ssh_key": "app/vagrant_key"
}
```
* The shared folder on vagrant is /vagrant
* An SSH Key was generated (```ssh-keygen -t rsa -b 2048```) and placed under /vagrant/app/vagrant_key
  so that the files are /vagrant/app/vagrant_key and /vagrant/app/vagrant_key.pub. Also the vagrant_key.pub
  was added to the autohorized_keys (```cat /vagrant/app/vagrant_key.pub >> ~/.ssh/authorized_keys```)
* The server_address is the IP of the Vagrant instance
* The phpunit_xml_path is the relative path to the PHPUnit config file (phpunit.xml or phpunit.xml.dist)


### Usage:
Press Cmd + Shift + P for the dropdown command list, search for `Remote PHPUnit: `, and pick your command. Also you can use `Tools/Remote PHPUnit` menu item

### Notes:
- PHPUnit config file needs to been in the root folder of your structure in the sidebar.
- You need insert in Sublime Text user settings `"show_panel_on_build": true` or use `Tools/Build Results/Show Build Results` menu item for view results.

Give some feedback.

Thanks.
