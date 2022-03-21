# Mac Specific
Copy terminal output directly to clip board = pbcopy < ~/.ssh/id_rsa.pub


## Add user to group
sudo dseditgroup -o edit -a john -t user admin
sudo dseditgroup -o edit -a john -t user wheel

## Change Password
sudo dscl . -passwd /Users/username password
