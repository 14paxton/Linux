## Reset admin password
    $ sudo passwd root

## Ways to purge apps
    * sudo dpkg --configure -a
    * sudo apt-get install -f
    * sudo apt-get remove --purge package_name
    * sudo apt autoremove
    * sudo ls -l /var/lib/dpkg/info | grep -i package_name *then* sudo mv /var/lib/dpkg/info/package_name.* /tmp *then* sudo apt-get update
    * sudo dpkg -i --force-overwrite /var/cache/apt/archives/full_name_of_package
