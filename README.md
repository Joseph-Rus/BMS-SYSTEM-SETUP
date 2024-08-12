# BMS-SYSTEM-SETUP
SEA-EV BMS coding git

setting up a Windows system 
use these YOUTUBE Vidoes to help walk through the BMS setup
https://www.youtube.com/watch?v=PxQw5_7yI8Q
https://www.youtube.com/watch?v=PxQw5_7yI8Q
--------------------------------------------------------------------------------------------------------------------

download from releases
The BMS code 
make
cmake
openocd


installing / add paths 

to add paths go to edit the system environment

Then click on Environment Variables 

![image](https://github.com/user-attachments/assets/c40e6056-8f35-496f-ab62-afda7d11f964)

click on double-click on paths, then add the paths of where the files are located.
![image](https://github.com/user-attachments/assets/63860b6d-62c6-4e9b-b36b-648beb148703)


--------------------------------------------------------------------------------------------------------------------

Config

```
{
    "configurations": [
        {
            "name": "STM32",
            "includePath": [
                "${workspaceFolder}/**"
            ],
            "defines": [
                "_DEBUG",
                "UNICODE",
                "_UNICODE",
                "USE_HAL_DRIVER",
                "STM32F303xC"
            ],
            "compilerPath": "C:\\Program Files (x86)\\GNU Arm Embedded Toolchain\\10 2021.10\\bin\\arm-none-eabi-gcc.exe",
            "cStandard": "c17",
            "cppStandard": "gnu++17",
            "intelliSenseMode": "gcc-arm",
            "compilerArgs": [

                "-mcpu=cortex-m4",
                "-mthumb"
            ]
           
        }
    ],
    "version": 4
}
```

Launch.json We are using the Cortex Debug you will need to install the extension
```
{
    // Use IntelliSense to learn about possible attributes.
    // Hover to view descriptions of existing attributes.
    // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Cortex Debug",
            "cwd": "${workspaceFolder}",
            "executable": "./main.elf",
            "request": "launch",
            "type": "cortex-debug",
            "runToEntryPoint": "main",
            "servertype": "openocd",
            "device": "STM32F303CCT6",
            "configFiles": [    
                "interface/stlink-v2.cfg",
                "target/stm32f3x.cfg"
            ]
        }
    ]
}
```

