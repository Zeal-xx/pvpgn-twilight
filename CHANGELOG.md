# PVPGN-Twilight Changelog

This document describes the differences and additions from the original PVPGN
project.

## 2009-01-07 = Wednesday 7 Jan 2009

*Changes listed here are current in the development branch. While the code
compiles, it is not meant to be run. It has not been tested by the developers.
These changes will migrate into a versioned release once testing is complete.*

all changes here relate to framework for the [experience system][expsys]

### command changes

* command#_handle_setlevel_command created
* command#_handle_setexperience_command created
* command#_handle_level_command created
* command#_handle_setlevel_command created
* command#_handle_setal_command created
* command#_handle_getal_command created
* command#_handle_lockacct_command completely rewritten
* command#_handle_unlockacct_command completely rewritten
* command#_handle_serverban_command changed to call _handle_lockacct_command
  instead of calling account_wrap#account_set_auth_lock

### account changes

* account_wrap#convert_level_to_experience created
* account_wrap#convert_experience_to_level created
* account_wrap#account_get_experience created
* account_wrap#account_set_experience created
* account_wrap#account_get_level created
* account_wrap#account_set_level created
* account_wrap#account_can_join_game created
* account_wrap#account_set_auth_lock changed to require a locker account

### connection changes

* access_level added to connection internal access
* connection#conn_get_access_level
* connection#conn_set_access_level
* connection#conn_set_account changed to set a default access_level
* connection#conn_can_join_game created
* connection#conn_set_game changed to use the new game#game_create (level)

### game changes

* level added to game internal access
* game#get_level created
* game#set_level created
* game#game_create changed to intialize a level
* command#_glist_cb changed to filter non-open games
* command#_glist_cb changed to filter games by level, using conn_can_join_game

## 2009-01-08 = Thursday 8 Jan 2009

*Changes listed here are current in the development branch. While the code
compiles, it is not meant to be run. It has not been tested by the developers.
These changes will migrate into a versioned release once testing is complete.*

### command changes

* command#_handle_experience_command changed to show exp to next level
* command#_handle_setal_command rewritten to opt-out style
* command#_handle_oper_command created

### message changes

* message#message_send_operators created

[expsys]: http://wiki.github.com/marcbowes/pvpgn-twilight/experience-system "Experience System @ PVPGN-Twilight Wiki"
