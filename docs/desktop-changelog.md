# Change Log IRCBLOQV4

## V4.1.5

- **Fix Bug**

    1. Upload Firmware Bug after update to V4.1.4.
	
## V4.1.4

- **New feature**

    1. Application NEW auto-update feature is now supported.
    2. Supports opening multiple apps at the same time.
    3. Add software new loading interface.
    4. Disable the edit button in the menu bar in upload mode.
    5. Optimize and reduce the file size of external resources.
    6. Merge the installation files for the 32-bit and 64-bit versions of the windows version.
    7. When saving a project without a hardware device, convert it to a format supported by scratch3, so that scratch3 can open the pure scratch project created by ircbloq. (The save format is still .ib but scratch can be forced to open)

- **Fix bug**

    1. Fix the problem that the software needs to copy the cache when it is first started, resulting in no display for a long time. After the user clicks the startup icon multiple times, multiple programs operate on the cache at the same time, causing the cache file to be damaged. Then the program fails to start.
    2. Fix wrong translation of button to turn on and off acceleration mode.
    3. After selecting arduino uno and then mega2560, the pin menu is not updated.
    4. The arduino pin interrupt function code is not right.
    5. The python variable increase block will cut off the first digit after inputting more than two digits.
    6. The generated code logic is incorrect when using a repeating block on a head block other than a hardware device startup event block.
    7. The arduino's comparison block generates code that does not conform to the rules of the C language when the input is a pair of strings or a single character.
    8. In micropython, since there is no global declaration for the custom variable in the function defined by the custom function or event, an error will be reported when using the custom variable block under these blocks.
    9. Adjust the micropython code generation structure to prevent variables and functions from being called before the definition declaration.
    10. Blocks generate code when they are dragged from the toolbar but not yet placed in the workspace.
    11. Fix the arduino device sometimes wait for more than ten seconds to start uploading after the compilation is completed.

## V4.1.3

- **New feature**
	
	1. Added code editing support, now you can edit the code after unlocking the code area.
	2. Changed Loading animation at start
	3. Hide costumes and sound stage in Program mode
	4. Added courier New font, modified wait block in python, removed event xml in program mode
	5. Add a new condition to check whether the block is in the custom block.
	6. device icon added for each device in Category header
	7. added some features for future update

- **Fix bug**
	1. fix: change block in micropython not accepting more than 2 digits
	2. fix: Lists in micropython
	3. fix: now you can numbers in String Format
	4. esp32 and 8266 interrupt bug fix
	5. fix the problem that the newly created list variable under arduino is displayed in the code area.

## V4.1.2

- **New feature**

    1. Added Main App Update Checking
    2. Added Sounds for Blocks adding and Deletion 
    3. Optimize the windows nsis installation script. Now the first installation path will be set to the root directory of the c drive, and the subsequent installation path will be automatically detected and modified to the installation directory selected during the first installation.
    4. Add support for original scratch project files.
    5. Add the eric to the sprite and custom library.

- **Fix bug**

    1. Switching the programming mode while the sprite is speaking will cause the interface to crash.
    2. When loading a project file containing custom list variables, an error will be reported that the loading cannot be completed.
    3. The parameter blocks of custom functions will be disabled when switching modes.
    4. The serial port data of esp32 and microbit is not displayed in the terminal.
    5. Correct the programming language icon of esp32 and NodeMCU.
    6. Port not disconnecting While uploading Error caused.

## V4.1.1

**Bug Fixes**

- Improving compiling and upload speed
- code space is empty if load a same project with no device extension twice
- Modify the parameter name to make it more appropriate to its function
- Misspelled LearnMore in Gui
- changed Whole Number to Integer in Data Blocks
- While loading a new project because of windows alert issues, cannot able to edit
- added 76800baud for esp32 and esp8266
- didn't update target and workspace if there is no device extension
- Adjust the project loading method and fix the problem of repeatedly loading targets
- adjust the params of installDeviceExtensions() to support call by gui
- Adjust the process of loading the project
- fix bug: After creating a new sprite, the device selection is cleared.
- fix bug: An error occurs when loading a project file that contains multiple device extensions.
- conversion name and typo fixed Commen -> Common
- Optimize server program, prepare data in advance to speed up service processing speed


## V4.1.0

**Bug Fixes**

- Because shield in ircbloq-resource source code is misspelled as sheild, shield filter in GUI interface is null.
- In VM, one more line of startheartbeat function call is written, and startheartbeat repeats reentry, resulting in real-time communication error.
- Cannot edit input-box after the alert or confirm window pops up.
- The device selection is not cleared after a new project is created.
- The old device is not disconnected after a new project is created.
- After using the shortcut key Ctrl + Z to modify blocks, the code on the right side is not updated.
- HC05 Bluetooth Tx and Rx interchanged
- add warp option for print in hc05 extension
- Bug fixes in Buzzer
- Fixed EOL for Print in Multi Serial Port

**Added**
- Added 8x8 Display Extension
- Added MPU6050 Extension
- Added SharpIR
- Added ArduinoSourceCode insert
- Added PCA9685- 16 Channel Servo Drive

## V4.0.4

- **New feature**

    1. Optimize the font and line break display effect of the serial terminal.
    2. Display the loaded extensions first in the extensions library.
    3. Modify the esp8266 upload rate to 921600 to speed up the upload speed.

- **Fix bug**

    1. When you double-click to open the project file with the selected device, an error will occur in loading.
    2. After add comment for device extension block and save the project file. If try to load the project after restart the software, there is another comment window appear which cannot able to delete.
    3. Fixed the bug loading error by double click project from saved location.
    4. When loading a project with a extension, an error will be reported and cannot be loaded.
    5. The input box of the variable increase block is parsed incorrectly when other blocks or variables are placed.
    6. In the double-numbered character, the movement blocks in the toolbox area will not automatically change to the coordinates of the character's current position.
    7. Fix the problem that esp32 and esp8266 cannot start after clicking the reset button when connecting to ircbloq due to the lack of serial port to enable dtr rts flow control.
    8. After connecting and disconnecting the device once in upload mode, no matter what mode is connected to the device again, it will not be able to establish communication with the connection firmata.
    9. ESP32 and ESP8266 will get stuck for a long time between compiling and uploading.

## V4.0.3

- **New feature**
    1. Add Kit filter option to device selection.
    2. Add the option to cancel the device selection.
    3. When loading a project containing unknown devices and plug-ins, the error details will be reported.
    4. Update the device picture according to the new picture standard.
    5. Automatically obtain the control board pin list in external extensions.
    6. Add slider type blocks.
    7. Extension can be auto sorted if enabled.

- **Fix bug**
    1. Fixed ESP Boards DTR/RTS Issues.
    2. The serial port send button is collapsed in small window mode.
    3. Modify the default installation path of the desktop version of windows to the root directory of C drive instead of the deep directory of user data.
    4. If there is an unsupported device id in the external device list, the device model will be empty.
    5. Because the vm building block adds the device type in front of the optype, the display variable cannot be translated normally.
    6. Esp8266 digital pin cannot select GPIO16.
    7. Check the checkbox so that the variable will be displayed in the stage area, and it will still exist after switching the device.
    8. Arduino ceil function name error.
    9. The microbit attitude option is not translated.
    10. Microbit uses multiple while true statements that are not supported.
    11. When using the scroll wheel to move the toolbox, the completely displayed blocks beyond the boundary are blocked again.
    12. Color picker function is not available.
    13. The disconnection error alert flashes after switching the mode.
    14. When using a third-party device, the alert uses the mother board instead of the picture of the third-party device board.

##V4.0.2
- **New feature
    1. IMPORVED NEW UI, Supports SCARTCH 3 Based Extensions.
    2. Added Blynk IOT, ADAFRUIT IO, LOCALSERVER, THINGSPEAK SERVER FOR NODEMCU boards
    3. Improved Some bug fix
    4. Added Serial communication Blocks in all Boards.

- **New feature**
    1. Add Kit filter option to device selection.
    2. Add the option to cancel the device selection.
    3. When loading a project containing unknown devices and plug-ins, the error details will be reported.
    4. Update the device picture according to the new picture standard.
    5. Automatically obtain the control board pin list in external extensions.
    6. Add slider type blocks.
    7. Optimized the devil bird svg image.

- **Fix bug**
    1. The serial port send button is collapsed in small window mode.
    2. Modify the default installation path of the desktop version of windows to the root directory of C drive instead of the deep directory of user data.
    3. If there is an unsupported device id in the external device list, the device model will be empty.
    4. Because the vm building block adds the device type in front of the optype, the display variable cannot be translated normally.
    5. Esp8266 digital pin cannot select GPIO16.
    6. Check the checkbox so that the variable will be displayed in the stage area, and it will still exist after switching the device.
    7. Arduino ceil function name error.
    8. The microbit attitude option is not translated.
    9. Microbit uses multiple while true statements that are not supported.
    10. When using the scroll wheel to move the toolbox, the completely displayed blocks beyond the boundary are blocked again.
    11. Color picker function is not available.
    12. The disconnection error alert flashes after switching the mode.
    13. When using a third-party device, the alert uses the mother board instead of the picture of the third-party device board.



- **New feature**
    1. Add esp8266 and makey makey support.
    2. Add a button to show all connectable device. Prevent users from being unable to connect to the device when using a USB-to-serial chip that is not included.
    3. Add file associations for .ib project file.

- **Fix bug**
    1. Severe freeze after switching targets several times.
    2. The remote resource update address configuration error caused the program to crash after clicking the Check Update button.
    3. The remote resource update address incorrectly uses ircbloqcc instead of the address in the configuration.
    4. When the blocks nested inside the blocks in the toolbox are in the workspace, the internal blocks are erroneously disabled when the disabled state is updated.
    5. An error is reported after opening multiple windows: the address is already in use.



- **New feature**
    1. Change arduino build tool from arduino-builder to arduino-cli.
    2. Add remote upgrade function for external extension and device.
    3. Modify the default sprite to Demon Bird.
    4. Add arduino esp32 board support.
    5. Add microbit V2 board support.
    6. Add clear cache button.
    7. Add install driver button.
    8. Move the real-time mode connection indicator to the stage head.
    9. Add localization for desktop alters.
    10. Add timeout error in upload modal. If it gets stuck for tens of seconds, it will show timeout error, allow users to click the close button but not stuck forever.
    11. Add arduino uno ultra base board to support customized board witch A6 A7 pins.
    12. Optimize the external extension and device framwork.
    13. Optimize the firmware files structure.
    14. Optimize the serialport framwork. Prevent interface freeze caused by receiving high-speed serialport data.
    15. Add QDP ROBOT C02 kit(arduino esp32).

- **Fix bug**
    1. Stuck at the upload modal if unplug the usb cable while in arduino build progress.
    2. Unplug the usb cable while in arduino upload progress, the gui does not disconnect the device. User could still click the upload button and then will stuck in upload modal.
    3. Uploading the program or firmware after connecting and disconnecting the device several times will cause the real-time mode communication bug.
    4. After the upload is successful, if user do not close the upload window, unplug the usb cable, it will display upload failure.



- **New feature**
    1. Add serilport console.
    2. Separate third party device from bundle pack. now support modify third party device without rebuild the project.
    3. Optimize the block's disable logic in different programming modes.
    4. Now in realtime mode, you can select the realtime mode extension.
    5. If a block is not connected into the effective tree. it's setup and define and others code will not generate.
    6. Optimize the structure of the code generated by Arduino code generator to make it more consistent with Arduino native code format.
    7. The project file will save the current programming mode and automatically switch to the saved mode after loading.
    8. In programming mode, blocks can no longer be click executed and glow.
    9. After the realtime mode communication is successfully established, there will be no atert. Instead, it will indicate whether the communication is successful by dimming the communication icon on the right side of the connection icon. A alter will pop up and prompt to download the real-time mode firmware only after the communication attempt fails.
    10. After the firmware is downloaded and the real-time communication is established successfully, the alert of real-time mode failure warning will automatically disappear.

- **Fix bug**
    1. When loading a project file with multiple large extensions, the toolbar area will repeatedly display the contents of multiple extensions, and some other errors.
    2. The button to download firmware is not disabled when there is no connected device.
    3. Shorten the window of upload to fix the problem of incomplete display on some pc.
    4. Fixed a number of potential problems with realtime mode communication.
    5. The code window is not re rendered after resizing, resulting in a missing display.
    6. After switching programming mode, the sprite will disappear in some times.
    7. Arduino and microbit do not hide all the unsupported building blocks in programming mode.
    8. Microbit's buttonIsPressed block transcoding function should have written n for b when button is B.
    9. Microbit custom variable name exception.
    10. Arduino UNO mega2560 serial port 0 translation code is incorrect.
    11. Number parsing error of data_changevariableby block.
    12. Cancel the 1.05x interface zoom setting and directly enlarge the font to fix the problem of blurred font in the toolbar menu.


- **New feature**
    1. Add hide code stage button.
    2. Change the ui of upload button.
    3. Change the description of some boards.
    4. Add a 1.05 scale to fix the problem of fuzzy font.
    5. Change project file extension from .sb3 to .ib.

- **Fix bug**
    1. Microbit generator error.
    2. The pin menu of arduino set digital out does not have analog pin items.



- **Fix bug**

	1. Third party's block which from vm code generator error.



- **New feature**

	1. Now most alert will automaticly disapear after 5s.
	2. Completed the blocks of microbit.
	3. Add a servo extension as demo for microbit.
	4. After installing the new version of the software, the old cache will be cleared automatically.


- **Fix bug**

	1. Error usb hardware id of cp2102.
	2. Error translation of microbit.
	3. Cannot scan to devices after loading a project.
	4. The loaded device extension still exists after switching the device selection.



- **New feature**

	1. Blocks could over flow the flyout boundary when mouse enter.
	2. Extension can be auto loaded when device selected.

- **New device/kit**

	1. microbit