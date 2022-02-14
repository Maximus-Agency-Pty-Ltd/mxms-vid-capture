# MXMS Vid Capture

Important note: this video capture is 'always on' for the flash.

## Usage

```javascript
  window.plugins.videocaptureplus.captureVideo(
      captureSuccess, // your success callback
      captureError,   // your error callback
      {
        limit: 1, // the nr of videos to record, default 1 (on iOS always 1)
        duration: duration, // max duration in seconds, default 0, which is 'forever'
        highquality: highquality, // set to true to override the default low quality setting
        frontcamera: frontcamera, // set to true to override the default backfacing camera setting. iOS: works fine, Android: YMMV (#18)
        // you'll want to sniff the useragent/device and pass the best overlay based on that.. assuming iphone here
        portraitOverlay: 'www/img/cameraoverlays/overlay-iPhone-portrait.png', // put the png in your www folder
        landscapeOverlay: 'www/img/cameraoverlays/overlay-iPhone-landscape.png', // not passing an overlay means no image is shown for the landscape orientation
        overlayText: 'Please rotate to landscape for the best result' // iOS only
      }
  );
```
