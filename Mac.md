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
