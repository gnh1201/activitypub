## Potential Issues Stemming from YouTube Links Posted on ActivityPub Servers
YouTube links posted on ActivityPub servers are often cited by users as a concern, due to technical methods that can be used to track visitors (e.g., the `si` parameter included in shared URLs, and various tracking technologies embedded in the YouTube website).

However, it seems unlikely that projects implementing the ActivityPub protocol will offer any solutions to this issue, as it is difficult to view it as a problem limited to a specific service like YouTube.

That said, server administrators can still implement measures to help mitigate these concerns.

### Use the alternative frontend
To address this issue, one possible approach is to use so-called "alternative frontends" — independently developed frontends for YouTube. Well-known projects in this category include [**Piped**](https://github.com/TeamPiped/Piped) and [**Invidious**](https://github.com/iv-org/invidious).

As of now, **Piped** is the project that is actively maintained and frequently updated with bug fixes.

### Use the `sub_filter` on Nginx
Once the alternative frontend has been set up, YouTube links can be rewritten using Nginx's **sub\_filter** feature. This prevents users from accessing the original YouTube links directly and instead encourages them to view the videos through the alternative frontend. For example:

```
sub_filter 'www.youtube.com/' 'dnt-yt.catswords.net/';
sub_filter 'youtube.com/' 'dnt-yt.catswords.net/';
sub_filter 'www.youtu.be/' 'dnt-yt.catswords.net/';
sub_filter 'youtu.be/' 'dnt-yt.catswords.net/';
```

### Result
Once you confirm that links to youtube.com or youtu.be are being replaced with links to the alternative frontend, the setup is complete.

A real-world example of this implementation can be seen at the following link:

https://catswords.social/@gnh1201/114784215434521357
