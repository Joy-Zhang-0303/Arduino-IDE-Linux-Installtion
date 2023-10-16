# Arduino-IDE-Linux-Installtion
Here I note the process for installing Arduino-IDE on Linux Ubuntu and How to add the Desktop Icon

## Installtion Flow
1. Download the **Arduino IDE 2.2.1 ZIP file** for linux
https://www.arduino.cc/en/software
![Screenshot from 2023-10-16 13-38-26](https://github.com/Joy-Zhang-0303/Arduino-IDE-Linux-Installtion/assets/48177679/dcf39a1b-7cf2-4b4a-b590-7f9cf8ebb6b1)

2. Open the terminal to create the Arduino folder under ```/usr/local/``` and change the ownership
 ``` bash
 cd /usr/local/
 sudo mkdir arduino
 sudo chown your-PC-username:your-PC-username arduino/
 ```
3. Move the ZIP file and uncompress it into the **arduino** folder
``` bash
mv ~/Downloads/arduino-ide_2.2.1_Linux_64bit.zip ./
unzip ./arduino-ide_2.2.1_Linux_64bit.zip 
```

4. Create the Arduino-Icon Deskptop file
Place this file inside: ```.local/share/applications/``` folder in your home directory
This file should be called ```aduino.desktop```
Make sure the path for Exec and Icon is correct
``` desktop
[Desktop Entry]
Version=1.0
Name=Arduino IDE
Comment=Write code and flash to Arduino hardware
GenericName=Embedded electronics IDE
Keywords=Programming;Development
Exec=<path to arduino ide executable>
Terminal=false
X-MultipleArgs=false
Type=Application
Icon=<path to arduino icon>
Categories=GNOME;GTK;Development;Programming;
MimeType=text/x-arduino;
StartupNotify=true
```

One Desktop  Example file 
``` desktop
[Desktop Entry]
Version=2.2.1
Name=Arduino IDE
Comment=Write code and flash to Arduino hardware
GenericName=Embedded electronics IDE
Keywords=Programming;Development
Exec=/usr/local/arduino/arduino-ide_2.2.1_Linux_64bit/arduino-ide
Terminal=false
X-MultipleArgs=false
Type=Application
Icon=/usr/local/arduino/arduino-ide_2.2.1_Linux_64bit/resources/app/resources/icons/512x512.png
Categories=GNOME;GTK;Development;Programming;
MimeType=text/x-arduino;
StartupNotify=true
```

5. Make the desktop file usable
Open the folder ```/home/yuminaka-lab/.local/share/applications/```,
Right Click the arduino.desktop file,
Select the ```Properties```, and go into the permissions tab,
Check the Execute to enable ``` Allow executing file as program```, like the picture below:

![image](https://github.com/Joy-Zhang-0303/Arduino-IDE-Linux-Installtion/assets/48177679/52e07584-b87f-4a44-a779-4e3e1fcdfda1)

6. Double left-click the arduino icon and enjoy it!

## After the above operation, you can find the arduino icon esisting in your app dock, you can alao right click the icon to add it as your favorate one.
![Screenshot from 2023-10-16 13-35-15](https://github.com/Joy-Zhang-0303/Arduino-IDE-Linux-Installtion/assets/48177679/a6e8cb0a-af0e-4409-a67b-869f5ca0dcb2)



