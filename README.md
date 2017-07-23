# Videos in OpenLayers 3.x and above

Example on how to use videos in OpenLayers 3.x and above. This example uses _OpenLayers 4.2.0_.

This examples adds a video in format _mp4_ and _webm_ to a OpenLayers layer, then you can control it just like a normal OL layer. Also adds video controls and a custom legend to the map.

This example was initially based on the _postcompose_ hook example by @tschaub, see [http://tschaub.net/ol3-video/examples/video.html](http://tschaub.net/ol3-video/examples/video.html).

This example can be applied to weather forecast, satellite data and many other usages.

## Running the App

Just check the index.html for details.

A live example in :

[__https://htmlpreview.github.io/?https://github.com/lcalisto/ol_videos/blob/master/index.html__](https://htmlpreview.github.io/?https://github.com/lcalisto/ol_videos/blob/master/index.html)

### Notes

The main function is:
```
showAnimLayer('example.mp4', 'example.webm', bbox, map, framerate, showSeconds, opacity, legend)
```

For browser compatibility both __mp4__ and __webm__ videos can be added. You need to provide at least one video (mp4 or webm).

__bbox__ (_required_) is the bounding box array. 

__map__ (_required_) The map where the video is going to be displayed.

__framerate__ (_optional_) is the framerate of the movie, if __none__ or __null__ is provided, then the default value is 1.

__showSeconds__ (_optional_) Allows the user to limit the video seconds. For example, if the video has 60 seconds in total and you provide __showSeconds=30__ then only the initial 30 seconds will be displayed, after 30 seconds the video will start from the beginning. If __none__ , __null__ or __'all'__ is provided, then the full video will be displayed.

__opacity__ (_optional_) Allows the user to specify the video opacity. If __none__ or __null__ is provided, then the default value is 0.5 (50%).

__legend__ (_optional_) The legend must be a JSON object with at least the same number of elements as the number of displayed frames. You can customize the number of displayed frames with __showSeconds__ variable.

### To remove the video

Function __removeAnimLayer(map)__ removes the loaded video, where __map__ variable is the map where the video is loaded:
```
removeAnimLayer(map);
```
