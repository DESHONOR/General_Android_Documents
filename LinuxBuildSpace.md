#### General how to get started developing android roms in linux, mainly intended for ubuntu and ubuntu based distros.

First thing you need to do is ditch openJRE/JDK and install sun java 6, open up your terminal and paste:  
`sudo apt-get purge openjdk-\* icedtea-\* icedtea6-\*`  

This will remove openJRE/JDK, now let's add the webupd8 java ppa  
`sudo add-apt-repository ppa:webupd8team/java`  
`sudo apt-get update`  
`sudo apt-get install oracle-java6-installer oracle-java7-set-default`  

Verify java version with:  
`java --version`  


Next, let's get the sdk from http://developer.android.com/sdk/index.html, once it's done cd in to the tools folder and excecute ./android via terminal to update.  Make sure you get platform-tools which includes adb and fastboot.  

Now let's edit the .bashrc to include the appropriate paths, open .bashrc in your favorite editor and include these lines:  
>#Android PATH
>export PATH=$PATH:~/android/sdk
>export PATH=$PATH:~/android/sdk/platform-tools
>export PATH=$PATH:~/android/sdk/tools
