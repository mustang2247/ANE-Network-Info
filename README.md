Air Native Extension for testing network connection (iOS + Android)
======================================

This is an [Air native extension](http://www.adobe.com/devnet/air/native-extensions-for-air.html) to if the current device has an active connection. It has been developed by [FreshPlanet](http://freshplanet.com) and is used in the game [SongPop](http://songpop.fm).


Installation
---------

The ANE binary (AirNetworkInfo.ane) is located in the *bin* folder. You should add it to your application project's Build Path and make sure to package it with your app (more information [here](http://help.adobe.com/en_US/air/build/WS597e5dadb9cc1e0253f7d2fc1311b491071-8000.html)).


On Android:

* you need to enable the following permissions (otherwise the returned state will always be not connected):

    ```xml
    <android>
        <manifestAdditions><![CDATA[
            <manifest android:installLocation="auto">
                
                ...

                <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE"/>
                <uses-permission android:name="android.permission.ACCESS_WIFI_STATE"/>
                
                ...

            </manifest>
        ]]></manifestAdditions>
    </android>
    ```


Usage
---------

Call the function *AirNetworkInfo.networkInfo.isConnected()* to check the current network status of the device.

Notes:
* included binary has been compiled for 64-bit iOS support

Build script
---------

Should you need to edit the extension source code and/or recompile it, you will find an ant build script (build.xml) in the *build* folder:

    cd /path/to/the/ane/build
    mv example.build.config build.config
    #edit the build.config file to provide your machine-specific paths
    ant


Authors
------

This ANE has been written by [Thibaut Crenn](https://github.com/titi-us). It belongs to [FreshPlanet Inc.](http://freshplanet.com) and is distributed under the [Apache Licence, version 2.0](http://www.apache.org/licenses/LICENSE-2.0).


Join the FreshPlanet team - GAME DEVELOPMENT in NYC
------

We are expanding our mobile engineering teams.

FreshPlanet is a NYC based mobile game development firm and we are looking for senior engineers to lead the development initiatives for one or more of our games/apps. We work in small teams (6-9) who have total product control.  These teams consist of mobile engineers, UI/UX designers and product experts.


Please contact Tom Cassidy (tcassidy@freshplanet.com) or apply at http://freshplanet.com/jobs/
