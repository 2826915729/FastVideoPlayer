# FastVideoPlayer
基于ijkplayer开发万能播放器，支持点播、直播播放。

![]()
![]()


# 如何引用
```
allprojects {
    repositories {
        ...
        maven { url 'https://jitpack.io' }
    }
}
```
```
dependencies {
        compile 'com.github.fanhua1994:FastVideoPlayer:1.0.1'
}
```

# demo演示
```
superPlayer = findViewById(R.id.super_player);
    play = findViewById(R.id.play);
    superPlayer.setLive(false);//是直播还是点播  false为点播
    superPlayer.setScaleType(FastVideoPlayer.SCALETYPE_FITXY);
    superPlayer.setTitle("TiDB宣传视频");//设置标题
    superPlayer.setUrl("https://download.pingcap.com/videos/pingcap-intro-converted.mp4");

    //封面图加载
    Glide.with(this).load("https://download.pingcap.com/images/video-poster.jpg").into(superPlayer.getCoverImage());

    play.setOnClickListener(new View.OnClickListener(){

        @Override
        public void onClick(View v) {
            superPlayer.play();
        }
    });
```
