Dockers file list
=================

glances_install: Ubuntu + Glances stable version (from Pypi)

glances_develop_install: Ubuntu + Glances develop branch version (from Github)

shinken_install: Ubuntu + Shinken (latest version from the official site)

Create the image
================

    sudo docker.io build -t nicolargo:glances_develop - < glances_develop_install

Use the image (exemples)
========================

Glances standaalone client

    sudo docker.io run -i -t --entrypoint /bin/bash nicolargo:glances_develop -c "cd glances ; git pull origin develop ; python -m glances"

Run a Shnken server (Web interface @IP:7767 with admin/admin as default password)

	sudo docker.io run -d -P nicolargo:shinken
