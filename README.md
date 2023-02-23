<h1 align="center">
<a href="https://JoinBase.io/">JoinBase</a> </h1>

<h3 align="center">
JoinBase, a single binary AIoT-first data-service platform.
</h3>

<br>

<div align="center">

  <a href="">[![Website](https://img.shields.io/badge/https://-joinbase.io-blue.svg)](https://joinbase.io/)</a>

</div>

<div align="center">

  <a href="">![](https://img.shields.io/github/stars/open-joinbase/JoinBase)</a>
  <a href="">![](https://img.shields.io/github/issues/open-joinbase/JoinBase)</a>

</div>

<div align="center">
 
  <a href="">[![Discord Invite](https://img.shields.io/discord/1031840841226002522?logo=discord&labelColor=8b2671)](https://discord.gg/sqX6vfnURj)</a>
  <a href="">[![Slack Invite](https://img.shields.io/badge/Slack-Join-blue?logo=slack&labelColor=8b2671)](https://join.slack.com/t/joinbaseworkspace/shared_invite/zt-1bizmnl2c-HaXl93gZ5Hnm_ukDAotZzg)</a>
  <a href="">[![WeChat Invite](https://img.shields.io/badge/WeChat-07C160?logo=wechat&labelColor=8b2671)](/community/wechat.md)</a>

</div>

# Welcome to JoinBase Community

## Download

From JoinBase 2023.2, the community edition is publicly available.

Get latest releases in the porject's [release page](https://github.com/open-joinbase/JoinBase/releases).

More [installation guide and prerequisites](https://joinbase.io/docs/references/install). 

JoinBase's community edition is provided under the [Commuity Edition License Agreement](https://joinbase.io/community_license): any people and company can use it free both for non-commercial and commercial purposes (including cloud services). 

The community edition has the same functions as the enterprise edition but without HA(High Availability) support. We crush competitors in the edge performance, if you don't require 100% HA, the community edition is enough, even for commercial services. 

### Get JoinBase with Docker

If you prefer the Docker way, try JoinBase with the above simplest command:

```bash
docker run --net=host -P -d joinbase/joinbase
```

This command will start a JoinBase server wiht the default conf in a detached container by exposing all ports to your host.

But **NOTE** that JoinBase has no `default user` concept at all, you should setup a user before going ahead by the following command:

```bash
docker run --net=host --entrypoint /joinbase/base_admin -it joinbase/joinbase create_user abc
```

Just check the server by pinging with curl, like:
```bash
curl -v -s -H 'X-JoinBase-User: abc' -H 'X-JoinBase-Key: abc' -X GET 'http://127.0.0.1:8080/ping'
```

Finally, note that all data and change are inside of the container for above quick commands. They may disappear when that container ternimated. For production use, you should customize JoinBase's conf to use dedicated directories. A sample conf file named "base.conf" is provided with every release. Just dowload and customize it yourself.


## Release Notes

New version of the community edition is released in a time rhythm, and the version number of the community edition is based on that time rhythm. Currently the release cycle is one month.

It is recommended that users always use the latest release. Version compatibility will be maintained as much as possible. In JoinBase, the version compatibility means: users only need to simply replace the binary and restart to complete the upgrade. If one release is incompatible with the previous version, it will be declared in that release note and a solution will be provided.

## :revolving_hearts: Watch our community :revolving_hearts:

Appreciated if you can watch our community.

![Watch our community](https://user-images.githubusercontent.com/79301703/182365526-df074c64-cee4-45f6-b8e0-b912f17332c6.gif)
