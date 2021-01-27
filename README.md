BL654 smartBASIC-Applications
=============================

A repository for smartBASIC applications that run on the Laird Connectivity BL654 (Released under the ISC License).

BL654 Overview
------------
Laird Connectivity’s BL654 contains the latest generation silicon with Bluetooth Low Energy v5 capabilities and groundbreaking ultra-low power performance. Building on the expertise of the BL600 and BL652 Series, the BL654’s class-leading Nordic nRF52840 silicon, optimized low power schemes and smartBASIC programming language provide a secure, stable, hostless Bluetooth environment. The BL654 introduces Bluetooth v5, bringing long range connectivity, industrial security and feature expansion to Laird Connectivity’s proven Bluetooth Low Energy modules. Let Laird Connectivity’s innovative BL654 series and decades of expertise in Bluetooth module design speed your product to market.

UwTerminalX
-----------
UwTerminalX is a cross-platform utility for communicating and downloading applications onto the BL654. The latest releases are available at https://github.com/LairdCP/UwTerminalX/releases

BL654 Documentation
-------------------
Documentation for the BL654 can be found on the [Laird Connectivity BL654 website](https://www.lairdconnect.com/wireless-modules/bluetooth-modules/bluetooth-5-modules/bl654-series-bluetooth-module-nfc) and documentation for the BL654PA can be found on the [Laird Connectivty BL654PA website](https://www.lairdconnect.com/wireless-modules/bluetooth-modules/bluetooth-5-modules/bl654pa-series-long-range-bluetooth-module), including a [quick start guide for using the AT interface application](https://www.lairdconnect.com/documentation/interface-quick-start-guide-v1-0pdf) and [user guide for the AT interface application](https://www.lairdconnect.com/documentation/user-guide-bl654-interface-application)

Older firmwares
-------------------------------
The files in this repository are designed for use with the latest BL654 firmware, which at the time of writing is 29.5.7.2. For applications targeting older firmware, please check the [Releases tab](https://github.com/LairdCP/BL654-Applications/releases)



Best Practices for Writing smartBASIC Applications
-------------------------------
1. Always check the resultcode returned from an API function. Non-zero result codes usually indicate that the operation has not been successful.
2. smartBASIC is event driven; ensure that the application is written in an event-driven manner. Starting with a state-machine or a flowchart is highly recommended.
3. Minimize the use of WAITEVENTs; ideally, WAITEVENT should be used only once at the end of the program to ensure the app is simple and robust.
4. Minimize radio usage when possible to save power.
5. Use comments wherever possible to ensure that the application can be read and understood.
6. Only hard-code when necessary. When hard-coding, use #defines to give meaning to the constants used.
7. Follow the smartBASIC app template found [here](https://github.com/LairdCP/BL654-Applications/blob/master/Applications/ttt.template.sb).

Notes
-------------------------------
Please note that for simplicity reasons, some sample apps have been written without important features such as error handling or result code checking. However, when writing your applications, please ensure that result codes returned from the API functions are always checked to ensure that your applications are robust and bug-free.
