[![Build Status](https://travis-ci.org/hex-firebone/YouTube-Downloader.svg?branch=master)](https://travis-ci.org/hex-firebone/YouTube-Downloader)

# YouTube Downloader

This project was inspired by a very popular [youtube-dl](https://github.com/rg3/youtube-dl) python package:

Yes, there are multiple PHP-based youtube downloaders on the Internet, but all of them haven't been updated in years or they depend on youtube-dl.

This script does not depend on anything other than cURL. No Javascript interpreters, no calls to shell... nothing but pure PHP.

## Installation

Recommended way of installing this is via [Composer](http://getcomposer.org/):

```
composer require firebone/youtube-downloader
```

## Usage

```php
$yt = new YTDownloader();

$links = $yt->getDownloadLinks("ffxKSjUwKdU");

print_r($links);
```

### Result 

```
Array

(

    [0] => Array

        (

            [url] => https://redirector.googlevideo.com/videoplayback?id=o-APhcxffiY6sr5fgEyc6ITssfWGyKfYa6_4KUfmWe2jYL&sparams=dur%2Cei%2Cid%2Cip%2Cipbits%2Citag%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Cratebypass%2Crequiressl%2Csource%2Cexpire&lmt=1524198756368804&ei=BCRDW_ijCdLygAeWkJGADA&ipbits=0&ip=185.176.40.135&mime=video%2Fmp4&itag=22&key=yt6&fexp=23709359&ms=au%2Crdu&mt=1531126644&fvip=2&mv=u&requiressl=yes&dur=238.213&pl=24&ratebypass=yes&expire=1531148388&c=WEB&source=youtube&mm=31%2C29&mn=sn-uxaxiv0nxx5q-nv4l%2Csn-nv47lney&signature=4D7B0561F48AB1B65B2ECEE807E8335F1473A420.0280F197CE092877CF78A73FAE464DDC0574C9D6&title=Ariana-Grande-no-tears-left-to-cry

            [itag] => 22

            [type] => HD MP4[1280x720]

        )

    [1] => Array

        (

            [url] => https://redirector.googlevideo.com/videoplayback?id=o-APhcxffiY6sr5fgEyc6ITssfWGyKfYa6_4KUfmWe2jYL&sparams=clen%2Cdur%2Cei%2Cgir%2Cid%2Cip%2Cipbits%2Citag%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Cratebypass%2Crequiressl%2Csource%2Cexpire&ei=BCRDW_ijCdLygAeWkJGADA&ip=185.176.40.135&fexp=23709359&ms=au%2Crdu&mt=1531126644&mv=u&dur=0.000&ratebypass=yes&c=WEB&source=youtube&clen=24489177&mn=sn-uxaxiv0nxx5q-nv4l%2Csn-nv47lney&lmt=1524199428883596&ipbits=0&mime=video%2Fwebm&itag=43&key=yt6&mm=31%2C29&fvip=2&requiressl=yes&pl=24&expire=1531148388&gir=yes&signature=AD118809D71095D33D1489E856B6EACA5280209C.419939B86C5BA1EC1874F2C64CF02F702DC0551D&title=Ariana-Grande-no-tears-left-to-cry

            [itag] => 43

            [type] => WEBM[640x360]

        )

    [2] => Array

        (

            [url] => https://redirector.googlevideo.com/videoplayback?id=o-APhcxffiY6sr5fgEyc6ITssfWGyKfYa6_4KUfmWe2jYL&sparams=clen%2Cdur%2Cei%2Cgir%2Cid%2Cip%2Cipbits%2Citag%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Cratebypass%2Crequiressl%2Csource%2Cexpire&ei=BCRDW_ijCdLygAeWkJGADA&ip=185.176.40.135&fexp=23709359&ms=au%2Crdu&mt=1531126644&mv=u&dur=238.213&ratebypass=yes&c=WEB&source=youtube&clen=17583688&mn=sn-uxaxiv0nxx5q-nv4l%2Csn-nv47lney&lmt=1524197389423702&ipbits=0&mime=video%2Fmp4&itag=18&key=yt6&mm=31%2C29&fvip=2&requiressl=yes&pl=24&expire=1531148388&gir=yes&signature=75AE38437FE5016A1A5499E0B310299656BB6421.A5446E54FC5D090B969F05E1822208645BA728CE&title=Ariana-Grande-no-tears-left-to-cry

            [itag] => 18

            [type] => MP4[640x360]

        )

    [3] => Array

        (

            [url] => https://redirector.googlevideo.com/videoplayback?id=o-APhcxffiY6sr5fgEyc6ITssfWGyKfYa6_4KUfmWe2jYL&sparams=clen%2Cdur%2Cei%2Cgir%2Cid%2Cip%2Cipbits%2Citag%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Crequiressl%2Csource%2Cexpire&lmt=1524197367992167&ei=BCRDW_ijCdLygAeWkJGADA&ipbits=0&clen=6389374&ip=185.176.40.135&mime=video%2F3gpp&itag=36&key=yt6&fexp=23709359&ms=au%2Crdu&mt=1531126644&fvip=2&mv=u&source=youtube&requiressl=yes&dur=238.236&pl=24&expire=1531148388&c=WEB&gir=yes&mm=31%2C29&mn=sn-uxaxiv0nxx5q-nv4l%2Csn-nv47lney&signature=21FBC563406106077B6CAF3686EEA2E2B3A2565C.5ED1B7DE652AD3BD7DDD4B51759B3B9282738DFF&title=Ariana-Grande-no-tears-left-to-cry

            [itag] => 36

            [type] => 3GP[320x180]

        )

    [4] => Array

        (

            [url] => https://redirector.googlevideo.com/videoplayback?id=o-APhcxffiY6sr5fgEyc6ITssfWGyKfYa6_4KUfmWe2jYL&sparams=clen%2Cdur%2Cei%2Cgir%2Cid%2Cip%2Cipbits%2Citag%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Crequiressl%2Csource%2Cexpire&lmt=1524197364896415&ei=BCRDW_ijCdLygAeWkJGADA&ipbits=0&clen=2253898&ip=185.176.40.135&mime=video%2F3gpp&itag=17&key=yt6&fexp=23709359&ms=au%2Crdu&mt=1531126644&fvip=2&mv=u&source=youtube&requiressl=yes&dur=238.236&pl=24&expire=1531148388&c=WEB&gir=yes&mm=31%2C29&mn=sn-uxaxiv0nxx5q-nv4l%2Csn-nv47lney&signature=9DBA0FB7D08428681F5FD76C41027FAE6FE46EA7.3A0F737287663766D1D388CF1F57B2F543D76373&title=Ariana-Grande-no-tears-left-to-cry

            [itag] => 17

            [type] => 3GP[176x144]

        )

)

Array

(

    [0] => Array

        (

            [url] => https://redirector.googlevideo.com/videoplayback?id=o-APhcxffiY6sr5fgEyc6ITssfWGyKfYa6_4KUfmWe2jYL&sparams=dur%2Cei%2Cid%2Cip%2Cipbits%2Citag%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Cratebypass%2Crequiressl%2Csource%2Cexpire&lmt=1524198756368804&ei=BCRDW_ijCdLygAeWkJGADA&ipbits=0&ip=185.176.40.135&mime=video%2Fmp4&itag=22&key=yt6&fexp=23709359&ms=au%2Crdu&mt=1531126644&fvip=2&mv=u&requiressl=yes&dur=238.213&pl=24&ratebypass=yes&expire=1531148388&c=WEB&source=youtube&mm=31%2C29&mn=sn-uxaxiv0nxx5q-nv4l%2Csn-nv47lney&signature=4D7B0561F48AB1B65B2ECEE807E8335F1473A420.0280F197CE092877CF78A73FAE464DDC0574C9D6&title=Ariana-Grande-no-tears-left-to-cry

            [itag] => 22

            [type] => HD MP4[1280x720]

        )

    [1] => Array

        (

            [url] => https://redirector.googlevideo.com/videoplayback?id=o-APhcxffiY6sr5fgEyc6ITssfWGyKfYa6_4KUfmWe2jYL&sparams=clen%2Cdur%2Cei%2Cgir%2Cid%2Cip%2Cipbits%2Citag%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Cratebypass%2Crequiressl%2Csource%2Cexpire&ei=BCRDW_ijCdLygAeWkJGADA&ip=185.176.40.135&fexp=23709359&ms=au%2Crdu&mt=1531126644&mv=u&dur=0.000&ratebypass=yes&c=WEB&source=youtube&clen=24489177&mn=sn-uxaxiv0nxx5q-nv4l%2Csn-nv47lney&lmt=1524199428883596&ipbits=0&mime=video%2Fwebm&itag=43&key=yt6&mm=31%2C29&fvip=2&requiressl=yes&pl=24&expire=1531148388&gir=yes&signature=AD118809D71095D33D1489E856B6EACA5280209C.419939B86C5BA1EC1874F2C64CF02F702DC0551D&title=Ariana-Grande-no-tears-left-to-cry

            [itag] => 43

            [type] => WEBM[640x360]

        )

    [2] => Array

        (

            [url] => https://redirector.googlevideo.com/videoplayback?id=o-APhcxffiY6sr5fgEyc6ITssfWGyKfYa6_4KUfmWe2jYL&sparams=clen%2Cdur%2Cei%2Cgir%2Cid%2Cip%2Cipbits%2Citag%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Cratebypass%2Crequiressl%2Csource%2Cexpire&ei=BCRDW_ijCdLygAeWkJGADA&ip=185.176.40.135&fexp=23709359&ms=au%2Crdu&mt=1531126644&mv=u&dur=238.213&ratebypass=yes&c=WEB&source=youtube&clen=17583688&mn=sn-uxaxiv0nxx5q-nv4l%2Csn-nv47lney&lmt=1524197389423702&ipbits=0&mime=video%2Fmp4&itag=18&key=yt6&mm=31%2C29&fvip=2&requiressl=yes&pl=24&expire=1531148388&gir=yes&signature=75AE38437FE5016A1A5499E0B310299656BB6421.A5446E54FC5D090B969F05E1822208645BA728CE&title=Ariana-Grande-no-tears-left-to-cry

            [itag] => 18

            [type] => MP4[640x360]

        )

    [3] => Array

        (

            [url] => https://redirector.googlevideo.com/videoplayback?id=o-APhcxffiY6sr5fgEyc6ITssfWGyKfYa6_4KUfmWe2jYL&sparams=clen%2Cdur%2Cei%2Cgir%2Cid%2Cip%2Cipbits%2Citag%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Crequiressl%2Csource%2Cexpire&lmt=1524197367992167&ei=BCRDW_ijCdLygAeWkJGADA&ipbits=0&clen=6389374&ip=185.176.40.135&mime=video%2F3gpp&itag=36&key=yt6&fexp=23709359&ms=au%2Crdu&mt=1531126644&fvip=2&mv=u&source=youtube&requiressl=yes&dur=238.236&pl=24&expire=1531148388&c=WEB&gir=yes&mm=31%2C29&mn=sn-uxaxiv0nxx5q-nv4l%2Csn-nv47lney&signature=21FBC563406106077B6CAF3686EEA2E2B3A2565C.5ED1B7DE652AD3BD7DDD4B51759B3B9282738DFF&title=Ariana-Grande-no-tears-left-to-cry

            [itag] => 36

            [type] => 3GP[320x180]

        )

    [4] => Array

        (

            [url] => https://redirector.googlevideo.com/videoplayback?id=o-APhcxffiY6sr5fgEyc6ITssfWGyKfYa6_4KUfmWe2jYL&sparams=clen%2Cdur%2Cei%2Cgir%2Cid%2Cip%2Cipbits%2Citag%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Crequiressl%2Csource%2Cexpire&lmt=1524197364896415&ei=BCRDW_ijCdLygAeWkJGADA&ipbits=0&clen=2253898&ip=185.176.40.135&mime=video%2F3gpp&itag=17&key=yt6&fexp=23709359&ms=au%2Crdu&mt=1531126644&fvip=2&mv=u&source=youtube&requiressl=yes&dur=238.236&pl=24&expire=1531148388&c=WEB&gir=yes&mm=31%2C29&mn=sn-uxaxiv0nxx5q-nv4l%2Csn-nv47lney&signature=9DBA0FB7D08428681F5FD76C41027FAE6FE46EA7.3A0F737287663766D1D388CF1F57B2F543D76373&title=Ariana-Grande-no-tears-left-to-cry

            [itag] => 17

            [type] => 3GP[176x144]

        )

)

```
