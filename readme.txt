*****

How to use:(download link if the image and driver,en.kedei.net/raspberry/raspberry.html, copy to browser to open it)

*****
A. Quick way, use the compiled files we provide to burn directly to the sd card.

Note: You must use this command before you update the system sudo apt-mark hold raspberrypi-kernel (lock the kernel and the driver is not changed) sudo apt-mark hold raspberrypi-bootloader (lock resolution does not change)

*****

B. Using driver installation

	a. Use online installation (recommended)
		1. Burn the Raspberry Pi official latest desktop system
		2. Ensure that the network connection is normal.
		3. Connect the LCD screen to the Raspberry Pi development board correctly (right alignment)
		4. Open the terminal and enter the following command
			Sudo git clone https://github.com/kedei/LCD_driver
		5. Modify file permissions
			Sudo chmod -R 777 LCD_driver
		6. Enter the folder
			Cd LCD_driver
		7. Install the driver and then automatically restart
			Do not use FBCP driver
			Direct installation ./LCD35_show
			Rotate 90° ./LCD35_show 90
			Rotate 180° ./LCD35_show 180
			Rotate 270° ./LCD35_show 270
			Use fbcp driver (the Raspberry Pi motherboard must be networked):
			Install sudo ./LCD35_fbcp directly
			Rotate 90° sudo ./LCD35_fbcp 90
			Rotate 180° sudo ./LCD35_fbcp 180
			Rotate 270° sudo ./LCD35_fbcp 270

NOTE: The default virtual resolution of the Raspberry Pi is 480*320. Maybe your hdmi device does not support this resolution!

	b.Use the driver in the network disk

		1. Burn the Raspberry Pi official latest desktop system
		2. Ensure that the network connection is normal.
		3. Connect the LCD screen to the Raspberry Pi development board correctly (right alignment)
		4. Copy the network drive to the Raspberry Pi (use ssh or mount with U disk media)
		5. Unzip the file and start the installation.
			Modify permissions sudo chmod 777 LCD_driver.zip
			Extract the file sudo unzip LCD_driver.zip
			Modify file permissions sudo chmod -R 777 LCD_driver
		6. Enter the folder
			Cd LCD_driver
		7. Install the driver and then automatically restart
			Do not use FBCP driver
			Direct installation ./LCD35_show
			Rotate 90° ./LCD35_show 90
			Rotate 180° ./LCD35_show 180
			Rotate 270° ./LCD35_show 270
			Use fbcp driver (the Raspberry Pi motherboard must be networked):
			Install sudo ./LCD35_fbcp directly
			Rotate 90° sudo ./LCD35_fbcp 90
			Rotate 180° sudo ./LCD35_fbcp 180
			Rotate 270° sudo ./LCD35_fbcp 270
Note: You must use this command before you update the system. sudo apt-mark hold raspberrypi-bootloader (lock basic configuration does not change)
		

		Then use the command,
		Sudo apt-get update
		Sudo apt-get upgrade
		Sudo apt-get dist-upgrade (This command is not recommended for upgrades, updates are up to date, but may be unsafe）
Otherwise it may fail after rebooting
