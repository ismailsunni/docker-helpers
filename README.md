## docker-helpers

Tim Sutton, 2014

Helper commands for docker because typing long docker commands is boring...


## Setup

```
cd ~
mkdir bin
cd bin
git clone git@github.com:timlinux/docker-helpers.git
```

Now add this somewhere to your ``~/.bashrc``:

```
export PATH=$PATH:$HOME/bin/docker-helpers
```

**Warning**: Some of these commands may be destructive - use at your own risk
and test on a test system before using in a production environment.

## Command quick reference

* **dcall** - Commit all named containers. Provide a prefix for the image name.
  The committed image will be in the form ``<prefix>/<container name>``.
* **deall** - Export all named containers. Exported containers will be named
  in the form ``docker-export-<container name>``.
* **dipall** - List the name and IP address of all named containers. Output 
  will be in the form ``<container name> : IP Address``. 
* **dli** - List all images. Shorthand for ``docker images``.
* **dnames** - List all the names of named containers.
* **dpasswords** - Print the names and passwords from all named containers.
  When you set up your container, print any passwords to stdout so they show up
  in the docker logs command. Be sure to print the word ``password`` in your
  stdout message as this is a simple grep operation.
* **dps** - List all running containers. Short hand for docker ps -a.
* **drmc** - Remove all stopped containers.
* **drmi** - Remove all images that have no tags.

