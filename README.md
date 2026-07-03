# OsirisEdit

The modified wavetable and bank editor for the Osiris Eurorack synthesizer modules.

### Fork Info

Modbap created a browser/js version of the editor to replace their fork of WaveEdit which was only built for Mac/Linux.  It works, but I prefer the GUI of the original version.  And I like having the EXE file just on my PC rather than the whole browser/js stack.  They had a work-in-progress Windows verison but I couldn't get it to compile as it was.  I forked that, updated some libraries, and did some tweaking until I got it to compile and work.  Really, 99% of the effort was AndrewBelt/switchupcb/Modbap.  But this does now compile and run successfully on Windows.  I am including a build in a zip file so you don't have to compile it yourself, but the code is here if you want to.  

### Building

- Install MingW64.
- Clone this repo.
- There are a bunch of packages you will need to install, but unfortunately I didn't track it closely (sorry).  It won't be hard to figure out as when you compile it, it will pretty clearly tell you what it can't find.
- I rolled all the external dependencies from the original project into the dep folder, rather than just having them external.  Now they are locked in time, forever, and you won't have to hunt the missing ones down like I did.
- SDL was fully updated to SDL2.  It seemed Modbap (or maybe the original author of WaveEdit) had partially migrated to SDL2, but it was incomplete and caused a lot of errors.  Hopefully the fixes I put it are complete.
- Run the following command to build:
	-	mingw32-make ARCH=win -j1 VERBOSE=1
- Copy all the updated files to the bin folder.  I tried to pile all the dependent DLLs together to make it easy to run.
