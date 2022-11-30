# RainMachine2
Indigo plugin for Rain Machine

Rain Machine Plugin has been developed for Indigo Home Automation version 2022.1 and hopefully beyond. It uses python3

Installation Instructions:
Download the plugin zip file from github
It requires a working python3 installation and the ability to install a new library to enable the plugin.
Open a terminal window (Applications -> Utilities -> Terminal app
type "pip3 install regenmaschine"
type "pip3 freeze | grep regenmaschine" and confirm that 2022.11.2 or greater is installed
Quit Terminal
Unzip plugin and install the plugin by double clicking and allowing it to be installed and enabled in indigo
Create a new indigo device of type RainMachine2 from the new device menu 
At top of dialog box after selecting device type, select "Model - HD12" (even if you have HD16 - I don't have either the Mini or Pro models, but this should work on them as well. It may not work on first generation devices or ones that have not had their firmware updated so it is using API 4.6.1 which is needed for the flowmeter. You can check the API version by going to the RainMachine web interface and looking in the "About" section)

On popup dialog choose either local or cloud login.
On local machine you login with the IP address of the RainMachine device (you should be able to get this from the rainmachine itself under "About" or lookup on your router) and the device password
On a cloud device you need to have set up an account with RainMachine company and use your email and password for your https://my.rainmachine.com/login?redirect_uri=/devices account
I do not have a rainmachine cloud account and will not be maintaining this if the company changes their login. Would suggest using local access as best idea
Do not change port unless you have RainMachine running on a different port
Enter password and hit login
If successful, you should see a list of RainMachine devices to chose from
Once selected hit save.

You can create either triggers or schedules to start a program, stop a program, start a zone, stop a zone or stop all watering
Ceate a new trigger/schedule with whatever constraints you want for it to run.
Under the third tab "Actions", select "Device Actions", select RainMachine2 Controls
In the popup, select the rainmachine device you want to conrtol
Select the program or zone you want to control, for zone start there is a duration, for programs it runs the program as it exists on the rainmachine device
In the details, if you have a flowmeter installed and enabled, it will count the watering and leak clicks and report a combined gallons.
To setup the flow meter you need to use the web interface of the local rainmachine or the cloud based one to enable and set clicks per gallon.

Please don't ask for further features to setup the rainmachine device, change names of zones, list the prior watering, etc. This is aldeardy well implemented in the webapp, phone app and on the machine itself. This plugin is just designed to allow you to trigger/schedule starting and stoping of programs and zones from Indigo. If you want more info, go to the device or login to the web interface of the device.



