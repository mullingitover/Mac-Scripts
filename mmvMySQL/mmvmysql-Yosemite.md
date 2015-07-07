#Yosemite OS X 10.10 and MySQL

MySQL and Apple have recently taken steps forward in their respective software development. In some ways OS X and MySQL are walking down separate paths at this point. We are making a few tweaks to our scripts to help with that.

Here are the events that lead up to the creation of our script:
+ MySQL has used StartupItems to auto start MySQL on boot for it’s OS X installer
+ Apple has deprecated StartupItems for quite some time (OS X 10.4)
+ There has been a MySQL [bug report](http://bugs.mysql.com/bug.php?id=59855) that dates back to 2011 about this
+ Apple finally dropped support for StartupItems in OS X 10.10 Yosemite
+ MySQL uses a mysql.server script as a part of their preference pane
+ The MySQL preference pane is a nice way to toggle MySQL off and on
+ Writing a Launchd plist to start MySQL would break the usability of the preference pane
+ We wrote a Launchd plist that ~~simply starts mysql.server~~ looks for networking on boot and starts MySQL once the mysql.server script can start MySQL with the proper ‘hostname’.pid

If you upgraded to Yosemite and you can’t get MySQL to auto start on boot anymore - you can run this script:


	 bash <(curl -Ls http://git.io/9QjHYg)

We’re going to release an updated MySQL installer script by December 9th that will incorporate these changes.
