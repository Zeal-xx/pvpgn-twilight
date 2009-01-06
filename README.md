# PVPGN.bnetd ala Twilight

This project focuses at providing the following functionality to bnetd. Note
that almost all changes are designed with DotA (a custom map) for W3XP in mind.
However, changes here can be beneficial to any game, provided the right
adjustments are made.

## History

PVPGN/bnetd is an opensource project which emulates Blizzard's Battle.NET.

The project is old, and thus quite mature. While it does a marvelous job
at cloning the functionality and behavior of the official servers, it has a
serious flaw: account control. While Blizzard have the luxury of authenticating
CD keys, PVPGN hosts do not. This makes it incredibly frustrating running
a bnetd server - it just takes one user intent on ruining it for everybody else,
and you have a big problem on your hands.

While IP banning can be effective, not all users sit behind static addresses.
Furthermore, custom games don't always follow the same ruleset as the
traditional W3XP AUP. For example, for DotA, will your server tolerate leavers,
item poolers, laggers, feeders.. there are a host of control issues - none of
which can be moderated via traditional Battle.NET controls.

The Twilight modifications have been running on Twilight[http://war3.co.za] with
much success for the better part of a year. The original source was based off
PVPGN 1.99.r384 (a snapshot at the time), and has been maintained with SVN.
Since then, there have been many requests for the source. While originally
hesitant, I have decided to opensource the project. However, the code
presented here is (or rather, will be) a full rewrite of the modifications.

## Twilight itself

From the long splurb above, one thing should be clear: PVPGN is great at
pretending to be Blizzard's Battle.NET.. but that's just the problem, ain't it?
Battle.NET is an old system designed in almost another era. PVPGN developers
do not have any intention of *deviating* from the Battle.NET design. That's
where we come in. Our entire goal is to make bnetd fun for all. We don't care
how much of BNET we molester in the process. If it works out to be a better
system.. well, then that's Mission Accomplished.

This is a very brief overview of the features involved.
* Experience system
* Group system
* Normalised database for MYSQL
* Simple web management, written in Rails for use with MYSQL

More information about current and future features can be found at the
[wiki](http://github.com/marcbowes/pvpgn-twilight/wikis) for this project.

## Layout

PVPGN is developed using SVN. This project is maintained using git, and git-svn
for keeping the project up to date with the SVN trunk of PVPGN. The master
branch of this project is therefore a hybrid between the upstream of PVPGN and
the development branch of our mods.

## Contributing

Please see ['contributing' on the wiki](http://github.com/marcbowes/pvpgn-twilight/wikis/contributing)

## Installation

First you need a copy of the code. Either grab it using git:

    % git clone git://github.com/marcbowes/pvpgn-twilight.git
    
or, you can get it through github's download system:
  * [tarball](http://github.com/marcbowes/pvpgn-twilight/tarball/master)
  * [zip](http://github.com/marcbowes/pvpgn-twilight/zipball/master)

The recommended install method is using cmake. As you might notice, git is
setup to ignore the build/ directory in the base of project. Once cmake is
installed, you should be able to (assuming NIX environment):

    % cd /path/to/pvpgn-twilight/
    % mkdir build
    % cd build
    % cmake ../pvpgn
    % make
  
For further information, please see
[README.cmake](http://github.com/marcbowes/pvpgn-twilight/tree/master/pvpgn/README.cmake)

# Other information

## Authors
  * Marc Bowes <marcbowes@gmail.com>
  
## External links
  * [PVPGN home](http://pvpgn.berlios.de)
  * Twilight [home](http://war3.co.za/) and [forums](http://forum.war3.co.za)
  
## Credit

Original credit to the PVPGN guys, without whom none of this would be possible.
I would especially like to thank d1zzy, who, despite the many many lazy people
throwing many many stupid questions at him, still finds it in him to help out.
Without his input, this venture would have been far more painful.
  
## Licensing

PVPGN is released under GPL-v2 (at the time of writing). However, this may
change in the future. Regardless, this project is re-released under whatever
license PVPGN chooses to use. Below is a copy of the current license.

> This program is free software; you can redistribute it and/or
> modify it under the terms of the GNU General Public License
> as published by the Free Software Foundation; either version 2
> of the License, or (at your option) any later version.
> 
> This program is distributed in the hope that it will be useful,
> but WITHOUT ANY WARRANTY; without even the implied warranty of
> MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
> GNU General Public License for more details.
> 
> You should have received a copy of the GNU General Public License
> along with this program; if not, write to the Free Software
> Foundation, Inc., 59 Temple Place - Suite 330, Boston, MA  02111-1307, USA.

