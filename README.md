# Videos in OpenLayers 3.x and above

Example on how to use videos in OpenLayers 3.x and above. This example uses _OpenLayers 4.2.0_.

This examples adds a video in format _mp4_ and _webm_ to a OpenLayers layer. Also this adds video controls and a custom legend to the map.

This usage can be important for weather forecast, satellite data and many other usages.

## Running the App

Just check the index.html for details.

### Notes

The main function is:
```
showAnimLayer('example.mp4', 'example.webm', bbox, framerate, showSeconds, opacity, legend, map);
```

For browser compatibility both __mp4__ and __webm__ videos can be added. You need to provide at least one video (mp4 or webm).

__bbox__ (_required_) is the bonding box array. 

__map__ (_required_) The map were the video is going to be displayed.

__framerate__ (_optional_) is the framerate of the movie, if __none__ or __null__ is provided then the default value is 1.

__showSeconds__ (_optional_) Allows the user to only limit the video. For example if the video as 60 seconds in total and you provide __showSeconds=30__ then only the initial 30 seconds will be displayed, after 30 seconds the video will start from the beginning. If __none__ , __null__ or __'all'__ is provided then the full video will be displayed.


__opacity__ (_optional_) Allows the user to specify the video opacity. If __none__ or __null__ is provided then the default value is 0.5 (50%).

__legend__ (_optional_) The legend must be a JSON object with at least same number of elements as the number of displayed frames. You can customize the number of displayed frames with __showSeconds__ variable.


Function __removeAnimLayer(map)__ removes the loaded video, where __map__ variable is the map were the video is loaded.
```
removeAnimLayer(map);
```
