## KeePassExport
###Description
I’ve been Moleskine’ing for a while now, and have the need to keep a bunch of passwords in printed form (on paper).  Keepass is my tool of choice for the digital repository of passwords, of which I keep on my cheap-man’s VPS (my version of a “cloud”).

This utility displays a Vigenère matrix for a given KeePass export.  It is encrypted with a given key provided at the command line.

[Read more about Vigenère Ciphers.](http://en.wikipedia.org/wiki/Vigen%C3%A8re_cipher)
###Usage
The usage is simple:  Export your Keepass database into XML plaintext, then pipe that into the script with a password, and it will print out the encoded Vigenère cipher to STDOUT.

This will work for Keepass 1 and 2.

```$python KeePassExport.py -key=<yourpassword> -file=export.xml -action=PARSE1.0```

* -key (required): the key for your Vigenère cipher
* -file (required): XML file output from KeePass
* -action (required): PARSE1.0 and PARSE2.0 are valid options, and are used to indicate what version of KeePass generated the file export
