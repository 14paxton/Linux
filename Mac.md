# Mac Specific
 Copy terminal output directly to clip board = pbcopy < ~/.ssh/id_rsa.pub


## Add user to group
 sudo dseditgroup -o edit -a john -t user admin
 sudo dseditgroup -o edit -a john -t user wheel
### add user to SUDO
  su AdminUser
  authentication, and then:
   
   Now, as Adminuser, use the visudo command to edit the sudoers file:

      Adminuser % sudo visudo
      Add the following line to the sudoers file:
      StandardJoeUser ALL = (ALL) ALL

## Change Password
 sudo dscl . -passwd /Users/username password


## How do I apply all recommended updates?
     All updates that are recommended for your system:
     sudo softwareupdate -r

## Updating Mac using the Terminal app
    To install all updates that are applicable to your system, enter:
    sudo softwareupdate -i -a

## Install all but make sure you ignore ‘JavaForOSX’ updates:
     sudo softwareupdate --ignore JavaForOSX

## To clear the list ignored updates, enter:
     sudo softwareupdate --reset-ignored
     
# Slow Java app     
     
First you need to find the hostname of your Mac. You do this from System Preferences. Click the Sharing icon in System Preferences.
javahosts_1.png


You will see a box that shows the Computer Name, under that will be the hostname ending in .local. That's what you will need, so take note of it. In my case it was Enzyme.local.
javahosts_2.png

The next step is to update your /etc/hosts file. This must be done as root, so at the Terminal, type in "sudo vi /etc/hosts". This will ask for your password...

Add the hostname you noted from earlier at the end of lines that start with "127.0.0.1" and "::1". If you don't know how to use vi, look here. You can also use nano instead, just replace "vi" in the command above with "nano".

In the end this is what my /etc/hosts file looked like:
127.0.0.1       TPLNK-BPAXTON3.local
255.255.255.255 broadcasthost
::1             TPLNK-BPAXTON3.local
     

