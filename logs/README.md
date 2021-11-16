# logs

This folder contains examples of healthy log files that can be used as a reference point.

- **LastRunWine-CX64Bit19.0.1-1** uses CX64Bit19.0.1-1
- **LastRunWine-CX64Bit19.0.1-1-play** uses CX64Bit19.0.1-1 and records a failed osu!standard beatmap play, instead of immediately exiting to the menu screen
- **LastRunWine-CX20.0.2** uses CX20.0.2

## CX64Bit19.0.1-1 Wineskin

Version 11.4 (Build 20F71)
Engine: WS11WineCX64Bit19.0.1-1
Wineskin 2.9.0.6 1
Release: Stable40
Quarantine attribute is absent (bundle)
Quarantine attribute is absent (wrapper)
Execute flag is present
Detect Direct3D is disabled
Compatibility mode is disabled
System Integrity Protection is enabled
Engine version is supported
Razer Synapse is absents
Log file: update.log is absent
No errors in: runtime.log

## CX20.0.2 Wineskin

Version 11.4 (Build 20F71)
Engine: WS11WineCX20.0.2
Wineskin 2.9.0.7-rc4
Release: Stable40
Quarantine attribute is absent (bundle)
Quarantine attribute is absent (wrapper)
Execute flag is present
Detect Direct3D is disabled
Compatibility mode is disabled
System Integrity Protection is enabled
Engine version is supported
Razer Synapse is absent
Log file: update.log is absent
No errors in: runtime.log

## Developer environment

Although these logs were executed on an older Wineskin on a standard Intel 80386 Mac, they should still look similar to Apple Silicon devices, newer Wineskins or versions of macOS (though there may be some minor differences).
```
Model Name:	MacBook Pro
Model Identifier:	MacBookPro13,1
Processor Name:	Dual-Core Intel Core i5
Processor Speed:	2 GHz
Number of Processors:	1
Total Number of Cores:	2
L2 Cache (per Core):	256 KB
L3 Cache:	4 MB
Hyper-Threading Technology:	Enabled
Memory:	8 GB
System Firmware Version:	429.120.4.0.0
SMC Version (system):	2.36f102 
```
Detailed CPU information available in [machdep.cpu.log](machdep.cpu.log)

## Binary

```bash
~> file osu\!.app/Contents/Resources/drive_c/osu\!/osu\!.exe
osu!.app/Contents/Resources/drive_c/osu!/osu!.exe: PE32 executable (GUI) Intel 80386 Mono/.Net assembly, for MS Windows
```
