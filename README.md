[![Build Status](https://travis-ci.org/hex-firebone/YouTube-Downloader.svg?branch=master)](https://travis-ci.org/hex-firebone/YouTube-Downloader)
[![Maintainability](https://api.codeclimate.com/v1/badges/a970dc85ec7f781e0797/maintainability)](https://codeclimate.com/github/madcode-git/YouTube-Downloader/maintainability)
[![Test Coverage](https://api.codeclimate.com/v1/badges/a970dc85ec7f781e0797/test_coverage)](https://codeclimate.com/github/madcode-git/YouTube-Downloader/test_coverage)

# YouTube Downloader

This project was inspired by a very popular [youtube-dl](https://github.com/rg3/youtube-dl) python package:

Yes, there are multiple PHP-based youtube downloaders on the Internet, but all of them haven't been updated in years or they depend on youtube-dl.

This script does not depend on anything other than cURL. No Javascript interpreters, no calls to shell... nothing but pure PHP :heart_eyes:

## Installation

#### Recommended way of installing this is via [Composer](http://getcomposer.org/):

```
composer require madcodez/youtube-downloader
```

## Usage

```php
$yt = new YTDownloader();

$links = $yt->getDownloadLinks("ffxKSjUwKdU");

print_r($links);
```
or 

```php
$yt = new YTDownloader();

$links = $yt->getDownloadLinks("https://www.youtube.com/watch?v=ffxKSjUwKdU");

print_r($links);
```

### Result 

```

Array
(
    [info] => Array
        (
            [Title] => Ariana Grande - no tears left to cry
            [ChannelName] => ArianaGrandeVevo
            [ChannelId] => UC0VOyT2OCBKdQhF3BAbZ-1g
            [Thumbnail] => http://i.ytimg.com/vi/ffxKSjUwKdU/hqdefault.jpg
            [Duration] => 238
            [Rating] => 4.80527830124
        )

    [dl] => Array
        (
            [0] => Array
                (
                    [url] => https://redirector.googlevideo.com/videoplayback?id=o-ABcxmZMkg98lAO0dp9abnFs0C33MuKLErLgGbdxpTC_C&mt=1543239431&mv=m&ms=au%2Crdu&mm=31%2C29&ip=103.67.156.47&mn=sn-c5oba5apo3-q5jl%2Csn-h557sns7&pl=23&expire=1543261177&gir=yes&c=WEB&key=yt6&txp=5531432&mime=video%2Fmp4&fvip=2&clen=17192723&dur=238.213&itag=18&ratebypass=yes&requiressl=yes&source=youtube&initcwndbps=86250&ei=mff7W5WeM5rkogP4-pegCg&sparams=clen%2Cdur%2Cei%2Cgir%2Cid%2Cinitcwndbps%2Cip%2Cipbits%2Citag%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Cratebypass%2Crequiressl%2Csource%2Cexpire&lmt=1540323392448324&ipbits=0&signature=CADC1E3F71D7DA574A0A02ABB5DEED68AA28A0AD.7D569D982EAFB7F79C0250647E53555CACE9461A&title=Ariana-Grande-no-tears-left-to-cry
                    [itag] => 18
                    [type] => MP4[640x360]
                )

            [1] => Array
                (
                    [url] => https://redirector.googlevideo.com/videoplayback?id=o-ABcxmZMkg98lAO0dp9abnFs0C33MuKLErLgGbdxpTC_C&mt=1543239431&mv=m&ms=au%2Crdu&mm=31%2C29&ip=103.67.156.47&mn=sn-c5oba5apo3-q5jl%2Csn-h557sns7&pl=23&expire=1543261177&gir=yes&c=WEB&key=yt6&txp=5531432&mime=video%2F3gpp&fvip=2&clen=6285149&dur=238.236&itag=36&requiressl=yes&source=youtube&initcwndbps=86250&ei=mff7W5WeM5rkogP4-pegCg&sparams=clen%2Cdur%2Cei%2Cgir%2Cid%2Cinitcwndbps%2Cip%2Cipbits%2Citag%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Crequiressl%2Csource%2Cexpire&lmt=1540322734148881&ipbits=0&signature=3D02AE0057F622B2DCCF8B097AD9D461A5EC6FD5.D936BA7418701A92F8CD08D277301BA08F94DCE9&title=Ariana-Grande-no-tears-left-to-cry
                    [itag] => 36
                    [type] => 3GP[320x180]
                )

            [2] => Array
                (
                    [url] => https://redirector.googlevideo.com/videoplayback?id=o-ABcxmZMkg98lAO0dp9abnFs0C33MuKLErLgGbdxpTC_C&mt=1543239431&mv=m&ms=au%2Crdu&mm=31%2C29&ip=103.67.156.47&mn=sn-c5oba5apo3-q5jl%2Csn-h557sns7&pl=23&expire=1543261177&gir=yes&c=WEB&key=yt6&txp=5531432&mime=video%2F3gpp&fvip=2&clen=2231775&dur=238.236&itag=17&requiressl=yes&source=youtube&initcwndbps=86250&ei=mff7W5WeM5rkogP4-pegCg&sparams=clen%2Cdur%2Cei%2Cgir%2Cid%2Cinitcwndbps%2Cip%2Cipbits%2Citag%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Crequiressl%2Csource%2Cexpire&lmt=1540322735757079&ipbits=0&signature=8DB3FA96822044D420B7B8ABF13874DB71FC480B.5725A695148B5E6ED96E61825ABB5E960E73B2DF&title=Ariana-Grande-no-tears-left-to-cry
                    [itag] => 17
                    [type] => 3GP[176x144]
                )

            [3] => Array
                (
                    [url] => https://redirector.googlevideo.com/videoplayback?id=o-ABcxmZMkg98lAO0dp9abnFs0C33MuKLErLgGbdxpTC_C&mt=1543239431&mv=m&ms=au%2Crdu&mm=31%2C29&ip=103.67.156.47&mn=sn-c5oba5apo3-q5jl%2Csn-h557sns7&pl=23&itag=137&gir=yes&c=WEB&key=yt6&txp=5533432&mime=video%2Fmp4&expire=1543261177&fvip=2&clen=47758513&dur=238.154&requiressl=yes&source=youtube&initcwndbps=86250&ei=mff7W5WeM5rkogP4-pegCg&keepalive=yes&sparams=aitags%2Cclen%2Cdur%2Cei%2Cgir%2Cid%2Cinitcwndbps%2Cip%2Cipbits%2Citag%2Ckeepalive%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Crequiressl%2Csource%2Cexpire&lmt=1540327635775976&ipbits=0&aitags=133%2C134%2C135%2C136%2C137%2C160%2C242%2C243%2C244%2C247%2C248%2C278%2C394%2C395%2C396%2C397&signature=06A80F030B77494A104F2419FD128EE9D0F5ACFE.D8F394202B96BC5021C4FB2A2CCA6DE27FA60BB7&title=Ariana-Grande-no-tears-left-to-cry
                    [itag] => 137
                    [type] => (Video Only) MP4[1920x1080]
                )

            [4] => Array
                (
                    [url] => https://redirector.googlevideo.com/videoplayback?id=o-ABcxmZMkg98lAO0dp9abnFs0C33MuKLErLgGbdxpTC_C&mt=1543239431&mv=m&ms=au%2Crdu&mm=31%2C29&ip=103.67.156.47&mn=sn-c5oba5apo3-q5jl%2Csn-h557sns7&pl=23&itag=248&gir=yes&c=WEB&key=yt6&txp=5533432&mime=video%2Fwebm&expire=1543261177&fvip=2&clen=46513069&dur=238.154&requiressl=yes&source=youtube&initcwndbps=86250&ei=mff7W5WeM5rkogP4-pegCg&keepalive=yes&sparams=aitags%2Cclen%2Cdur%2Cei%2Cgir%2Cid%2Cinitcwndbps%2Cip%2Cipbits%2Citag%2Ckeepalive%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Crequiressl%2Csource%2Cexpire&lmt=1540328055212110&ipbits=0&aitags=133%2C134%2C135%2C136%2C137%2C160%2C242%2C243%2C244%2C247%2C248%2C278%2C394%2C395%2C396%2C397&signature=207F407CD755569608038CBC6EADA8E49DC12303.AA932870C9B2EA83C450DBE2C92DB1D191EC38E0&title=Ariana-Grande-no-tears-left-to-cry
                    [itag] => 248
                    [type] => (Video Only) WEBM[1920x1080]
                )

            [5] => Array
                (
                    [url] => https://redirector.googlevideo.com/videoplayback?id=o-ABcxmZMkg98lAO0dp9abnFs0C33MuKLErLgGbdxpTC_C&mt=1543239431&mv=m&ms=au%2Crdu&mm=31%2C29&ip=103.67.156.47&mn=sn-c5oba5apo3-q5jl%2Csn-h557sns7&pl=23&itag=136&gir=yes&c=WEB&key=yt6&txp=5533432&mime=video%2Fmp4&expire=1543261177&fvip=2&clen=32178846&dur=238.154&requiressl=yes&source=youtube&initcwndbps=86250&ei=mff7W5WeM5rkogP4-pegCg&keepalive=yes&sparams=aitags%2Cclen%2Cdur%2Cei%2Cgir%2Cid%2Cinitcwndbps%2Cip%2Cipbits%2Citag%2Ckeepalive%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Crequiressl%2Csource%2Cexpire&lmt=1540327373678757&ipbits=0&aitags=133%2C134%2C135%2C136%2C137%2C160%2C242%2C243%2C244%2C247%2C248%2C278%2C394%2C395%2C396%2C397&signature=074E746D2DECDE9939BBFF89E37E128D2EFBB1E9.6467CA98085004F4506BA9CC756035661E7BD230&title=Ariana-Grande-no-tears-left-to-cry
                    [itag] => 136
                    [type] => (Video Only) MP4[1280x720]
                )

            [6] => Array
                (
                    [url] => https://redirector.googlevideo.com/videoplayback?id=o-ABcxmZMkg98lAO0dp9abnFs0C33MuKLErLgGbdxpTC_C&mt=1543239431&mv=m&ms=au%2Crdu&mm=31%2C29&ip=103.67.156.47&mn=sn-c5oba5apo3-q5jl%2Csn-h557sns7&pl=23&itag=247&gir=yes&c=WEB&key=yt6&txp=5533432&mime=video%2Fwebm&expire=1543261177&fvip=2&clen=31109333&dur=238.154&requiressl=yes&source=youtube&initcwndbps=86250&ei=mff7W5WeM5rkogP4-pegCg&keepalive=yes&sparams=aitags%2Cclen%2Cdur%2Cei%2Cgir%2Cid%2Cinitcwndbps%2Cip%2Cipbits%2Citag%2Ckeepalive%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Crequiressl%2Csource%2Cexpire&lmt=1540328094157172&ipbits=0&aitags=133%2C134%2C135%2C136%2C137%2C160%2C242%2C243%2C244%2C247%2C248%2C278%2C394%2C395%2C396%2C397&signature=C5EE226C9FBDDB1DB92447F0F80A3ABB7B4EA6E9.83AC0D3C7EBD40418DE685447C519DE7470A8130&title=Ariana-Grande-no-tears-left-to-cry
                    [itag] => 247
                    [type] => (Video Only) WEBM[1280x720]
                )

            [7] => Array
                (
                    [url] => https://redirector.googlevideo.com/videoplayback?id=o-ABcxmZMkg98lAO0dp9abnFs0C33MuKLErLgGbdxpTC_C&mt=1543239431&mv=m&ms=au%2Crdu&mm=31%2C29&ip=103.67.156.47&mn=sn-c5oba5apo3-q5jl%2Csn-h557sns7&pl=23&itag=135&gir=yes&c=WEB&key=yt6&txp=5533432&mime=video%2Fmp4&expire=1543261177&fvip=2&clen=20735386&dur=238.154&requiressl=yes&source=youtube&initcwndbps=86250&ei=mff7W5WeM5rkogP4-pegCg&keepalive=yes&sparams=aitags%2Cclen%2Cdur%2Cei%2Cgir%2Cid%2Cinitcwndbps%2Cip%2Cipbits%2Citag%2Ckeepalive%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Crequiressl%2Csource%2Cexpire&lmt=1540327352923243&ipbits=0&aitags=133%2C134%2C135%2C136%2C137%2C160%2C242%2C243%2C244%2C247%2C248%2C278%2C394%2C395%2C396%2C397&signature=35730AC3EA44E75BA8CB589A668E53D9D85C911A.267D072B6B9B285E10833CDCD007545D8C1E0C30&title=Ariana-Grande-no-tears-left-to-cry
                    [itag] => 135
                    [type] => (Video Only) MP4[854x480]
                )

            [8] => Array
                (
                    [url] => https://redirector.googlevideo.com/videoplayback?id=o-ABcxmZMkg98lAO0dp9abnFs0C33MuKLErLgGbdxpTC_C&mt=1543239431&mv=m&ms=au%2Crdu&mm=31%2C29&ip=103.67.156.47&mn=sn-c5oba5apo3-q5jl%2Csn-h557sns7&pl=23&itag=244&gir=yes&c=WEB&key=yt6&txp=5533432&mime=video%2Fwebm&expire=1543261177&fvip=2&clen=18919018&dur=238.154&requiressl=yes&source=youtube&initcwndbps=86250&ei=mff7W5WeM5rkogP4-pegCg&keepalive=yes&sparams=aitags%2Cclen%2Cdur%2Cei%2Cgir%2Cid%2Cinitcwndbps%2Cip%2Cipbits%2Citag%2Ckeepalive%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Crequiressl%2Csource%2Cexpire&lmt=1540328353904518&ipbits=0&aitags=133%2C134%2C135%2C136%2C137%2C160%2C242%2C243%2C244%2C247%2C248%2C278%2C394%2C395%2C396%2C397&signature=52E8F673170B98AEE1950B452B8285AFF4E09B62.4B117929F268805F49937EA5A08F7A2C36F3A6FB&title=Ariana-Grande-no-tears-left-to-cry
                    [itag] => 244
                    [type] => (Video Only) WEBM[854x480]
                )

            [9] => Array
                (
                    [url] => https://redirector.googlevideo.com/videoplayback?id=o-ABcxmZMkg98lAO0dp9abnFs0C33MuKLErLgGbdxpTC_C&mt=1543239431&mv=m&ms=au%2Crdu&mm=31%2C29&ip=103.67.156.47&mn=sn-c5oba5apo3-q5jl%2Csn-h557sns7&pl=23&itag=397&gir=yes&c=WEB&key=yt6&txp=5511222&mime=video%2Fmp4&expire=1543261177&fvip=2&clen=15927702&dur=238.154&requiressl=yes&source=youtube&initcwndbps=86250&ei=mff7W5WeM5rkogP4-pegCg&keepalive=yes&sparams=aitags%2Cclen%2Cdur%2Cei%2Cgir%2Cid%2Cinitcwndbps%2Cip%2Cipbits%2Citag%2Ckeepalive%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Crequiressl%2Csource%2Cexpire&lmt=1540338215194934&ipbits=0&aitags=133%2C134%2C135%2C136%2C137%2C160%2C242%2C243%2C244%2C247%2C248%2C278%2C394%2C395%2C396%2C397&signature=319D891A535368DE12B79D773E0AABD13F51599B.B135D3AD38E092D7E5C3F8845D8F2F0AC531C409&title=Ariana-Grande-no-tears-left-to-cry
                    [itag] => 397
                    [type] => Unknown
                )

            [10] => Array
                (
                    [url] => https://redirector.googlevideo.com/videoplayback?id=o-ABcxmZMkg98lAO0dp9abnFs0C33MuKLErLgGbdxpTC_C&mt=1543239431&mv=m&ms=au%2Crdu&mm=31%2C29&ip=103.67.156.47&mn=sn-c5oba5apo3-q5jl%2Csn-h557sns7&pl=23&itag=134&gir=yes&c=WEB&key=yt6&txp=5533432&mime=video%2Fmp4&expire=1543261177&fvip=2&clen=12405443&dur=238.154&requiressl=yes&source=youtube&initcwndbps=86250&ei=mff7W5WeM5rkogP4-pegCg&keepalive=yes&sparams=aitags%2Cclen%2Cdur%2Cei%2Cgir%2Cid%2Cinitcwndbps%2Cip%2Cipbits%2Citag%2Ckeepalive%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Crequiressl%2Csource%2Cexpire&lmt=1540327292823042&ipbits=0&aitags=133%2C134%2C135%2C136%2C137%2C160%2C242%2C243%2C244%2C247%2C248%2C278%2C394%2C395%2C396%2C397&signature=11FBC49A47C44120A480C52C553C77182345D3CE.7E29F20189539B2124B7E7EA29C99F6BBCC4DBB2&title=Ariana-Grande-no-tears-left-to-cry
                    [itag] => 134
                    [type] => (Video Only) MP4[640x360]
                )

            [11] => Array
                (
                    [url] => https://redirector.googlevideo.com/videoplayback?id=o-ABcxmZMkg98lAO0dp9abnFs0C33MuKLErLgGbdxpTC_C&mt=1543239431&mv=m&ms=au%2Crdu&mm=31%2C29&ip=103.67.156.47&mn=sn-c5oba5apo3-q5jl%2Csn-h557sns7&pl=23&itag=243&gir=yes&c=WEB&key=yt6&txp=5533432&mime=video%2Fwebm&expire=1543261177&fvip=2&clen=10586626&dur=238.154&requiressl=yes&source=youtube&initcwndbps=86250&ei=mff7W5WeM5rkogP4-pegCg&keepalive=yes&sparams=aitags%2Cclen%2Cdur%2Cei%2Cgir%2Cid%2Cinitcwndbps%2Cip%2Cipbits%2Citag%2Ckeepalive%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Crequiressl%2Csource%2Cexpire&lmt=1540328390781881&ipbits=0&aitags=133%2C134%2C135%2C136%2C137%2C160%2C242%2C243%2C244%2C247%2C248%2C278%2C394%2C395%2C396%2C397&signature=3AF4AC8CF0BA0B9632837E82A658302B6DD7A024.424E54AB2F613D33AFEA8D52CC8F1CC74D7055F9&title=Ariana-Grande-no-tears-left-to-cry
                    [itag] => 243
                    [type] => (Video Only) WEBM[640x360]
                )

            [12] => Array
                (
                    [url] => https://redirector.googlevideo.com/videoplayback?id=o-ABcxmZMkg98lAO0dp9abnFs0C33MuKLErLgGbdxpTC_C&mt=1543239431&mv=m&ms=au%2Crdu&mm=31%2C29&ip=103.67.156.47&mn=sn-c5oba5apo3-q5jl%2Csn-h557sns7&pl=23&itag=396&gir=yes&c=WEB&key=yt6&txp=5511222&mime=video%2Fmp4&expire=1543261177&fvip=2&clen=9162662&dur=238.154&requiressl=yes&source=youtube&initcwndbps=86250&ei=mff7W5WeM5rkogP4-pegCg&keepalive=yes&sparams=aitags%2Cclen%2Cdur%2Cei%2Cgir%2Cid%2Cinitcwndbps%2Cip%2Cipbits%2Citag%2Ckeepalive%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Crequiressl%2Csource%2Cexpire&lmt=1540335132601804&ipbits=0&aitags=133%2C134%2C135%2C136%2C137%2C160%2C242%2C243%2C244%2C247%2C248%2C278%2C394%2C395%2C396%2C397&signature=7BA42223A44B2EA0D3B8ECF5960FA61F52326168.A4384B97BDB074D40E2053E75EA3B2B9130D6B0D&title=Ariana-Grande-no-tears-left-to-cry
                    [itag] => 396
                    [type] => Unknown
                )

            [13] => Array
                (
                    [url] => https://redirector.googlevideo.com/videoplayback?id=o-ABcxmZMkg98lAO0dp9abnFs0C33MuKLErLgGbdxpTC_C&mt=1543239431&mv=m&ms=au%2Crdu&mm=31%2C29&ip=103.67.156.47&mn=sn-c5oba5apo3-q5jl%2Csn-h557sns7&pl=23&itag=133&gir=yes&c=WEB&key=yt6&txp=5533432&mime=video%2Fmp4&expire=1543261177&fvip=2&clen=5787145&dur=238.154&requiressl=yes&source=youtube&initcwndbps=86250&ei=mff7W5WeM5rkogP4-pegCg&keepalive=yes&sparams=aitags%2Cclen%2Cdur%2Cei%2Cgir%2Cid%2Cinitcwndbps%2Cip%2Cipbits%2Citag%2Ckeepalive%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Crequiressl%2Csource%2Cexpire&lmt=1540327270090562&ipbits=0&aitags=133%2C134%2C135%2C136%2C137%2C160%2C242%2C243%2C244%2C247%2C248%2C278%2C394%2C395%2C396%2C397&signature=DF16585807DC16AB7B78F02E8321A0E42F1F5880.8634D479AB6EEF37A6023ACD38253FDD99BB8B2C&title=Ariana-Grande-no-tears-left-to-cry
                    [itag] => 133
                    [type] => (Video Only) MP4[320x240]
                )

            [14] => Array
                (
                    [url] => https://redirector.googlevideo.com/videoplayback?id=o-ABcxmZMkg98lAO0dp9abnFs0C33MuKLErLgGbdxpTC_C&mt=1543239431&mv=m&ms=au%2Crdu&mm=31%2C29&ip=103.67.156.47&mn=sn-c5oba5apo3-q5jl%2Csn-h557sns7&pl=23&itag=242&gir=yes&c=WEB&key=yt6&txp=5533432&mime=video%2Fwebm&expire=1543261177&fvip=2&clen=5338701&dur=238.154&requiressl=yes&source=youtube&initcwndbps=86250&ei=mff7W5WeM5rkogP4-pegCg&keepalive=yes&sparams=aitags%2Cclen%2Cdur%2Cei%2Cgir%2Cid%2Cinitcwndbps%2Cip%2Cipbits%2Citag%2Ckeepalive%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Crequiressl%2Csource%2Cexpire&lmt=1540328539660504&ipbits=0&aitags=133%2C134%2C135%2C136%2C137%2C160%2C242%2C243%2C244%2C247%2C248%2C278%2C394%2C395%2C396%2C397&signature=6972BEC81A2A815AB21815656347182F7C2C7F54.5C1876B34AB2F51DB6ED912D913F1AF89C59EAF9&title=Ariana-Grande-no-tears-left-to-cry
                    [itag] => 242
                    [type] => (Video Only) WEBM[320x240]
                )

            [15] => Array
                (
                    [url] => https://redirector.googlevideo.com/videoplayback?id=o-ABcxmZMkg98lAO0dp9abnFs0C33MuKLErLgGbdxpTC_C&mt=1543239431&mv=m&ms=au%2Crdu&mm=31%2C29&ip=103.67.156.47&mn=sn-c5oba5apo3-q5jl%2Csn-h557sns7&pl=23&itag=395&gir=yes&c=WEB&key=yt6&txp=5511222&mime=video%2Fmp4&expire=1543261177&fvip=2&clen=5152281&dur=238.154&requiressl=yes&source=youtube&initcwndbps=86250&ei=mff7W5WeM5rkogP4-pegCg&keepalive=yes&sparams=aitags%2Cclen%2Cdur%2Cei%2Cgir%2Cid%2Cinitcwndbps%2Cip%2Cipbits%2Citag%2Ckeepalive%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Crequiressl%2Csource%2Cexpire&lmt=1540333129940852&ipbits=0&aitags=133%2C134%2C135%2C136%2C137%2C160%2C242%2C243%2C244%2C247%2C248%2C278%2C394%2C395%2C396%2C397&signature=35807C4538487FFA7228DF600265DF9E2361DBF0.B0510051DF912F7CE3028F22B777529C95EF4F3F&title=Ariana-Grande-no-tears-left-to-cry
                    [itag] => 395
                    [type] => Unknown
                )

            [16] => Array
                (
                    [url] => https://redirector.googlevideo.com/videoplayback?id=o-ABcxmZMkg98lAO0dp9abnFs0C33MuKLErLgGbdxpTC_C&mt=1543239431&mv=m&ms=au%2Crdu&mm=31%2C29&ip=103.67.156.47&mn=sn-c5oba5apo3-q5jl%2Csn-h557sns7&pl=23&itag=160&gir=yes&c=WEB&key=yt6&txp=5533432&mime=video%2Fmp4&expire=1543261177&fvip=2&clen=2242718&dur=238.154&requiressl=yes&source=youtube&initcwndbps=86250&ei=mff7W5WeM5rkogP4-pegCg&keepalive=yes&sparams=aitags%2Cclen%2Cdur%2Cei%2Cgir%2Cid%2Cinitcwndbps%2Cip%2Cipbits%2Citag%2Ckeepalive%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Crequiressl%2Csource%2Cexpire&lmt=1540327246360189&ipbits=0&aitags=133%2C134%2C135%2C136%2C137%2C160%2C242%2C243%2C244%2C247%2C248%2C278%2C394%2C395%2C396%2C397&signature=AC4527492F2AE5DDA3632D2DFFB0ECB1B2ADBE9A.0E2E3EF693ADE703BFB4476854896A9D8D222C77&title=Ariana-Grande-no-tears-left-to-cry
                    [itag] => 160
                    [type] => (Video Only) MP4[176x144]
                )

            [17] => Array
                (
                    [url] => https://redirector.googlevideo.com/videoplayback?id=o-ABcxmZMkg98lAO0dp9abnFs0C33MuKLErLgGbdxpTC_C&mt=1543239431&mv=m&ms=au%2Crdu&mm=31%2C29&ip=103.67.156.47&mn=sn-c5oba5apo3-q5jl%2Csn-h557sns7&pl=23&itag=278&gir=yes&c=WEB&key=yt6&txp=5533432&mime=video%2Fwebm&expire=1543261177&fvip=2&clen=2677938&dur=238.154&requiressl=yes&source=youtube&initcwndbps=86250&ei=mff7W5WeM5rkogP4-pegCg&keepalive=yes&sparams=aitags%2Cclen%2Cdur%2Cei%2Cgir%2Cid%2Cinitcwndbps%2Cip%2Cipbits%2Citag%2Ckeepalive%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Crequiressl%2Csource%2Cexpire&lmt=1540328235731055&ipbits=0&aitags=133%2C134%2C135%2C136%2C137%2C160%2C242%2C243%2C244%2C247%2C248%2C278%2C394%2C395%2C396%2C397&signature=30D157449CC2ADA0AD0EAC0E5CB69AE3F6B0B186.DB19F4FE5F55EFC96C8C8F5877981DA6B6F15AB7&title=Ariana-Grande-no-tears-left-to-cry
                    [itag] => 278
                    [type] => (Video Only) WEBM[176x144]
                )

            [18] => Array
                (
                    [url] => https://redirector.googlevideo.com/videoplayback?id=o-ABcxmZMkg98lAO0dp9abnFs0C33MuKLErLgGbdxpTC_C&mt=1543239431&mv=m&ms=au%2Crdu&mm=31%2C29&ip=103.67.156.47&mn=sn-c5oba5apo3-q5jl%2Csn-h557sns7&pl=23&itag=394&gir=yes&c=WEB&key=yt6&txp=5511222&mime=video%2Fmp4&expire=1543261177&fvip=2&clen=2391292&dur=238.154&requiressl=yes&source=youtube&initcwndbps=86250&ei=mff7W5WeM5rkogP4-pegCg&keepalive=yes&sparams=aitags%2Cclen%2Cdur%2Cei%2Cgir%2Cid%2Cinitcwndbps%2Cip%2Cipbits%2Citag%2Ckeepalive%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Crequiressl%2Csource%2Cexpire&lmt=1540332148742671&ipbits=0&aitags=133%2C134%2C135%2C136%2C137%2C160%2C242%2C243%2C244%2C247%2C248%2C278%2C394%2C395%2C396%2C397&signature=568027EDD4879021599B089FB2FDE5DFE1C08297.126C8B63219593FB0176484E59BDE2DB1938E46B&title=Ariana-Grande-no-tears-left-to-cry
                    [itag] => 394
                    [type] => Unknown
                )

            [19] => Array
                (
                    [url] => https://redirector.googlevideo.com/videoplayback?id=o-ABcxmZMkg98lAO0dp9abnFs0C33MuKLErLgGbdxpTC_C&mt=1543239431&mv=m&ms=au%2Crdu&mm=31%2C29&ip=103.67.156.47&mn=sn-c5oba5apo3-q5jl%2Csn-h557sns7&pl=23&itag=140&gir=yes&c=WEB&key=yt6&txp=5533432&mime=audio%2Fmp4&expire=1543261177&fvip=2&clen=3784047&dur=238.213&requiressl=yes&source=youtube&initcwndbps=86250&ei=mff7W5WeM5rkogP4-pegCg&keepalive=yes&sparams=clen%2Cdur%2Cei%2Cgir%2Cid%2Cinitcwndbps%2Cip%2Cipbits%2Citag%2Ckeepalive%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Crequiressl%2Csource%2Cexpire&lmt=1540325077923834&ipbits=0&signature=ADC55883CEA2CA6D492DF2BAAE7956C83B1F6E85.3E10B9BA97E9D243C48F1E7DC53BDFC035C9468E&title=Ariana-Grande-no-tears-left-to-cry
                    [itag] => 140
                    [type] => (Audio Only) M4A[128Kbps]
                )

            [20] => Array
                (
                    [url] => https://redirector.googlevideo.com/videoplayback?id=o-ABcxmZMkg98lAO0dp9abnFs0C33MuKLErLgGbdxpTC_C&mt=1543239431&mv=m&ms=au%2Crdu&mm=31%2C29&ip=103.67.156.47&mn=sn-c5oba5apo3-q5jl%2Csn-h557sns7&pl=23&itag=171&gir=yes&c=WEB&key=yt6&txp=5511222&mime=audio%2Fwebm&expire=1543261177&fvip=2&clen=3596671&dur=238.150&requiressl=yes&source=youtube&initcwndbps=86250&ei=mff7W5WeM5rkogP4-pegCg&keepalive=yes&sparams=clen%2Cdur%2Cei%2Cgir%2Cid%2Cinitcwndbps%2Cip%2Cipbits%2Citag%2Ckeepalive%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Crequiressl%2Csource%2Cexpire&lmt=1540339743437619&ipbits=0&signature=787C37933ED1E8230E574B235C1E6FBB61E7A9C4.0EBD5A86A701C7E22026A4F32A9713B31E797E1E&title=Ariana-Grande-no-tears-left-to-cry
                    [itag] => 171
                    [type] => (Audio Only) WEBM[128Kbps]
                )

            [21] => Array
                (
                    [url] => https://redirector.googlevideo.com/videoplayback?id=o-ABcxmZMkg98lAO0dp9abnFs0C33MuKLErLgGbdxpTC_C&mt=1543239431&mv=m&ms=au%2Crdu&mm=31%2C29&ip=103.67.156.47&mn=sn-c5oba5apo3-q5jl%2Csn-h557sns7&pl=23&itag=249&gir=yes&c=WEB&key=yt6&txp=5511222&mime=audio%2Fwebm&expire=1543261177&fvip=2&clen=1471340&dur=238.181&requiressl=yes&source=youtube&initcwndbps=86250&ei=mff7W5WeM5rkogP4-pegCg&keepalive=yes&sparams=clen%2Cdur%2Cei%2Cgir%2Cid%2Cinitcwndbps%2Cip%2Cipbits%2Citag%2Ckeepalive%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Crequiressl%2Csource%2Cexpire&lmt=1540339743826892&ipbits=0&signature=0DFCE7E51298BA4FE4CFF8C024DD6AB6E0987CC3.B36B46405AA5A62ED5D5A3BE4E7EA0570F8828A4&title=Ariana-Grande-no-tears-left-to-cry
                    [itag] => 249
                    [type] => (Audio Only) WEBM[50Kbps]
                )

            [22] => Array
                (
                    [url] => https://redirector.googlevideo.com/videoplayback?id=o-ABcxmZMkg98lAO0dp9abnFs0C33MuKLErLgGbdxpTC_C&mt=1543239431&mv=m&ms=au%2Crdu&mm=31%2C29&ip=103.67.156.47&mn=sn-c5oba5apo3-q5jl%2Csn-h557sns7&pl=23&itag=250&gir=yes&c=WEB&key=yt6&txp=5511222&mime=audio%2Fwebm&expire=1543261177&fvip=2&clen=1931230&dur=238.181&requiressl=yes&source=youtube&initcwndbps=86250&ei=mff7W5WeM5rkogP4-pegCg&keepalive=yes&sparams=clen%2Cdur%2Cei%2Cgir%2Cid%2Cinitcwndbps%2Cip%2Cipbits%2Citag%2Ckeepalive%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Crequiressl%2Csource%2Cexpire&lmt=1540339743415146&ipbits=0&signature=7F001BF89FD774FE4D3480E0B222B2B10A7F54F1.CF16FD66F2CCFE161FAD587C2E4AAFD6B9CB5137&title=Ariana-Grande-no-tears-left-to-cry
                    [itag] => 250
                    [type] => (Audio Only) WEBM[70Kbps]
                )

            [23] => Array
                (
                    [url] => https://redirector.googlevideo.com/videoplayback?id=o-ABcxmZMkg98lAO0dp9abnFs0C33MuKLErLgGbdxpTC_C&mt=1543239431&mv=m&ms=au%2Crdu&mm=31%2C29&ip=103.67.156.47&mn=sn-c5oba5apo3-q5jl%2Csn-h557sns7&pl=23&itag=251&gir=yes&c=WEB&key=yt6&txp=5511222&mime=audio%2Fwebm&expire=1543261177&fvip=2&clen=3789543&dur=238.181&requiressl=yes&source=youtube&initcwndbps=86250&ei=mff7W5WeM5rkogP4-pegCg&keepalive=yes&sparams=clen%2Cdur%2Cei%2Cgir%2Cid%2Cinitcwndbps%2Cip%2Cipbits%2Citag%2Ckeepalive%2Clmt%2Cmime%2Cmm%2Cmn%2Cms%2Cmv%2Cpl%2Crequiressl%2Csource%2Cexpire&lmt=1540339742978708&ipbits=0&signature=8BD8C6F2FE974762341C1F73DA8A4153E64FD784.E2BBA156A639A10D91734ADEF051E212C8A3A2C3&title=Ariana-Grande-no-tears-left-to-cry
                    [itag] => 251
                    [type] => (Audio Only) WEBM[160Kbps]
                )

        )

)

```
