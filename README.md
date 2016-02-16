# Kinect-Interaction
test for using Kinect for portal interaction and sending joint information to server via node.js

# Installation
Host machine that kinect connect to should be windows, the one that is going to receive and handle the sensor data in the Node.js application. Configureation step listed.

-Install official Kinect 2 SDK from [this page](https://www.microsoft.com/en-us/download/details.aspx?id=44561). Please also note that in order to install the SDK you will need a 64bit Windows 8 or higher.
-Next, you need [Node.js installed](https://nodejs.org/en/download/) in the Windows command line. If the installation was successful entering `node -v` into the command line will give you the version number of Node installed. You need at least version 0.11.3 for the Kinect 2 module to work. The installation will depend on node-gyp so install that too: `npm install -g node-gyp`.
-Install Microsoft Visual Studio, [free community version](https://www.visualstudio.com/en-us/visual-studio-homepage-vs.aspx) is sufficient. And if you have a 64-bit build then [the Windows 7 64-bit SDK](https://www.microsoft.com/en-us/download/details.aspx?id=8279). Yes, even if you are not on Windows 7.
-After that you can type `npm install kinect2` and the library will be installed to your machine.

# Reading skeleton data
Running output.js file from the project folder with node output.js will result in outputting the pure sensor data in a JSON format.

# output
When human detected, it shows joint information as follow:

{ bodyIndex: 0,
  tracked: true,
  trackingId: 72057594037929500,
  leftHandState: 1,
  rightHandState: 1,
  joints:
   [ { depthX: 0.34918805956840515,
       depthY: 0.7327612638473511,
       colorX: 0.39997994899749756,
       colorY: 0.7802628874778748,
       cameraX: -0.6315786838531494,
       cameraY: -0.8742918372154236,
       cameraZ: 3.137962818145752,
       orientationX: 0.18124830722808838,
       orientationY: 0.5968549251556396,
       orientationZ: 0.7218343019485474,
       orientationW: 0.29978057742118835 },
       ...
       {
       ...
       }
    ]
}

Otherwise kinect close after setted timeout.

# TODO
- Stream the skeleton data to server like cameras do.
- Can it be re-used for local representation?

