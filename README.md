# lv-bin

lv-bin is a collection of labview utilities which reference self-contained binaries and/or commands available in Windows. although the libraries aren't limited to Windows, all of the libraries are generally OS specific (e.g. Windows 7/10 etc).

## Installation

Although lv-bin is a collection of packages, the non lv-bin (e.g. lv-bin-7zip) don't reference lv-bin within the repo, but lv-bin from the vi.lib (or rather user.lib). lv-bin is a dependency to any of those packages.

Either build a vip using the appropriate *.vip file in the distribution folder or copy the contents of the source directory into user.lib/antonio-alexander.

## Description

lv-bin only contains auxiliary functionality, mostly the ability to generate temporary folders, and manage pathing. Many of the lv-bin-packages work on the idea that the binaries are within the provided application rather than installed externally (e.g. with an installer). This makes your application footprint smaller and there's less to manage on uninstall or conflicting applications.

For anyone importing the package to create their own lv-bin libraries, note that the "api" is separated into a v1 package to attempt to maintain the api for major vesion 1, in the event that non-forward compatible changes are added, previous functionality should be maintained and new features with a different namespace (e.g. v2).

## Available packages/Additional Documentation

Packages are self-contained, their main dependency is the lv-bin package (this package). Keep in mind that binaries ARE NOT bundled with the application, you'll need to source them yourself (instructions within their readmes).

* lv-bin: base package used as an internal dependency for the other packages, it's documentation is available in [source/lv-bin/README.md](source/lv-bin/README.md)
* lv-bin-7zip: gives you the ability to extract and compress archives in supported formats (e.g. 7zip, zip), it's documentation is avilable in [source/lv-bin-7zip/README.md](source/lv-bin-7zip/README.md)
* lv-bin-wget: gives you the ability to download a file from the internet, it's documentation is available in [source/lv-bin-wget/README.md](source/lv-bin-wget/README.md)
* lv-bin-git: (currently) only gives you the ability to get the git commit hash of a given directory, it's documentation is avialable in [source/lv-bin-git/README.md](source/lv-bin-git/README.md)

## Disclaimers

There's a lot to be said about how to distribute executables within your application. Be as careful as possible
