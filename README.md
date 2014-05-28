Dockers file list
=================

glances_install: Ubuntu + Glances stable version (from Pypi)

glances_develop_install: Ubuntu + Glances develop branch version (from Github)

Create the image
================

    sudo docker.io build -t ubuntu:glances_develop - < glances_develop_install

Use the image
=============

    sudo docker.io run -i -t --entrypoint /bin/bash ubuntu:glances_develop -c "cd glances ; git pull origin develop ; python -m glances"

