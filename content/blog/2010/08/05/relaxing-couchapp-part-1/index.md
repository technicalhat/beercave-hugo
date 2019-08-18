---
title : "Relaxing with CouchApp part 1"
description : ""
tags : []
date: '2010-08-05 20:03:59'
---

I have an epic nerd-boner for non-relational databases, so when I ran across <a href="http://couchapp.org/">CouchApp</a> on Hacker News the other day I had to give it a go.


A CouchApp is a web application built directly on top of <A href="http://www.couch.io">Apache CouchDB</a> - because the database talks HTTP natively, apps can be set up to be served direct to the browser, with none of that tedious mucking about in application layers. The details are explained pretty well in <a href="http://wiki.couchapp.org/page/what-is-couchapp#/">What the HTTP is CouchApp?</a>

<!--more-->

So, now that you know what I'm talking about, what the HTTP am I planning to <i>DO</i> with CouchApp? Well, I've got a few ideas in the pipeline once I've got the hang of it, but for now I was thinking it might be fun to get a quick and dirty clone of the beercave site up and running.

<h3>The now traditional tedious "Getting Started" bit"</h3>
This wouldn't be a proper development article without a laborious description of how to get up and running, now would it. Fortunately, it's not very difficult. So here goes.


<h4 style="margin-left:10px;">Things you'll need before you start</h4>

<ul>
<li><a href="http://www.python.org/">Python</a> - 2.5 or later</li>
<li><a href="http://pypi.python.org/pypi/setuptools">setuptools</a> - sure, you <i>could</i> manually install the couchapp scripts, but why would you want to?</li>
</ul>



Go install those and come back.  I'll wait.


<h4 style="margin-left:10px;">Things you'll need to get started</h4>

<ul>
<li><a href="http://www.couch.io/get">CouchDB</a> - I've played with the Windows and Mac builds and they were both incredibly painless to get running. Download, unzip & run and you have your own database instance right there. A far cry from your standard Open Source scenario of "download these <i>exact</i> versions of 123 different packages and build them from source or fuck off, noob!"</li>
<li>Some sort of text editor would probably come in handy ;) I use <a href="http://notepad-plus-plus.org/">Notepad++</a> on windows. If you like something else, use that instead. If you try and embroil me in a vim vs. emacs war I will <i>kill you with knives</i>. Large, shiny knives. I have <i>several...</i></li>
</ul>


<h4 style="margin-left:10px;">The Install</h4>

Unzip the CouchDB binaries somwhere you'll find them again and start it up. C:\Program Files\CouchDB would be a good choice for Windows types, Mac users might want to try the Applications folder.If you're installing from source, you probably know what you're doing, so go to it.


Pop open a command window and install the CouchApp scripts:
<p/>
<pre style="background-color: #ccc; -moz-border-radius: 5px; -webkit-border-radius: 5px;font-family: monospace; border: 1px solid #000; margin-left:10px;margin-right:10px; padding: 10px;">easy_install couchapp
</pre>

Now create yourself a shiny new CouchApp!


<pre style="background-color: #ccc; -moz-border-radius: 5px; -webkit-border-radius: 5px;font-family: monospace; border: 1px solid #000; margin-left:10px;margin-right:10px; padding: 10px;">
C:\DevSoftware\projects>couchapp generate beercave
2010-08-05 19:17:38 [INFO] C:\DevSoftware\projects\beercave generated.
</pre>

This generates you the skeleton of your new CouchApp.<br/>
If you set up an admin account on your CouchDB, now's the time to fill in its details in the new .couchapprc file


<pre style="background-color: #ccc; -moz-border-radius: 5px; -webkit-border-radius: 5px;font-family: monospace; border: 1px solid #000; margin-left:10px;margin-right:10px; padding: 10px;">
{
"env": { 
"default": {
  "db": "http://username:password@localhost:5984/beercave"
}
}
}
</pre>

Now that that's done, just publish your new CouchApp to CouchDB.


<pre style="background-color: #ccc; -moz-border-radius: 5px; -webkit-border-radius: 5px;font-family: monospace; border: 1px solid #000; margin-left:10px;margin-right:10px; padding: 10px;">
C:\DevSoftware\projects\beercave>couchapp push
2010-08-05 20:11:33 [INFO] Visit your CouchApp here:
http://localhost:5984/beercave/_design/beercave/index.html
</pre>

Now just follow the <a href="http://localhost:5984/beercave/_design/beercave/index.html">link</a> and you should see something like this:<br/>
<a href="http://s24.photobucket.com/albums/c12/b33rman/beercave/?action=view&current=couch1.jpg" target="_blank"><img src="http://i24.photobucket.com/albums/c12/b33rman/beercave/th_couch1.jpg" border="0" alt="Photobucket"></a><br/>
Not <i>much</i> like the beercave site yet, but we'll get to that.

