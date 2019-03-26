# cocos2d-x_v3.17.1_UWP_Templates
Fixed project files so UWP templates are added and built 

Warning: WinRT hasn't been officially supported since 3.15.1 so some newer functions added since will not for UWP apps, ex: glview->setCursor("custom-cursor.png").  You need to figure a way to do that for WinRT using custom win32 cursors. See my post here: https://discuss.cocos2d-x.org/t/hidden-mouse-inputs-and-custom-cursors/45879

To build for XBox / UWP

1) Copy these folders into your Cocos2d 3.17.1 directory
2) Create new game with the usual command: cocos new MyGame -p com.your_company.mygame -l cpp
3) Retarget solution min version 10.0.16299, max 10.0.17763, and set your game's project as startup target.
4) To build for xbox, make sure Xbox is in dev mode, registered in developer program, and test account is logged in
5) Right click your game's project file -> properties, Configuration Properties->Debugging.  Make sure "Debugger to launch" is set to "Remote Machine"
6) enter the XBox's IP address for the Machine name.
7) Instead of building for "local Machine", build for "remote machine". Select either Debug or Release, x64 and it should push it to the Xbox
