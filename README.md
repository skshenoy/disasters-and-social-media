# Client Project: Leveraging Social Media to Map Disasters
DSI 9 ATX - Shreya, Michelle, Ben

## Executive Summary
In emergencies, information is the most critical resource. Social media allows for near-instantaneous sharing of information, but it is difficult to find relevant posts quickly when dealing with a time-sensitive issue like a disaster. Our solution aims to join relevant tweets with a dashboard that monitors the details of the disaster itself. Many tweets contain embedded images or video that have pertinent information, including landmarks and visual indicators of location (highway exits, street signs, etc.). By targeting tweets that may have rich location information embedded in them in these ways, we manage to sidestep the issue of most tweets not having geolocation enabled. Tracking in near real-time, our dashboard/web app provides that disaster-specific image and video content for a human to review. This can help emergency coordinators identify at-risk areas, locate people in need of help, and analyze the intensity and extent of damage.

For this project, we decided to focus on the California fires.

### Data Dictionary

The Twitter data was gathered by using the Tweepy package to access the Twitter API. The tweet information that was kept:

|Feature|Type|Dataset|Description|
|---|---|---|---|
|fire|string|Twitter API pulls|Name of the fire the tweet is associated with; needed to interface correctly with the dashboard.| 
|full_text|string|Twitter API pulls|Full text of the tweet (up to 240 characters).| 
|media_link|string|Twitter API pulls|Direct link to the first piece of embedded media in the tweet if present, otherwise none.|
|place|string|Twitter API pulls|The provided location if the tweet had location services enabled, otherwise none.|
|created_at|datetime.datetime|Twitter API pulls|Timestamp of when the tweet was posted.| 

On top of this, data in the form of shape files were pulled from the Cal Fire server for wildfire boundaries and evacuation boundaries. This data was used in the dashboard to accurately map the wildfires themselves, zones of evacuation, relief shelters, and so on.

### Conclusions

[See the fully-functional demo here.](https://benjaminmetcalfe.maps.arcgis.com/apps/webappviewer/index.html?id=ad0525f04ff5484d88ecf6a18eb8a8cc)
