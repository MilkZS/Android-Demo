
```
/**
 * Initialize ExoPlayer.
 * @param mediaUri The URI of the sample to play.
 */
 private void initializePlayer(Uri mediaUri) {
    if (mExoPlayer == null) {

        // Create an instance of the ExoPlayer.
        TrackSelector trackSelector = new DefaultTrackSelector();
        LoadControl loadControl = new DefaultLoadControl();
        mExoPlayer = ExoPlayerFactory.newSimpleInstance(this, trackSelector, loadControl);
        mPlayerView.setPlayer(mExoPlayer);

        // Set the ExoPlayer.EventListener to this activity.
        mExoPlayer.addListener(this);
    
        // Prepare the MediaSource.
        String userAgent = Util.getUserAgent(this, "ClassicalMusicQuiz");
        MediaSource mediaSource = new ExtractorMediaSource(mediaUri, new DefaultDataSourceFactory(
                this, userAgent), new DefaultExtractorsFactory(), null, null);
        mExoPlayer.prepare(mediaSource);
        mExoPlayer.setPlayWhenReady(true);
    }
 }
```

