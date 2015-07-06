# ansible-eclim
Files to load eclim for java dev on ubuntu servers

This is a work in progress.  The goal is to make an ansible playbook that will load a fresh ubuntu server (usually in a VBox, but wherever) with a copy of eclim, which allows vim to do pretty decent development on Java, including debugging.  It is a headless development environment.

## Current state of the art

In order to use this repo, you must:

1.  Clone it
2.  Edit the settings (they are in several different variable files) to point to your specific user name.  No passwords are in this right now, nor are any needed.
3.  run `build.sh` to pay the playbook.  (Ansible must obviously already be on the system.  Pretty much everything else will be loaded.)
5.  run `start_headless.sh` to run the headless X environment that eclipse needs.
6.  run `start_eclim.sh` to run eclim.


##Notes

* TODO:  There appears to be intermittent problems with getting the eclim to start.  The whole thing seems a bit fragile, with eclim sometimes starting and sometimes not.  Error messages are not always indicative of the real error.  Looks like I need to add `sudo apt-get install libgtk2.0-0:i386` to the ansible script, because that got it to work one time.



