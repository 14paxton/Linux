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

