## Reset admin password
    $ sudo passwd root

## Ways to purge apps
    * sudo dpkg --configure -a
    * sudo apt-get install -f
    * sudo apt-get remove --purge package_name
    * sudo apt autoremove
    * sudo ls -l /var/lib/dpkg/info | grep -i package_name *then* sudo mv /var/lib/dpkg/info/package_name.* /tmp *then* sudo apt-get update
    * sudo dpkg -i --force-overwrite /var/cache/apt/archives/full_name_of_package

## Udate chmod
    cd $HOME
    { sudo chflags -R nouchg,nouappnd ~ $TMPDIR.. ; \
      sudo chown -R $UID:staff ~ $_ ; \
      sudo chmod -R -N ~ $_ ; \
      sudo chmod -R 755 ~ $_ ; \
      sudo chmod 700 Desktop Documents Downloads Dropbox Library Movies Music Pictures Sites $_ ; \
      sudo chmod 777 Public ; \
      sudo chmod 733 Public/Drop\ Box ; \
      } 2> /dev/null

## Find App By Name
    mdfind -name [application name]
