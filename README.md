# lv-bin

lv-bin is a collection of labview utilities which reference self-contained binaries and/or commands available in Windows. although the libraries aren't limited to Windows, all of the libraries are generally OS specific (e.g. Windows 7/10 etc).

## Installation

Although lv-bin is a collection of packages, the non lv-bin (e.g. lv-bin-7zip) don't reference lv-bin within the repo, but lv-bin from the vi.lib (or rather user.lib). lv-bin is a dependency to any of those packages.

Either build a vip using the appropriate *.vip file in the distribution folder or copy the contents of the source directory into user.lib/antonio-alexander.

## Description

lv-bin only contains auxiliary functionality, mostly the ability to generate temporary folders, and manage pathing. Many of the lv-bin-packages work on the idea that the binaries are within the provided application rather than installed externally (e.g. with an installer). This makes your application footprint smaller and there's less to manage on uninstall or conflicting applications.

For anyone importing the package to create their own lv-bin libraries, note that the "api" is separated into a v1 package to attempt to maintain the api for major vesion 1, in the event that non-forward compatible changes are added, previous functionality should be maintained and new features with a different namespace (e.g. v2).

## __lv-bin-template__

Packages are self-contained, their main dependency is the lv-bin package (this package). Keep in mind that binaries ARE NOT bundled with the application, you'll need to source them yourself (instructions within their readmes).

## Disclaimers

There's a lot to be said about how to distribute executables within your application. Be as careful as possible
