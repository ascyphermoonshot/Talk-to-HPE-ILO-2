# Talk-to-HPE-ILO-2

## BLUF: ILO2 is obsolete but you can still use it if you update the firmware as much as possible.

### Things you will need:
+ Something running Windows (either a Windows machine or a VM will work)
+ The oldest firefox possible (available in this repo as a portable program)
+ HP ILO2 firmware (available in this repo)
+ monitor and keyboard (only if you dont have an ILO2 user and password)
+ HP ILO2 license key (optional)
+ Termux (optional)
+ PuTTY (optional)

### Getting an user and password (only if you dont have one)
1. With the monitor and keyboard connected turn on the server and press F8 during post (the server will tell you when).
2. Go to `User` and add a new user and password, grant all permissions.
3. Go to `Network` and write down the IP address
4. Save and close all

### Opening ILO2
1. In a Windows machine open the portable Firefox and go to the IP Address you wrote down.
2. Log in with your username and password (the default user is Administrator, the default password is written on a sticker somewhere in your server).
3. It will give you a security error, accept it

### updating the ILO2 firmware
1. Go to the last tab and go to `Firmware Update`
2. Upload your new firmware and run the update
3. If you have an ILO2 Advanced license key add it now

## Talking to ILO2 from Linux (or Mozilla Firefox on Windows)

### Enabling legacy options
> [!WARNING]
> This will downgrade your browser security **CONSIDER YOUR ACTIONS**
1. Go to `about:config`
2. Set `security.tls.version.enable-deprecated` to `true`
3. Set `security.tls.version.min` to `1`
4. Go to the the IP Address you wrote down.
5. Log in with your username and password (the default user is Administrator, the default password is written on a sticker somewhere in your server).
6. Open the page despite the warnings
> [!NOTE]
> The virtual console will not work, that`s normal.

##Talking to ILO through SSH 
