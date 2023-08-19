# Checklist for Cyber-Taipan Competition

## Notes

When going through the README file on the image, think about all the tasks that could exist for each sentence.

Jot them down and at the end, assign a amount of time to each task, then group into hours so at each hour if you are stuck move onto the next hours' tasks.

Most things can be done from the Terminal (press the Windows key, and search for Terminal to open it), and you should be able to find a command to do what you need.

**If you don't understand a word or term, Google it. Also, if you are unsure how to do something Google `'ubuntu [version] [thing you want to do]'`.**

## Overview

1. Read readme file
2. Enter team ID
3. Open a root terminal
4. Do forensic questions
5. Check users
6. Check passwords
7. Check files
8. Do updates
9. Check software
10. Secure the network
11. 

## Read readme file

**MAKE SURE TO DO THIS FIRST**

Make notes of tasks for each sentence in the readme file.

Note down users, if they are administrators or standard users, and what their passwords are.

Note down any PORTS that need to be open/closed.

## Enter team ID

Enter your team ID in otherwise the VM might lockdown.

Coach should have the team ID emailed day of.

## Open a root terminal

[watch]()

Open Terminal by pressing CTRL+ALT+T on the keyboard, or by clicking the Ubuntu logo on the dock on the left, and searching for Terminal and click.

An icon will appear for it on dock that looks like a black console window, right click and select 'add to favourites' in case you close it, you just need to click this icon to open it again.

In the terminal, note the username (left of the @ symbol). You will need to look up the password for this user from the readme file.

Type `sudo su` and press Enter on the keyboard. You will be asked for the user's password. Type this in a press Enter on the keyboard.

This will make you the "root" user which will allow you to do anything to config the system. It saves you typing `sudo` in front of everything command

## Do forensic questions

## Check users

### Disable guest account

[watch]()

Go to /etc/lightdm/lightdm.conf and add the line

allow-guest=false

Then restart your session with sudo restart lightdm. This will log you out, so make sure you are not executing anything important.

### Secure root login through openssh

In the terminal type:

``

### Remove users not in readme file

### Add users that are needed to be there

In terminal (with root) type:

`adduser <user>`

`<user>` is the name of the user. Usernames are CASE-SENSITIVE!

Set password as per the readme, if no password specified, make sure it meets minimum requirements.

If the user needs administrator privileges, add them to the `sudo` group by typing:

`usermod -aG sudo <user>`

`<user>` is the name of the user. If they need to be part of another group replace `sudo` with group.


