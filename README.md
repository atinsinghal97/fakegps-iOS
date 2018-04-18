# fakegps

fakegps can be used to spoof location of iOS devices when connected to Xcode.
fakegps has been tested on iOS 10 and iOS 11.
This can be useful for apps which need you to be at a particular location to access or unlock some features or for any other similar things.

This method works with all the apps simultaneously as the location data for the entire device is spoofed.

<b>To spoof the location, do the following:</b>

1. Clone/Download the given repo to your PC.
2. Open the 'fakegps.xcodeproj' file.
3. Change the bundle identifier as per your choice and sign the app by assigning a team.
4. Using the Navigator, open 'fakegps.gpx' file and update the values in Line 9, 10 and 19 <br>
   i. Enter the latitude and longitude of the location you want to spoof to in Line 9 <br>
      &ensp; eg: <i> &lt;wpt lat="28.637323" lon="77.327680"> </i> <br>
   ii. Enter a name to identify the location in Line 10 <br>
      &ensp; eg: <i> &lt;name>Radisson Blu Kaushambi Delhi NCR&lt;/name> </i> <br>
   iii. Update the time and date to a few mintes past the current time as the location would be spoofed at the mentioned time.<br>
      &ensp; Make these changes in Line 19.<br>
      &ensp; eg: <i> &lt;time>2017-10-15T16:12:00Z&lt;/time> </i> <br>
5. Run the app on your iOS device via Xcode.
  
  <b>Note#</b> If this is your first app installed on the iOS device with that Developer Certificate, you will need to Trust the    Profile by going to Settings> General> Device Management> Select your Developer Profile> Trust> Trust.
  
9. In Xcode menu, select Debug> Simulate Location> fakegps.  
10. Now at the time mentioned in 'fakegps.gpx' file, the location would be spoofed.
  
  
Even if you disconnect the device from your Mac, the location would remain spoofed.

To remove Location spoofing immediately, restart your device after quitting the fakegps app.

If you want to add this to your own project, download the 'fakegps.gpx' file from the repo and add it to your own Xcode Project and follow the above steps to spoof the location. The 'fakegps.gpx' file can be found in fakegps-iOS/fakegps/
