# ansible-eclim
Files to load eclim for java dev on ubuntu servers

This is a work in progress.  The goal is to make an ansible playbook that will load a fresh ubuntu server (usually in a VBox, but wherever) with a copy of eclim, which allows vim to do pretty decent development on Java, including debugging.  It is a headless development environment.

## Current state of the art

In order to use this repo, you must:

1.  Clone it
2.  Edit the settings (they are in several different variable files) to point to your specific user name.  No passwords are in this right now, nor are any needed.
3.  run `build.sh` to pay the playbook.  (Ansible must obviously already be on the system.  Pretty much everything else will be loaded.)
4.  run `install_eclim.sh` to finish the last step that hasn't quite been put into the playbook yet.
5.  run `start_headless.sh` to run the headless X environment that eclipse needs.
6.  run `start_eclim.sh` to run eclim.


##Notes

* TODO:  add the last step so install_eclim can be done idempotently in the ansible script.
* TODO:  generate the start_ scripts so that they won't need to be edited.  (right now, check them for paths and versions)
* TODO:  make the dang thing work... right now, I'm at the end and there is some annoying problem with eclim that is preventing it from working.  It may be my problem, but I need some help chasing it down.


