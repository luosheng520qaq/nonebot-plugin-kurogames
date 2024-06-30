<div align="center">
  <a href="https://v2.nonebot.dev/store"><img src="https://github.com/A-kirami/nonebot-plugin-template/blob/resources/nbp_logo.png" width="180" height="180" alt="NoneBotPluginLogo"></a>
  <br>
  <p><img src="https://github.com/A-kirami/nonebot-plugin-template/blob/resources/NoneBotPlugin.svg" width="240" alt="NoneBotPluginText"></p>
</div>

<div align="center">

# nonebot-plugin-kurogames

_✨ 一款库洛游戏数据详情 谢比螺六~ ✨_


<a href="./LICENSE">
    <img src="https://img.shields.io/github/license/ConcyWee/nonebot-plugin-kurogames.svg" alt="license">
</a>
<a href="https://pypi.python.org/pypi/nonebot-plugin-kurogames">
    <img src="https://img.shields.io/pypi/v/nonebot-plugin-kurogames.svg" alt="pypi">
</a>
<img src="https://img.shields.io/badge/python-3.8+-blue.svg" alt="python">

</div>

## 📖 介绍

输入命令即可查询库洛游戏数据详情  
所需的token须为库街区app获取，网页的token不可以哦~  
可以用抓包软件抓取sdkLogin的包，具体获取方法请参考文档：https://docs.qq.com/doc/DZW9SQ294SnhlbkFw  
token格式如下所示
![image](https://github.com/ConcyWee/nonebot-plugin-kurogames/assets/36001297/1fc32ace-cca4-4ddc-bda4-7ed4f9054848)

## ❗ 宇宙安全声明

本插件仅提供库洛游戏的账号数据查询，并不会保存您的用户名和密码，但会保存获取到的账号 token! 如果您的账号出现封禁, 被盗等处罚与本插件无关. 使用即视为您阅读并同意以上条款!

## 💿 安装

<details open>
<summary>使用 nb-cli 安装</summary>
在 nonebot2 项目的根目录下打开命令行, 输入以下指令即可安装

    nb plugin install nonebot-plugin-kurogames

</details>

<details>
<summary>使用包管理器安装</summary>
在 nonebot2 项目的插件目录下, 打开命令行, 根据你使用的包管理器, 输入相应的安装命令

<details>
<summary>pip</summary>

    pip install nonebot-plugin-kurogames
</details>
<details>
<summary>pdm</summary>

    pdm add nonebot-plugin-kurogames
</details>
<details>
<summary>poetry</summary>

    poetry add nonebot-plugin-kurogames
</details>
<details>
<summary>conda</summary>

    conda install nonebot-plugin-kurogames
</details>

打开 nonebot2 项目根目录下的 `pyproject.toml` 文件, 在 `[tool.nonebot]` 部分追加写入

    plugins = ["nonebot_plugin_kurogames"]

</details>

## ⚙️ 配置

插件中包含playwright，首次使用可能需手动执行 playwright install
| 配置项 | 必填 | 说明 |
|:-----:|:----:|:----:|
| kuro_db_path | 否 | 配置数据库路径，例如 "D:\kurogames"(如不填写则默认保存位置为/data/kurogames) |

## 📝 画饼

- [x] 增加鸣潮游戏详情查询
- [x] 增加短信登录功能
- [x] 库街区签到
- [x] 增加鸣潮查询指定人的数据
- [ ] 增加鸣潮抽卡数据分析(完成了一半，现在只有数据详情，没有欧非判定）
- [ ] 自定义背景图片
- [ ] 战双血清回满提前提醒



## 🎉 使用

### 指令表

| 指令 | 权限 | 需要@ | 范围 | 说明 |
|:-----:|:----:|:----:|:----:|:----:|
| 库洛登录 token | 群员 | 否 | 群聊 | 登录库街区账号 |
| 库洛登录 验证码 | 群员 | 否 | 群聊 | 登录库街区账号 |
| 库洛签到 | 群员 | 否 | 群聊 | 完成库街区每日任务以及游戏签到 |
| 战双数据 | 群员 | 否 | 群聊 | 获取战双当前数据 |
| 鸣潮数据 | 群员 | 否 | 群聊 | 获取鸣潮当前数据 |
| 库洛帮助 | 群员 | 否 | 群聊 | 查看本插件使用帮助 |

### 效果图

#### 战双：
<details>
  
![IMG_20240610_204654](https://github.com/ConcyWee/nonebot-plugin-kurogames/assets/36001297/91b9203c-18a4-4e65-bd29-dde8ff901356)

![IMG_20240510_185200](https://github.com/ConcyWee/nonebot-plugin-kurogames/assets/36001297/0ad515f3-cfc2-4ab6-a433-3056c944d754)

</details>

#### 鸣潮：
<details>
  
![IMG_20240610_204714](https://github.com/ConcyWee/nonebot-plugin-kurogames/assets/36001297/b31ed2c7-f8d7-4721-8da3-220b03bf9c90)

![1717680630759](https://github.com/ConcyWee/nonebot-plugin-kurogames/assets/36001297/ae3c91f5-a87f-4521-9ada-ea804d9834df)

</details>

## 🦜 更新日志

### 2024.06.30
- 修复鸣潮抽卡数据分析功能，在重复抽取时，数据不准确的问题

### 2024.06.29
- 修复角色“今汐”排版异常的问题（沟槽的库洛图片大小不统一😡👊）
- 修复发送“鸣潮抽卡详情”指令后查询鸣潮数据出现“还没有设置鸣潮角色”的问题

### 2024.06.16
- 新增查询指定人的鸣潮数据
- 新增抽卡数据查询

### 2024.06.10

- 新增短信登录功能
- 新增库街区签到功能

### 2024.06.07

- 修复无游戏角色时崩溃的bug
- 增加鸣潮体力回满时间

### 2024.06.06

- 增加鸣潮数据查询
