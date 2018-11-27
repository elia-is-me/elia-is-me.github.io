---
title: 如何使用 foobar2000 管理你的音乐？
date: 2018年11月28日
categories: [foobar2000]
tags: [foobar2000]
---

## 一、管理起你所有的音乐文件

foobar2k 可以将你的音乐文件很好地组织起来，然后就可以通过不同的方式浏览你的音乐文件了，比如可以通过 Library > Search 直接搜索，也可以通过 Library > Album List 来查看你有哪些专辑、歌手等等。

<!--more--->

首先得告诉 foobar2k 你音乐文件存在哪里，为此需要添加你音乐文件所在的文件夹：

![]( https://pic3.zhimg.com/80/v2-9227bf981fea0402e3eb4bebc936a256_hd.jpg)


foobar2k 会自动监控这些文件夹（看到 Monitoring 了没），音乐文件如果有增加、删减之类的操作它都会自动更新。

> iTunes 也有媒体库功能，然而却不能自动监控增删，添加音乐还好办，手动一下也不太费事，但已经删除了的它却不能自动从音乐库中给你去掉，这个就很烦恼了，有时候直到双击播放才知道歌已经没了。不过 iTunes 的音乐库功能也很强大。

>Groove 播放器，MusicBee 还有上面的 iTunes 都有音乐库功能，并且还可以自动从在线数据库中同步歌曲、专辑及歌手的各种信息。有些事情未必就要强求 foobar2k 去做……


## 二、探索 foobar2k 的搜索功能

foobar2k 的搜索功能很强大，不过不太好用（因为复杂）。通过菜单 Library > Search 和 Library > Album List 都可以。至于怎么用，恐怕要好好读读帮助文件了……

![](https://pic3.zhimg.com/80/v2-477702f64eb6d3fc4e4315cc77c08066_hd.jpg)

这里举几个例子：

- 艺人叫“梶浦由记”的所有歌曲：`%artist% IS 梶浦由記`
- 所有五星评级歌曲：`%rating% IS 5` (评级需要安装 Playback Statistics 插件，下面几条也是）
- 最近一周新加的歌曲：`%added% DURING LAST 1 WEEK`
- 最近播放的歌曲：`%last_played% DURING LAST 1 WEEK`
- 从没播放过的：`%play_count% IS 0`

这些搜索条件还可以通过 `AND`、`OR` 组合起来，也可以用 `NOT` 取反比如：

- 艺人不叫“梶浦由记”的：`NOT %artist% IS 梶浦由记`
- 最近一周新加的并且最近一周播放的：`%added% DURING LAST 1 WEEK AND %last_played% DURING LAST 1 WEEK`

还可以排序搜索结果：

- `%artist% IS 梶浦由記 SORT DESCENDING BY %last_played%`

有的搜索条件很常用到，不想每次都输入的，可以保存成 AutoPlaylist，（默认会保存成 New Playlist，重命名个好记的……）：

![](https://pic2.zhimg.com/80/v2-c021b5994e391f8184bacb96e62db48d_hd.jpg)

也可以重新修改搜索条件，菜单 View > Playlist manager 打开播放列表管理，如果是智能列表的话右键菜单会多出 Autoplaylist... ：


![](https://pic2.zhimg.com/80/v2-2d177c4c2cd7e0d2841ce62713eca925_hd.jpg)

## 三、增强播放列表的体验

建立播放列表各人有各人的风格，有人喜欢国产软件的双击添加到列表；有人会像网易云那样精选出少而精致的歌单；也有人很随意，拖几个一眼捕捉到的到播放列表里（本人第三种），这些都是各人的偏好，无所谓好坏。

但 foobar2k 的播放列表有个缺点就是太容易被修改，不小心添加一首歌，删除一首歌；有时候还会不小心直接删了全部…… 如果是精选歌单的话就有点伤了。这里介绍俩插件：

- [Playlist Attributes]( https://link.zhihu.com/?target=http%3A//www.foobar2000.com/components/view/foo_playlist_attributes) ：这个插件可以更细致地制定播放列表属性，可以限制播放列表不能修改，不能重命名，不能删除等等；
- [Playlist Revive](https://link.zhihu.com/?target=https%3A//hydrogenaud.io/index.php/topic%2C73910.0.html): 有时候你移动了你的歌曲文件，然后播放列表里对应的歌曲就不能播放了…… 这个插件可以搜索媒体库里对应的符合要求的歌曲文件，然后“修复”你的列表，如果常常整理文件夹的话这个插件会很有用。
