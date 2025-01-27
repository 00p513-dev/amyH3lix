# amyH3lix

### Jailbreak for iOS 10.x 64bit devices without KTRR in one second.

### Jailbreak for iOS 10.3.4 iPhone5,2 in an instant.

This should be the best variant of H3lix jailbreak tool.

**Replace the exploit from v0rtex to [sock port](https://github.com/jakeajames/sock_port) with higher success rate and shorter time.**

Kernel patches and other resources are inherited from doubleH3lix.

**Only tested on my 5s (10.3.3).** 10.x 64bit KPP devices is supported in theory. **Use at your own risk.**

This jailbreak tool is ***no longer compatible*** with doubleH3lix, which means you can ***NOT*** switch between them ***AT ALL***. Use Cydia Eraser

## Additional modifications:
- Exploit
  - v0rtex -> sock port with higher success rate.
  - Reimplement the sock port exploit on 32bit platform.
- Sandbox
  - Remove a patch which fully disable sandbox for any process. This keeps sandbox container intact and keeps NSUserDefaults (cfprefsd) from storing plist in the unsandbox patch.
  - sockH3lix will call uicache with sock port exploit for sandbox escaping. 
- export tfp0
  - Enable hgsp4 for root process.
- patchfinder32
  - Implement a 32bit patchfinder for iPhone5,2 iOS10.3.4.
- Reduce jailbreak costs, improve jailbreak speed and stability
  - Merge kernel read/write request to reduce syscall count.
  - Add a kernel memory management for remapping pages and page table entries to reduce kernel memory usage after jailbreak.
  - Choose a right size of the fake IOTrap while initializing kexec.
  - Use a large number of Mach primitives and other syscalls that affect scheduling to increase stability.
  - kexec some hardware codes to flush the cache and TLB instead of waiting for the kpp patch to work.
- Bootstrap
    - Switch to Procursus bootstrap
    - Use Zebra instead of the aging Cydia package manager
- User interface
    - Dark Mode
