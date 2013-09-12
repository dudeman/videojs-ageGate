videojs-ageGate
===============

presents an age gate that users must pass before videos are playable.

## USAGE:

```html
<video id="video" src="movie.mp4" controls></video>
<script src="video.js"></script>
<script src="videojs-ageGate.js"></script>
<link href="videojs-ageGate.css" rel="stylesheet">
<script>
  var player = videojs('video');
  var minimumDate = new Date();
  minimumDate.setFullYear(minimumDate.getFullYear() - 18);

  player.ageGate({
    minDate: minimumDate,
    promptMessage: 'Please enter your birth date',
    deniedMessage: 'Sorry, the content creator has limited views of this video to people aged 18 and older'
  });

</script>
