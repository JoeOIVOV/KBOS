# Kill Bluetooth On Sleep (KBOS)
Tired of your bluetooth headphones pairing with a MacOs computer you thought was asleep ? This fixes that

KBOS uses `sleepwatcher` and `Blueutil` to turn off bluetooth when your mac falls asleep, then turns it back on when the computer is woken up. 

## Prerequisites
KBOS requires [Homebrew](https://brew.sh/) which is used to install the following packages:
 * [Blueutil](https://formulae.brew.sh/formula/blueutil#default)
 * [sleepwatcher](https://formulae.brew.sh/formula/sleepwatcher#default)

## Installation
 1. Install [Homebrew](https://brew.sh/) manually first. 
 2. run `bash setup.sh` from this directory.

## Testing
 1. Run each command from Terminal, one at a time: 

/usr/local/Cellar/sleepwatcher/2.2.1/sbin/sleepwatcher -V -s ~/.sleepscripts/disable_bluetooth.sh 
/usr/local/Cellar/sleepwatcher/2.2.1/sbin/sleepwatcher -V -w ~/.sleepscripts/enable_bluetooth.sh 

- Will activate sleepwatcher and provide the verbose output when the computer sleeps or wakes.


### Additional arguments
```
-h, --help                show brief help menu
-d, --disable             disables KBOS, but doesn't uninstall anything.
-e, --enable              re-enables KBOS from a disabled state
-u, --uninstall           removes the ~/sleepscripts directory and the KBOS Plist but does NOT uninstall brew, Blueutil, or sleepwatcher. I'll let you handle that on your own https://docs.brew.sh/FAQ#how-do-i-uninstall-a-formula.

```

## Future improvements
- Attempt to connect to last connected device on wake. 
- Improve script output and robustness


## Report a bug
If this script doesn't work for you, please let me know so I can improve it or feel free to send a pull request. 
