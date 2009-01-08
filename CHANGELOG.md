# PVPGN-Twilight Changelog

This document describes the differences and additions from the original PVPGN
project.

## 2009-01-07 = Wednesday 7 Jan 2009

*Changes listed here are current in the development branch. While the code
compiles, it is not meant to be run. It has not been tested by the developers.
These changes will migrate into a versioned release once testing is complete.*

* all changes here relate to framework for the [experience system][expsys]
* games filtered so that only users with the same level or higher can see them
* added experience (or /exp) command which returns the users current experience
* added setexperience (or /setexp) command which changes the specified users experience
* added level command
* added setlevel command for admins
* admins are notified if lockacct/unlockacct is used on an account which is already locked
* added getal which returns the users current access level
* added setal which allows the user to change their access level

## 2009-01-08 = Thursday 8 Jan 2009

*Changes listed here are current in the development branch. While the code
compiles, it is not meant to be run. It has not been tested by the developers.
These changes will migrate into a versioned release once testing is complete.*

* experience command shows experience to next level
* setal checks bounds against global min/max and user's level

[expsys]: http://wiki.github.com/marcbowes/pvpgn-twilight/experience-system "Experience System @ PVPGN-Twilight Wiki"
