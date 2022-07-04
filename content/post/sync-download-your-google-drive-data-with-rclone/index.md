---
title: "rclone: Download your Google Drive data easily"
subtitle: "rclone: 如何輕易下載Google Drive資料"
date: 2022-07-06T08:28:18.904Z
draft: false
featured: false
tags:
  - cloud
  - drive
  - rclone
categories:
  - Guide
image:
  filename: logo_on_light__horizontal_color.svg
  focal_point: Smart
  preview_only: false
---
Starting this July, Google is going to change their storage policy for educational organisations, and many of these organisations are starting to limit their users in terms of individual storage space.

> **Google Workspace for Education 縮減儲存空間**
>
> Google的新政策將於今年7月生效，僅提供各機構 100TB 的儲存空間。
> Link: <https://support.google.com/a/answer/10431555?hl=zh-Hant>
>
> ![](storage-policy.png)

I supposed many are looking to download/sync their data to prevent data losses. But manual download from the browser is going to be so tedious.

Luckily, there are tools available to help: 
For lite users, using Google Takeout ([https://takeout.google.com/](https://takeout.google.com/)) would be quick and easy. But for a heavy user like me (a few TB across multiple accounts), there is a much better tool -**rclone**- which is more powerful and flexible.

**rclone** is a feature-rich cloud storage manager. It supports many cloud storage providers such as (Google Drive, Dropbox, OneDrive, Nextcloud and more).


## Table of contents
1. Setting up rclone:
    * Adding a remote cloud
    * Advance setup: create your own Google App ClientID
2. Downloading your data: 
    * *ls/lsd*  - list object and directories
    * *ncdu*    - interactive disk usage
    * *copy*
    * *sync*
3. Advanced usage:
    * *dedupe*
    * *mount*
    * *sync* between 2 cloud drives
---
## Setting up rclone:
### Installation
For Ubuntu, simply:
    
    ```bash
    sudo apt install rclone
    ```
> For Windows, just download the exe from <https://rclone.org/downloads/> and use
> it in CMD. (You need to be in the rclone folder to use *rclone* command).

### Adding a remote cloud

    ```bash
    rclone config
    ```
