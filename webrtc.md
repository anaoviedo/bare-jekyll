---
layout: page
title: webrtc

---

# Camera

<video height="300" id="localVideo"></video>
<div id="remotesVideos"></div>

# Library

<https://simplewebrtc.com/>

<script>
var webrtc = new SimpleWebRTC({
  // the id/element dom element that will hold "our" video
  localVideoEl: 'localVideo',
  // the id/element dom element that will hold remote videos
  remoteVideosEl: 'remotesVideos',
  // immediately ask for camera access
  autoRequestMedia: true
});
webrtc.on('readyToCall', function () {
  // you can name it anything
  webrtc.joinRoom('your awesome room name');
});
</script>
