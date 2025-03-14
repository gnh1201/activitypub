# gnh1201/activitypub
[![Discord chat](https://img.shields.io/discord/359930650330923008?logo=discord)](https://discord.gg/Q9MWa6bjGP)

My awesome list about ActivityPub and Fediverse

## Projects
* Caterpillar Proxy - The simple and parasitic web proxy with SPAM filter (formerly, php-httpproxy)
  * https://github.com/gnh1201/caterpillar
  * https://github.com/gnh1201/caterpillar/wiki/Fediverse
  * https://qiita.com/gnh1201/items/09f4081f84610db3a9d3 - K-Anonymity for Spam Filtering: Case with Mastodon, and Misskey
* ActivityPub (Fediverse) implementation for GNUBOARD5
  * https://github.com/gnh1201/gnuboard5-activitypub
* How to accelerate video trancoding (FFmpeg) in Mastodon
  * https://gist.github.com/gnh1201/1ba49e0e80a11237038900bf8abfa434
* Simple web API for extracting images/audio from video and converting audio/video/image files with ffmpeg.
  * https://github.com/gnh1201/ffmpeg-api
  * https://github.com/gnh1201/ffmpeg-api/blob/master/technical-notes.md
* Lingva Translate Gateway for Mastodon (LibreTranslate API compatible)
  * https://github.com/gnh1201/mastodon-lingva
* Social on the file - File reputation checker with Social media timeline
  * https://github.com/gnh1201/SocialOnTheFile
* ActivityPub over LoRaWAN (Proposal)

## Servers
* [relay.catswords.net](https://relay.catswords.net/) - ActivityPub Relay Server
* [catswords.social](https://catswords.social) - Mastodon server

## Softwares
* [nginx](https://nginx.org/)
* [Cloudflare WARP (Zero Trust)](https://one.one.one.one/)
  * You can benefit from improved data transfer (federation) speeds between different nodes.
* [Cloudflare Tunnel (Argo Smart Routing)](https://www.cloudflare.com/products/tunnel/)
  * You can benefit from improved data transfer (federation) speeds between different nodes as well as website response speeds.
* [Cloudflare R2](https://www.cloudflare.com/ko-kr/developer-platform/r2/)
  * As an object storage service. In my case, I use it to save and share a server settings (certificates, configuration files, etc.) between my other servers.
* [acme.sh](https://github.com/acmesh-official/acme.sh)
  * SSL certificate issuance
* [Squid Cache](https://www.squid-cache.org/)
  * If you're considering creating a proxy server yourself, you might want to consider squid-cache.
* Private VPN software: [OpenVPN](https://openvpn.net/), [WireGuard](https://www.wireguard.com/), [Shadowsocks](https://shadowsocks.org/), etc.
  * By appropriately utilizing private VPN software, you can configure network structures such as Cloud DMZ that can help in cost-saving.
* [SendGrid](https://sendgrid.com/)
  * Integrate fast and explore features with 100 emails/day forever.
* [Honeypots](honeypots.md)
* [Image stocks](https://policy.catswords.social/stock_images.html)

## Contact me
* ActivityPub [@catswords_oss@catswords.social](https://catswords.social/@catswords_oss)
* abuse@catswords.net
* [Join Catswords on Microsoft Teams](https://teams.live.com/l/community/FEACHncAhq8ldnojAI)
