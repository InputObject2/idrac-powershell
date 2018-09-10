# idrac-powershell
## Getting the console to work on 11th gen PowerEdge servers

[I used the java parameters from some other source](https://gist.github.com/xbb/4fd651c2493ad9284dbcb827dc8886d6) before and wrapped it in a nice, easy to use Powershell tool. Full credits to whoever did this, they saved me from (more) hours of messing around.

The Java version needed is 1.7.0. [It can be acquired here.](http://www.oracle.com/technetwork/java/javase/downloads/java-archive-downloads-javase7-521261.html) It needs to be installed in the same folder as this script.

You'll end up with basically this :

```
jre/*
lib/avctKVMIO.dll
lib/avmWinLib.dll
avctKVM.jar
connect-drac-console.ps1
README.md
serverlist.csv
```

## Updating the server inventory
Running the script will prompt at first to add a server, further runs will show the list and allow a user to connect to the servers that were already entered.

The list can also be entered into the included .csv file.

## Some notes
avctKVMIO.dll & avmWinLib.dll come from one of my server's iDRAC console connection file (viewer.jnlp). They can be retrieved from your server on the URL in there. 

The console settings in the iDRAC menu should be set to *native*.

