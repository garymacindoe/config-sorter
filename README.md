# config-sorter

[![Build Status](https://travis-ci.org/garymacindoe/config-sorter.svg?branch=master)](https://travis-ci.org/garymacindoe/config-sorter)

Gentoo's portage package manager uses configuration files to unmask unstable branch packages to install, configure package-specific USE flags or choose which software licenses to accept.  The ```emerge``` command can automatically add entries to these files when they are required.  These entries look like this:

```
# required by media-sound/ardour-3.5.403::gentoo[lv2]  
# required by @selected  
# required by @world (argument)  
=dev-libs/serd-0.20.0 ~amd64  
# required by media-sound/ardour-3.5.403::gentoo[lv2]  
# required by @selected  
# required by @world (argument)  
=dev-libs/sord-0.12.2 ~amd64  
```

This utility sorts configuration files by package atom keeping the comment blocks above the relevant entries.  Multiple keywords/flags/licenses on each line are also sorted keeping the package atom at the start of the line.
