---
title : "DethTank Demo update"
description : ""
tags : []
date: '2010-10-18 21:26:14'
---

I've been alerted to some issues with the previous release on windows 7, apparently due to my referencing a specific dll version for the DirectInput support. Looking into the problem also highlighted that the ClickOnce installer that Visual Studio Express generates is a bit... odd, not least in its choice of install location (somewhere in &lt;user&gt;\local settings\Apps\2.0\BIGUGLYGUID)

For anyone who doesn't want to deal with all that, I've packaged an alternative version that will just unzip and run, including an alternative version of the exe with all references to DirectInput removed.

Download it here (15MB)
<div class="download">
<a href="https://s3.amazonaws.com/beercave.co.uk/DethTankDemoNoInstaller.zip">Download</a>
</div>

You may also need the <a href="http://msdn.microsoft.com/en-gb/netframework/cc378097.aspx">.Net Framework 3.5</a> and <a href="http://www.microsoft.com/downloads/en/details.aspx?FamilyID=53867a2a-e249-4560-8011-98eb3e799ef2&displaylang=en">XNA Framework 3.1</a> redistributables if you don't already have them installed.

<!--more-->
