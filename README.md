


About
=====
Originally forked from Mitlik [https://github.com/Mitlik/tt-on-rod] who initially referenced Scandum's scripts found here : [https://tintin.mudhalla.net/scripts/]
License is WTFPL, aka do what the fuck you want. 

Notes
=====
*   The "Logs" directory will need to exist in order for various logging
    functions to write correctly. So the directory will be under version
    control, so git clone can pull it.  

*   **BEWARE** older releases do not have Utilities/worlds.dat in .gitignore
    and it is possible to commit it with sensitive data.

Getting Started
===============
After downloading the files, you'll want to remove the .example from the files 
module.conf.example and system.conf.example and replace the information with
your preferred setup. Then it's as simple as running:

    tt++ path/to/main.tin

Once there you can add characters via the "addworld" command, and connect to
one of those worlds using the alias "cn".

For further information, the simplest way to get started is to head into the 
project directory and run:

    grep -r "ALIAS" . && grep -r "FUNCTION" .

Project Structure
=================
The basic layout should be something like:
<pre>
+-PROJECT_HOME: the head project directory
  +-Characters: where character specific files go
  +-Logs: this is the default folders should write logs to
  +-Modules: where RoD specific scripts are stored
  +-Utilities: where generic scripts are stored (i.e. scripts that only
    deal with Tintin)
  +-main.tin: this one file should read in everything you need in #gts and
    to load up your characters
  +-modules.conf: this turns modules on and off, and may define variables
    for those modules
</pre>

Types of files:
<pre>
  .tin | Contain aliases, functions, actions, etc.
  .dat | Contain only data for use in another script (e.g. character listing
       | or equipment damage listing)
 .conf | Setup variables that a user might change
</pre>

Road Map
========
Athena : As a new player I haven't a clue what some of these milestones mean, but I do want to learn.

Subject to change. Part of sharing is hoping that another mind can come up with
some neat ideas to include.

Version 1
---------
Milestone goal: Help make tintin easier to use for logging in and offer some
neat features

- [X] Simplified connect with stored character data
- [ ] Separate Comms area
- [ ] Simple speed walk with storage: check vs built-in speedwalk
- [X] Basic MSDP
- [ ] Basic battle scripts
    - [X] Disarm
    - [ ] Cure blind if true sight runs before gouge/blind

Version 2
---------
Milestone goal: Improve scripts to be more useful

- [ ] Have option to encrypt character passwords
- [ ] Search data for certain criterion
    - [ ] Characters
    - [ ] Speedwalks/Areas
- [ ] Unfailing spell bots
- [ ] Alexian compatible auction logging
    - [ ] bash script to merge log into db source and pick out obvious repeats

Version 3
---------
Milestone goal: Add some features that might be considered ridiculous

- [ ] Auto-CR (spam visit deities only)
- [ ] Auto-Fight

