- 👋 Hi, I’m @Delmainn
- 👀 I’m interested in embedded systems
- 🌱 I’m currently learning bare-metal programming in C on arm microcontrollers
- 💞️ I’m looking to collaborate on projects relating to microcontrollers that would take me from a beginner to a regular.
- 📫 How to reach me ---> I'm right here ;)
- 😄 Pronouns: Him/Himothy/Himalayas/Himmy Neutron/
- ⚡ Fun fact: I played Sax in high school

<!---
Delmainn/Delmainn is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

Cortex-Debug: VSCode debugger extension version 1.12.1 git(652d042). Usage info: https://github.com/Marus/cortex-debug#usage
Reading symbols from /usr/bin/objdump-multiarch --syms -C -h -w /home/delmain/Bare-Bootloader/app/firmware.elf
Reading symbols from /usr/bin/nm-multiarch --defined-only -S -l -C -p /home/delmain/Bare-Bootloader/app/firmware.elf
Launching GDB: /usr/bin/gdb-multiarch -q --interpreter=mi2
    IMPORTANT: Set "showDevDebugOutput": "raw" in "launch.json" to see verbose GDB transactions here. Very helpful to debug issues or report problems
Error: /usr/bin/nm-multiarch failed! statics/global/functions may not be properly classified: Error: spawn /usr/bin/nm-multiarch ENOENT
    Expecting `nm` next to `objdump`. If that is not the problem please report this.
Error: objdump failed! statics/globals/functions may not be properly classified: Error: spawn /usr/bin/objdump-multiarch ENOENT
    ENOENT means program not found. If that is not the issue, please report this problem.
Launching gdb-server: /usr/bin/gdb-multiarch -p 50000 --no-reset
    Please check TERMINAL tab (gdb-server) for output from /usr/bin/gdb-multiarch
Finished reading symbols from objdump: Time: 27 ms
Finished reading symbols from nm: Time: 23 ms

 *  Executing task: make bin 

make: Nothing to be done for 'bin'.
 *  Terminal will be reused by tasks, press any key to close it. 

 *  Executing task: make bin 

make: Nothing to be done for 'bin'.
 *  Terminal will be reused by tasks, press any key to close it. 

 *  Executing task: make bin 

make: Nothing to be done for 'bin'.
 *  Terminal will be reused by tasks, press any key to close it. 

 

{
    "configurations": [
      // {
      //   "name": "JLink: Debug Application",
      //   "cwd": "${workspaceFolder}/app",
      //   "executable": "./firmware.elf",
      //   "serverpath": "/usr/bin/JLinkGDBServer",
      //   "servertype": "jlink",
      //   "request": "launch",
      //   "type": "cortex-debug",
      //   "device": "STM32F401RE",
      //   "runToEntryPoint": "main",
      //   "interface": "swd",
      //   "preLaunchTask": "build_debug"
      // },
      // {
      //   "name": "JLink: Debug Bootloader",
      //   "cwd": "${workspaceFolder}/bootloader",
      //   "executable": "./bootloader.elf",
      //   "serverpath": "/usr/bin/JLinkGDBServer",
      //   "servertype": "jlink",
      //   "request": "launch",
      //   "type": "cortex-debug",
      //   "device": "STM32F401RE",
      //   "runToEntryPoint": "main",
      //   "interface": "swd",
      //   "preLaunchTask": "build_bootloader"
      // },
      // {
      //   "name": "JLink: Attach to Application",
      //   "cwd": "${workspaceFolder}/app",
      //   "executable": "./firmware.elf",
      //   "serverpath": "/usr/bin/JLinkGDBServer",
      //   "servertype": "jlink",
      //   "request": "attach",
      //   "type": "cortex-debug",
      //   "device": "STM32F401RE",
      //   "runToEntryPoint": "main",
      //   "interface": "swd"
      // },
      // {
      //   "name": "JLink: Attach to Bootloader",
      //   "cwd": "${workspaceFolder}/bootloader",
      //   "executable": "./bootloader.elf",
      //   "serverpath": "/usr/bin/JLinkGDBServer",
      //   "servertype": "jlink",
      //   "request": "attach",
      //   "type": "cortex-debug",
      //   "device": "STM32F401RE",
      //   "runToEntryPoint": "main",
      //   "interface": "swd",
      //   "preLaunchTask": "build_bootloader"
      // },
      {
        "name": "ST-Link: Debug Application",
        "cwd": "${workspaceFolder}/app",
        "executable": "./firmware.elf",
        "serverpath": "/usr/bin/gdb-multiarch",
        "servertype": "stutil",
        "request": "launch",
        "type": "cortex-debug",
        "device": "STM32F411RE",
        "runToEntryPoint": "main",
        "interface": "swd",
        "preLaunchTask": "build_debug"
      },
      {
        "name": "ST-Link: Debug Bootloader",
        "cwd": "${workspaceFolder}/bootloader",
        "executable": "./bootloader.elf",
        "serverpath": "/usr/bin/gdb-multiarch",
        "servertype": "stutil",
        "request": "launch",
        "type": "cortex-debug",
        "device": "STM32F411RE",
        "runToEntryPoint": "main",
        "interface": "swd",
        "preLaunchTask": "build_bootloader"
      },
      {
        "name": "ST-Link: Attach to Application",
        "cwd": "${workspaceFolder}/app",
        "executable": "./firmware.elf",
        "serverpath": "/usr/bin/gdb-multiarch",
        "servertype": "stutil",
        "request": "attach",
        "type": "cortex-debug",
        "device": "STM32F411RE",
        "runToEntryPoint": "main",
        "interface": "swd"
      },
      {
        "name": "ST-Link: Attach to Bootloader",
        "cwd": "${workspaceFolder}/bootloader",
        "executable": "./bootloader.elf",
        "serverpath": "/usr/bin/gdb-multiarch",
        "servertype": "stutil",
        "request": "attach",
        "type": "cortex-debug",
        "device": "STM32F411RE",
        "runToEntryPoint": "main",
        "interface": "swd"
      }
    ]
  }
