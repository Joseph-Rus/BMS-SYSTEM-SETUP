# BMS-SYSTEM-SETUP
SEA-EV BMS coding git

setting up a Windows system 

--------------------------------------------------------------------------------------------------------------------

use these YOUTUBE Vidoes to help walk through the BMS setup

https://www.youtube.com/watch?v=PxQw5_7yI8Q

https://www.youtube.com/watch?v=PxQw5_7yI8Q

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
------------------------------------------------------------------------------
TOOLS YOU WILL NEED TO DEBUG

ST-link Debugger
![image](https://github.com/user-attachments/assets/05b4afa8-8dfe-4d95-ab9f-7ad49948b720)
https://www.digikey.com/en/products/detail/stmicroelectronics/STLINK-V3SET/9636028

Power Supply needs to go down to 3.3 volts
https://www.amazon.com/Variable-4-Digits-Adjustable-Regulated-Quick-Charge/dp/B0C17NLZNH/ref=sr_1_1_sspa?crid=EQMYPCZ3BZNX&dib=eyJ2IjoiMSJ9.14BACUt1zvhiTU11Y4kIhojSKiTJOM8dShT-p4diuSni_7n2IFwpZQiVovZa-Egbs057zNRvpJ-6vyYz60iPgC8vI-BPkSB3t-UPi8CvgOOXGsR-X2XJLItpp_jZPXdVweHbv2FA9BblRzDFYD_CIpzzDAZ0QiLLOtXJOYoA4ECYVy7m3CjkjLecUDjGyzhGdBuzzu9BwReUSdjANXekELWhw5pzlNZaT-4ITWdt6zY.GGxq3Cwmrbk29LtyKrg8bjEqxF__Aid-ZuaCWq4yZKM&dib_tag=se&keywords=power%2Bsupply&qid=1723493480&sprefix=power%2Bsuppl%2Caps%2C151&sr=8-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&th=1

-----------------------------------------------------------------------------

Setting up the test board for Debugging


![Screenshot 2024-08-12 132140](https://github.com/user-attachments/assets/705d3aa7-614f-4db2-8535-6262cbcdb8f1)

Blue - GND

Red- 3v3

Green - Stlink

Orange - mini USB




