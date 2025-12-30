## Preventing YouTube Tracking Links on ActivityPub Servers

YouTube links shared on ActivityPub servers are often cited by users as a privacy concern. This is due to various technical mechanisms that can be used to track visitors, such as the `si` parameter included in shared URLs and additional tracking technologies embedded in the YouTube website itself.

In practice, it is unlikely that projects implementing the ActivityPub protocol will provide a built-in solution to this issue, as it is not a problem limited to a single service like YouTube but rather a broader web-tracking concern.

That said, server administrators can still take practical steps to mitigate these concerns at the server level.

### 1. Use alternative YouTube frontends

Instead of linking directly to YouTube, administrators can encourage the use of privacy-friendly alternative frontends:

* [**DNT-YT**](https://github.com/gnh1201/dnt-yt?utm_source=gnh1201) (recommended — specifically designed for this scenario)
* [Piped](https://github.com/TeamPiped/Piped?utm_source=gnh1201)
* [Invidious](https://github.com/iv-org/invidious?utm_source=gnh1201)

These frontends help reduce or eliminate tracking while preserving access to video content.

### 2. Rewrite links using Nginx `sub_filter`

After setting up an alternative frontend, YouTube links can be rewritten transparently using Nginx’s **`sub_filter`** feature. This prevents users from accessing the original YouTube URLs directly and redirects them to the alternative frontend instead.

Example configuration:

```
sub_filter 'www.youtube.com/' 'dnt-yt.catswords.net/';
sub_filter 'youtube.com/' 'dnt-yt.catswords.net/';
sub_filter 'www.youtu.be/' 'dnt-yt.catswords.net/';
sub_filter 'youtu.be/' 'dnt-yt.catswords.net/';
```

### Result

Once you confirm that links to `youtube.com` or `youtu.be` are consistently replaced with links to the alternative frontend, the configuration is complete.

A real-world example of this approach can be seen here:

[https://catswords.social/@gnh1201/115801692643125819](https://catswords.social/@gnh1201/115801692643125819?utm_source=gnh1201)
