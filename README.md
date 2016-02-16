# Kinect-Interaction
test for using Kinect for portal interaction and sending joint information to server via node.js

# Installation
Host machine that kinect connect to should be windows, the one that is going to receive and handle the sensor data in the Node.js application. Configureation step listed.

- Install official Kinect 2 SDK from [this page](https://www.microsoft.com/en-us/download/details.aspx?id=44561). Please also note that in order to install the SDK you will need a 64bit Windows 8 or higher.
- Next, you need [Node.js installed](https://nodejs.org/en/download/) in the Windows command line. If the installation was successful entering `node -v` into the command line will give you the version number of Node installed. You need at least version 0.11.3 for the Kinect 2 module to work. The installation will depend on node-gyp so install that too: `npm install -g node-gyp`.
- Install Microsoft Visual Studio, [free community version](https://www.visualstudio.com/en-us/visual-studio-homepage-vs.aspx) is sufficient. And if you have a 64-bit build then [the Windows 7 64-bit SDK](https://www.microsoft.com/en-us/download/details.aspx?id=8279). Yes, even if you are not on Windows 7.
- After that you can type `npm install kinect2` and the library will be installed to your machine.

# Reading skeleton data
Running output.js file from the project folder with `node output.js` will result in outputting the pure sensor data in a JSON format.

# Output
When human detected, it shows joint information as follow:

![alt tag](http://www.webondevices.com/wp-content/uploads/2015/09/data.png)

Otherwise kinect close after setted timeout.

# TODO
- Stream the skeleton data to server like cameras do.
- Can it be re-used for local representation?

# Useful Links
[Kinect SDK for web applications](https://msdn.microsoft.com/en-us/library/dn435664.aspx)
[Kinect Unity support, does not work on v2?](http://wiki.etc.cmu.edu/unity3d/index.php/Microsoft_Kinect_-_Microsoft_SDK)
[Microsoft Kinect general tools and resources](https://dev.windows.com/en-us/kinect/tools)
