# BMS-SYSTEM-SETUP
SEA-EV BMS coding git

setting up a Windows system 


downloads
code 
make
cmake
openocd


installing

cmake
make
openocd

add paths

file setup 
config.json
launch.json

Windows System setup for BMS system 

Click this link to get system Requirements and the stlink Release
http://Github.com/stlink-org/stlink
click on the Debian Linux this is because a windows system can handle the Debian Linux because of sand box Linux subsystem that windows as add (if you do not have thin setup you will need to set it up) 

 
SYSTEM REQUIREMENTS
-	Cmake ( Download CMake )
-	Make ( Make for Windows (sourceforge.net) )
Click on the Complete package, except sources
 
-	Arm toolchain make sure you install GCC ( Downloads | GNU Arm Embedded Toolchain Downloads – Arm Developer )
 
You do not need laibusb and libgtk-dev

Openocd install
Download OpenOCD for Windows (gnutoolchains.com)

Here are some good walk through videos this for openocd and setup
https://www.youtube.com/watch?v=PxQw5_7yI8Q
https://www.youtube.com/watch?v=PxQw5_7yI8Q

Click on the win32 when in the main/main.cpp file and then click on the .json to make a .json file then input your information of board and compilerpath.


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

BEFORE RUNNING THE COMMAND MAKE SURE TO SET THE (version)
We are using the HV so set the number to 1 in the file location main/generalDefines.h/ENNOID_HV
 
Ater doing so run the command make to compiler








After installing everything download the code from ( EnnoidMe/ENNOID-BMS-Firmware at ENNOID (github.com) )

Part Needed
Debugger ( STLINK-V3SET STMicroelectronics | Development Boards, Kits, Programmers | DigiKey )
1x BMS testing Board 


Section 32 loop back mode


