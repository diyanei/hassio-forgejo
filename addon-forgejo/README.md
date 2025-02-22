# Forgejo addon

Take back control of your software development process, self-host your projects and get everyone involved in delivering quality software on the same page. 

##  About

This addon is based on docker image made by https://forgejo.org/docs/next/admin/installation-docker/#docker
<!-- It provides admin user configuration, no need to launch docker commands to create admin.
I didn't expose all other settings, let's see if it is needed at some point. -->

Happy giting !

##  Installation

1. [Add my Forgejo add-on repository](https://github.com/diyanei/hassio-forgejo.git) to your Home Assistant instance.
1. Install this add-on.
1. If you want an already installed and running gitea server (up to version 1.22.x ONLY) to be moved over the forgejo one, you can do this the following way:
	1. Stop and Backup your gitea server
	1. Backup again your gitea server (on another disk for instance)
	1. Be sure to backup it, remember.
	1. on the Home Assistant host, go to /usr/share/hassio/addons/data and from there:
		* do a copy from the gitea addon subdir (db21ed7f_gitea) to the forgejo one, for instance with the following command `sudo rsync -avn db21ed7f_gitea/ #forgejo#/` (remove the `-n` option to actually do it, this is the dry-run version).
	1. Then go on

1. Start the add-on.
1. Check the logs of the add-on to see if everything went well.
1. Use the `Open Web interface` button to access the instance and complete the configuration
1. Enjoy
