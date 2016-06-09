# User Environments

### User Manager

```bash
# list all users
cat /etc/passwd

# add user
useradd user_name

# delete user
userdel [username]
userdel example

# change password
passwd user_name

# grant root privileges to the user
visudo
mynewuser ALL=(ALL) ALL
```

### Group Manager [^1]

```bash
# list all groups
cat /etc/group

# create a new group
groupadd [options] group
groupadd admins

# delete a group
groupdel <groupname>
groupdel example

# add user to group
usermod -a -G <groupname> username
usermod -a -G admins geek

# change a user’s primary Group
usermod -g <groupname> username
usermod -g admins geek

# list group of user
id <username>
id geek
```

Known Issues:

* [groupdel: cannot remove the primary group of user 'administrator'](http://askubuntu.com/questions/677344/groupdel-cannot-remove-the-primary-group-of-user-administrator)
* [How to enable automatic user logins in CentOS 7 and GNOME](http://wpguru.co.uk/2015/08/how-to-enable-automatic-user-logins-in-centos-7-and-gnome/)

[^1]: [Add a User to a Group (or Second Group) on Linux](http://www.howtogeek.com/50787/add-a-user-to-a-group-or-second-group-on-linux/)