<p align="center">
<img width="500" src="https://cdn.jsdelivr.net/gh/teamssix/BlogImages/imgs/202207022209168.png"><br><br>
<a href="https://github.com/teamssix/cf/stargazers"><img alt="GitHub stars" src="https://img.shields.io/github/stars/teamssix/cf"/></a>
<a href="https://github.com/teamssix/cf/releases"><img alt="GitHub issues" src="https://img.shields.io/github/release/teamssix/cf"/></a>
<a href="https://github.com/teamssix/cf/blob/main/LICENSE"><img alt="License" src="https://img.shields.io/badge/License-Apache%202.0-blue.svg"/></a>
<a href="https://github.com/teamssix/cf/releases"><img alt="Downloads" src="https://img.shields.io/github/downloads/teamssix/cf/total?color=brightgreen"/></a>
<a href="https://goreportcard.com/report/github.com/teamssix/cf"><img alt="Go Report Card" src="https://goreportcard.com/badge/github.com/teamssix/cf"/></a>
<a href="https://twitter.com/intent/tweet/?text=CF%2C%20an%20amazing%20cloud%20exploitation%20framework%0Ahttps%3A%2F%2Fgithub.com%2Fteamssix%2Fcf%0A%23cloud%20%23security%20%23cloudsecurity%20%23cybersecurtiy"><img alt="tweet" src="https://img.shields.io/twitter/url?url=https://github.com/teamssix/cf" /></a>
<a href="https://twitter.com/teamssix"><img alt="Twitter" src="https://img.shields.io/twitter/follow/teamssix?label=Followers&style=social" /></a>
<a href="https://github.com/teamssix"><img alt="Github" src="https://img.shields.io/github/followers/TeamsSix?style=social" /></a><br></br>
中文 | <a href="README_EN.md">English</a>
</p>



---

CF 是一个云环境利用框架，主要用来方便红队人员在获得云服务的访问凭证即 Access Key 的后续工作。

CF 下载地址：[github.com/teamssix/cf/releases](https://github.com/teamssix/cf/releases)

目前 CF 可以实现以下功能：

* 已实现

  - [x] 列出对象存储（包括存储桶大小和文件数量信息）
  - [x] 列出 ECS 实例
  - [x] 一键获得实例上的临时访问凭证
  - [x] 一键为所有实例执行三要素，方便 HVV
  - [x] 一键为实例反弹 Shell
  - [x] 支持阿里云
  - [x] 列出 RDS 云数据库实例
  - [x] 一键接管控制台
  - [x] 一键查看当前访问凭证所拥有的权限
  - [x] 支持腾讯云
  - [x] ……
  
* 预计实现

  - [ ] 云上痕迹清除
  
  - [ ] 自动检测当前运行环境是不是实例，如果是则一键扫描本地实例的凭证信息
  - [ ] 一键将获取到的临时凭证添加到工具中
  - [ ] 支持其他云厂商
  - [ ] ……

## 使用手册

使用手册请参见：[wiki.teamssix.com/cf](https://wiki.teamssix.com/cf)

[![img](https://cdn.jsdelivr.net/gh/teamssix/BlogImages/imgs/202207112152449.png)](https://wiki.teamssix.com/cf)

## 使用案例

[《我用 CF 打穿了他的云上内网》](https://zone.huoxian.cn/d/1341-cf)

## 简单上手

![](https://cdn.jsdelivr.net/gh/teamssix/BlogImages/imgs/202207180028840.png)

配置 CF

```bash
cf configure
```

一键列出当前访问凭证的云服务资源

```bash
cf alibaba ls
```

一键列出当前访问凭证的权限

```bash
cf alibaba permissions
```

一键接管控制台

```bash
cf alibaba console
```

查看 CF 为实例执行命令的操作的帮助信息

```bash
cf alibaba ecs exec -h
```

一键为所有实例执行三要素，方便 HVV

```
cf alibaba ecs exec -b
```

一键获取实例中的临时访问凭证数据

```bash
cf alibaba ecs exec -m
```

一键查看 VPC 安全组规则

```bash
cf tencent vpc ls
```

如果感觉还不错的话，师傅记得给个 Star 呀 ~，另外 CF 的更多使用方法可以参见使用文档：[wiki.teamssix.com/cf](https://wiki.teamssix.com/cf)

## 贡献者

十分感谢各位师傅对 CF 的贡献~，如果你也想对 CF 贡献代码，请参见贡献说明：[CONTRIBUTING](https://github.com/teamssix/cf/blob/main/CONTRIBUTING.md)

<div align=center>
<table>
    <tr>
        <td align="center"><a href="https://github.com/teamssix"><img alt="TeamsSix"
                                src="https://avatars.githubusercontent.com/u/49087564?v=4" style="width: 100px;"/><br/>TeamsSix</a></td>
        <td align="center"><a href="https://github.com/Amzza0x00"><img alt="Amzza0x00"
                                src="https://avatars.githubusercontent.com/u/32904523?v=4"  style="width: 100px;"/><br/>Amzza0x00</a></td>
        <td align="center"><a href="https://github.com/Esonhugh"><img alt="Esonhugh"
                                src="https://avatars.githubusercontent.com/u/32677240?v=4"  style="width: 100px;"/><br/>Esonhugh</a></td>
        <td align="center"><a href="https://github.com/Dawnnnnnn"><img alt="Dawnnnnnn"
                                src="https://avatars.githubusercontent.com/u/24506421?v=4"  style="width: 100px;"/><br/>Dawnnnnnn</a></td>
        <td align="center"><a href="https://github.com/Belos-pretender"><img alt="Belos-pretender"
                                src="https://avatars.githubusercontent.com/u/52148409?v=4"  style="width: 100px;"/><br/>Belos-pretender</a></td>
</table>
</div>

<div align=center><a href="https://github.com/teamssix"><img src="https://repobeats.axiom.co/api/embed/30b8de6c059cbe83fe0ba44fff91136270a39ab9.svg"></a></div>


## 注意事项

* 本工具仅用于合法合规用途，严禁用于违法违规用途。
* 本工具中所涉及的风险点均属于租户责任，与云厂商无关。

## 更多

如果你对云安全比较感兴趣，可以看我的另外一个项目 [Awesome Cloud Security](https://github.com/teamssix/awesome-cloud-security)，这里收录了很多国内外的云安全资源。

另外在我的[云安全文库](https://wiki.teamssix.com/)里有大量的云安全方向的笔记和文章，最后，下面这个是我的个人微信公众号，欢迎关注 ~

**有想法一起研究的师傅可以投递简历至 admin@wgpsec.org 加入狼组安全团队。**

<div align=center><a href="https://github.com/teamssix"><img width="700" src="https://cdn.jsdelivr.net/gh/teamssix/BlogImages/imgs/202204152148071.png"></a></div>

<div align=center><a href="https://github.com/teamssix"><img src="https://api.star-history.com/svg?repos=teamssix/cf&type=Timeline"></a></div>