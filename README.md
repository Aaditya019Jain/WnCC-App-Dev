# Installation-and-setup-of-Flutter

# Flutter
* Flutter is an open-source UI framework developed by Google that allows developers to create cross-platform applications for mobile, web, and desktop platforms using a single codebase. Traditionally, developing applications for different platforms required separate teams of developers using different programming languages and frameworks, resulting in increased development time and maintenance costs. Flutter addresses these challenges by enabling developers to write code once and deploy it on multiple platforms. With Flutter, developers can build visually stunning, high-performance applications that can run on iOS, Android, web browsers, and even desktop platforms like Windows, macOS, and Linux.

### Installation of flutter in Windows:
* follow the upcoming tutorial to install flutter: [Install Flutter](https://www.youtube.com/watch?v=BqHOtlh3Dd4)
* Those who prefer documentation over video can visit: [Flutter install Documentation](https://docs.flutter.dev/get-started/install)

### Testing of App:
* While programming an App, we will have to run our app multiple times to see its current status. 

  
* Running flutter on real device: Real devices provide an accurate representation of how your application will behave in the hands of real users.Real device testing allows you to assess the performance of your app in real-world scenarios.For this we can connect our phone to the programming device through USB cable. Here's a short tutorial for this:
* [Run flutter app on real device](https://www.youtube.com/watch?v=v01ISnOIbL8)
* (Alternative) Emulator: Emulators are virtual devices that mimic the behavior of real devices. They provide a simulated environment to test and debug your Flutter application. If someone prefers app emulator over real device, here's a tutorial explaining steps to be followed:
*  [Android Virtual Device for Flutter](https://www.youtube.com/watch?v=tB1sjfijupU)

*It needs to be noted that running an application in flutter may take time for the first time in both real device and virtal device (emulator).

#Setup for MAC OS

The actual code to change the path permanently
 export PATH="$PATH:$(pwd)/flutter/bin"

Step wise method to set up flutter in your MAC OS:-

Refer to the website [official website for fliutter installation](https://docs.flutter.dev/get-started/install/macos#android-setup)
This will setup the required environment needed for you to set up flutter in your mac.

Another thing to refer is the video [youtube video to setup flutter on MAC OS](https://www.youtube.com/watch?v=fEfMYAAeHmY)

Coming on the steps to set up flutter:-
Use the command to set up the environment on your mac os “sudo softwareupdate --install-rosetta --agree-to-license”


Download the package according to the core of your mac book from the website mentioned above.

Now set a path where you will keep the downloaded file (later will be mentioned as the SDK file). The commands in the tutorial may include the path that is a folder present in the downloads section.

Use the below commands to go to the required directories 
cd ~/development
unzip ~/Downloads/flutter_macos_3.10.5-stable.zip

Right now if you type the flutter commands on any given window of your terminal it  
won't recognize them so to solve this we need to permanently change its path.for this 
Try to open a file with the command “open ~/.zshrc”
If the file doesn't exists then create one with the command “touch ~/.zshrc”
Add the lines “export ANDROID_HOME=/Users/(username)/Library/Android/sdk
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/platform-tools
export PATH="$PATH:/Users/(username)/Downloads/development/flutter/bin"in the file

After this you need some softwares downloaded in your mac which include 
VS Code 
X Code
Android Studio (download each form their respective official sites)

Now run a command “flutter doctor” on your terminal and check on what all points you  
receive a red cross. (The ways to solve each cross will be discussed later.)

Open VS Code and download the extensions flutter and dart.

														
On android studio install the flutter and dart plugins. The rest of the settings on X code 
and Android studio code are to be done according to the above mentioned video.
Make sure you download the files in the correct directory and install the packages that 
you require for your app.

Coming on how to correct individual crosses:-

For the flutter channel cross use the commands “flutter channel stable” and then “flutter upgrade”. Also make sure that your SDK file is in the correct directory.

For the android tool chain, run the following command flutter config --android-sdk "/Users/username/Library/Android/sdk" . after this it will ask you to restart your editor. Just run the “flutter doctor” command again and then to accept all the required permissions run the command “flutter doctor --android-licenses”. Now type y to accept every permission.

For the x code error just install the x code application properly and make the required changes in the applications settings from the above video. The reference website being https://docs.flutter.dev/get-started/install/macos#android-setup the xcode install section.
Use the following commands “sudo xcode-select --switch /Applications/Xcode.app/Contents/Developer” and 
“sudo xcodebuild -runFirstLaunch”

To open your simulator use the command “open -a Simulator”.

The same x code error will ask you to download cocoa pods to set up the complete environment. Run the command “sudo gem uninstall ffi && sudo gem install ffi -- --enable-libffi-alloc” after this enter the password of your mac and let it run. Use y to allow uninstallation.

Now use the command “sudo gem install cocoapods” and if it shows a similar error use the following commands “gem install activesupport -v 6.1.7.3” and then “sudo gem install cocoapods”. If it asks for write permissions use the command “sudo gem install activesupport -v 6.1.7.3 “.

Run “flutter doctor” command again and check if everything is resolved or not. For more problems you can contact us individually.
For the android studio errors you mainly need to install the command line. The link to the command lines is commandlinetools-mac-9477386_latest.zip.

Now open VS Code and use the command palette to start a new flutter project and once it opens its main.dart, change the device used for display to be the ios simulator. Now run the code. If the code shows some error simply type “flutter run” command on the terminal.

Rest all the issues will be taken up separately

The program can also be run through the Android Studio app.


