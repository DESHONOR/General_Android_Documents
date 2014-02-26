#### General how to get started developing android roms in linux, mainly intended for ubuntu and ubuntu based distros.

First thing you need to do is ditch openJRE/JDK and install sun java 6, open up your terminal and paste:  
`sudo apt-get purge openjdk-\* icedtea-\* icedtea6-\*`  

This will remove openJRE/JDK, now let's add the webupd8 java ppa  
`sudo add-apt-repository ppa:webupd8team/java`  
`sudo apt-get update`  
`sudo apt-get install oracle-java6-installer oracle-java6-set-default`  

Verify java version with:  
`java --version`  


Next, let's get the sdk from http://developer.android.com/sdk/index.html, once it's done cd in to the tools folder and excecute ./android via terminal to update.  Make sure you get platform-tools which includes adb and fastboot.  

Now let's edit the .bashrc to include the appropriate paths, open .bashrc in your favorite editor and include these lines: 
```
#Android PATH
export PATH=$PATH:~/android/sdk  
export PATH=$PATH:~/android/sdk/platform-tools  
export PATH=$PATH:~/android/sdk/tools  
```  

Be sure to change ~/android with your actual path (the folder you extracted the sdk to) and save and exit, after that we need to update the file by issueing the command `source ~/.bashrc`  

#### Libs and files we need to build
Open your terminal again and copy and paste this to get the required libs and files:  

```
sudo apt-get install git gnupg flex bison gperf build-essential \
  zip curl libc6-dev libncurses5-dev:i386 x11proto-core-dev \
  libx11-dev:i386 libreadline6-dev:i386 libgl1-mesa-glx:i386 \
  libgl1-mesa-dev g++-multilib mingw32 tofrodos \
  python-markdown libxml2-utils xsltproc zlib1g-dev:i386
```
And then:  
`sudo ln -s /usr/lib/i386-linux-gnu/mesa/libGL.so.1 /usr/lib/i386-linux-gnu/libGL.so`

Congragulations, you are ready to roll.

