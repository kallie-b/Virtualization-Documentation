# Memory scripts

## clear-MemoryReserve-regkey.ps1
Clears the (now deprecated) MemoryReserve registry key if it is set.

This key controls how much memory Hyper-V sets aside for the host.  By default, Hyper-V root reserve is:  
384MB + 30MB per 1GB of physical memory on the host machine.

To run the script, open PowerShell and run:
``` PowerShell
Invoke-WebRequest -Uri https://raw.githubusercontent.com/Microsoft/Virtualization-Documentation/live/hyperv-tools/root-memory-reserve/clear-MemoryReserve-regkey.ps1 -OutFile clear-MemoryReserve-regkey.ps1
.\clear-MemoryReserve-regkey.ps1
```


For changes to take effect, restart the vmms.

``` PowerShell
Restart-Service vmms
```
