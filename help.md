# Tools

## Memory Analysis

### Volatility 2.6

vol.exe -f <file.mem> imageinfo

vol.exe -f <file.mem> --profile=<profile> 

(Mem Analysis)[https://medium.com/@davidschiff_35251/memory-analysis-for-beginners-with-volatility-coreflood-trojan-part-1-89981433eeb6]
windows.bigpools
windows.cachedump
windows.callbacks
windows.cmdline
windows.crashinfo
windows.devicetree
windows.dlllist
windows.driverirp
windows.drivermodule
windows.driverscan
windows.dumpfiles
windows.envars
windows.filescan
windows.getservicesids
windows.getsids
windows.handles
windows.hashdump
windows.info
windows.joblinks
windows.ldrmodules
windows.lsadump
windows.malfind
windows.mbrscan
windows.memmap
windows.mftscan
windows.modscan
windows.modules
windows.mutantscan
windows.netscan
windows.netstat
windows.poolscanner
windows.privileges
windows.pslist
windows.psscan
windows.pstree
windows.registry
windows.registry
windows.registry
windows.registry
windows.registry
windows.sessions
windows.skeleton_key_check
windows.ssdt
windows.statistics
windows.strings
windows.svcscan
windows.symlinkscan
windows.vadinfo
windows.vadwalk
windows.vadyarascan
windows.verinfo
windows.virtmap


Use volatility and get the imageinfo to determine which command to get network connections, and filter by port 4444:

```
volatility_2.6_win64_standalone.exe -f image.vmem imageinfo
volatility_2.6_win64_standalone.exe -f image.vmem --profile=Win7SP1x64 netscan | findstr "4444"
```

Output:

```
0x13e5a4cf0        TCPv4    192.168.220.130:49160          192.168.220.129:4444 ESTABLISHED      2792     taskmgr.exe
```

