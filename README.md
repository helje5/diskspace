# diskspace

> Fork of [scriptingosx/diskspace](https://github.com/scriptingosx/diskspace)

Returns available disk space

With the various APFS features the value for free disk space returned from
tools such as `du` or `df` will not be accurate. This tool uses system
functions to get various measures of available disk space.

The 'Important' value matches the free disk space value shown in Finder.

You can get the details from Apple's documentation:

https://developer.apple.com/documentation/foundation/urlresourcekey/checking_volume_storage_capacity

```
USAGE: diskspace [--human-readable] [--available] [--important] [--opportunistic] [--total] [<volume-path>]

ARGUMENTS:
  <volume-path>           path to the volume (default: /)

OPTIONS:
  -H, --human-readable    Human readable output using unit suffixes
  -a, --available         Print only the value of the Available Capacity
  -i, --important         Print only the value of the Important Capacity
  -o, --opportunistic     Print only the value of the Opportunistic Capacity
  -t, --total             Print only the value of the Total Capacity
  --version               Show the version.
  -h, --help              Show help information.
```

## Installation using swift-sh

This fork of `diskspace` includes the necessary annotations for
[swift-sh](https://github.com/mxcl/swift-sh).
I.e. the script can execute directly.

To install it just copy the main.swift to your desired location, e.g.:
```
cp diskspace/main.swift /usr/local/bin/diskspace
```

[swift-sh](https://github.com/mxcl/swift-sh) can be installed using a
simple `brew install mxcl/made/swift-sh`.
