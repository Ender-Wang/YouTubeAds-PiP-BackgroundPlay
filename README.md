# YouTube Ads Removed, PiP, Background Play

Quantumult X link: [YouTubeAds.conf](https://raw.githubusercontent.com/Ender-Wang/YouTubeAds-PiP-BackgroundPlay/main/YouTubeAds.conf).

# Credit

Based on [ddgksf2013's rewrite script](https://raw.githubusercontent.com/ddgksf2013/Rewrite/master/AdBlock/YoutubeAds.conf) (version 05172024), the only modification is the removal of the **captions translation** part, now the script **does not translate or show the captions by default**, while remaining the rest of the features provided by the original script. Visit [ddgksf2013](https://github.com/ddgksf2013/ddgksf2013) for more information.

# Change Log after formatted via Prettier

## Changes to `YouTubeAds.conf`

> **Original:**
>
> ```conf
> # ======= 视频PIP|后台播放|瀑布流|搜索页|播放页|短视频|贴片广告  ======= #
> ^https?:\/\/youtubei\.googleapis\.com\/youtubei\/v1\/(browse|next|player|reel\/reel_watch_sequence|get_watch) url script-request-body https://raw.githubusercontent.com/Maasea/sgmodule/master/Script/Youtube/dist/youtube.request.preview.js
> ^https?:\/\/youtubei\.googleapis\.com\/youtubei\/v1\/(browse|next|player|search|reel\/reel_watch_sequence|guide|account\/get_setting|get_watch) url script-response-body https://raw.githubusercontent.com/Maasea/sgmodule/master/Script/Youtube/dist/youtube.response.preview.js
> ```
>
> **Modified:**
>
> ```conf
> # ======= 视频PIP|后台播放|瀑布流|搜索页|播放页|短视频|贴片广告  ======= #
> ^https?:\/\/youtubei\.googleapis\.com\/youtubei\/v1\/(browse|next|player|reel\/reel_watch_sequence|get_watch) url script-request-body https://raw.githubusercontent.com/Ender-Wang/YouTubeAds-PiP-BackgroundPlay/main/youtube.request.preview.js
> ^https?:\/\/youtubei\.googleapis\.com\/youtubei\/v1\/(browse|next|player|search|reel\/reel_watch_sequence|guide|account\/get_setting|get_watch) url script-response-body https://raw.githubusercontent.com/Ender-Wang/YouTubeAds-PiP-BackgroundPlay/main/youtube.response.preview.js
> ```

## Changes to `youtube.request.preview.js`

> **Original line 2409-2410:**
>
> ```javascript
> lyricLang: "\u6B4C\u8BCD\u7FFB\u8BD1\u8BED\u8A00",
> captionLang: "\u5B57\u5E55\u7FFB\u8BD1\u8BED\u8A00",
> ```
>
> **Modified line 2409-2410:**
>
> ```javascript
> //   lyricLang: "\u6B4C\u8BCD\u7FFB\u8BD1\u8BED\u8A00",   //Default lyrics > Simplified Chinese off
> //   captionLang: "\u5B57\u5E55\u7FFB\u8BD1\u8BED\u8A00", //Default subtitles > Simplified Chinese off
> ```

> **Original line 2416-2417:**
>
> ```javascript
> lyricLang: "zh-Hans",
> captionLang: "zh-Hans",
> ```
>
> **Modified line 2416-2417:**
>
> ```javascript
> //   lyricLang: "zh-Hans", //Default Simplified Chinese
> //   captionLang: "zh-Hans", //Default Simplified Chinese
> ```

## Changes to `youtube.response.preview.js`

> **Original line 2809-2810:**
>
> ```javascript
> lyricLang: "\u6B4C\u8BCD\u7FFB\u8BD1\u8BED\u8A00",
> captionLang: "\u5B57\u5E55\u7FFB\u8BD1\u8BED\u8A00",
> ```
>
> **Modified line 2809-2810:**
>
> ```javascript
> //   lyricLang: "\u6B4C\u8BCD\u7FFB\u8BD1\u8BED\u8A00",   //Default > lyrics Simplified Chinese off
> //   captionLang: "\u5B57\u5E55\u7FFB\u8BD1\u8BED\u8A00", //Default > subtitles Simplified Chinese off
> ```

> **Original line 2816-2817:**
>
> ```javascript
> lyricLang: "zh-Hans",
> captionLang: "zh-Hans",
> ```
>
> **Modified line 2816-2817:**
>
> ```javascript
> //   lyricLang: "zh-Hans", //Default Simplified Chinese
> //   captionLang: "zh-Hans", //Default Simplified Chinese
> ```

> **Original line 3105:**
>
> ```javascript
> e !== "off";
> ```
>
> **Modified line 3105:**
>
> ```javascript
> e == "off";
> ```

<hr>

\*Tools used: [Text Compare](https://text-compare.com/) for comparing the original and modified files.
