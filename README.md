# paket.bootstrapper.exe shim

```text
+-----------------------+
|   bootstrapper shim   |
+-----------+-----------+
            |
            |
            |
+-----------+-----------+
|     bootstrapper      |
+-----------+-----------+
            |
            |
            |
+-----------+-----------+
|         paket         |
+-----------------------+
```


This is a script that acts as a shim for [`paket.bootstrapper.exe`](http://fsprojects.github.io/Paket/bootstrapper.html).  
What it does actually is that it downloads the latest version of the bootstrapper,
if it doesn't already exist, it then it just executes it. That is all.  
So in some sense this script is a bootstrapper for the bootstrapper.

For the download of the binary it first tries github
and only upon failure does it proceed to nuget.

## Why

Only one reason I can think of.  
Committing in your source control
~2KB of shell code instead of ~30KB of binary code.
