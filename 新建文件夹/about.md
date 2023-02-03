# 老佛爷小程序发布文档


## 微信开发者工具

1. 打开微信开发者工具 - 选择本地小程序路径
2. 拉取最新代码
    - git status  查看状态
    - Git reset --hard  --代码重置
    - Git pull     ---代码拉取
3. 代码拉取后，点击上传，修改版本号和修改内容

## 微信开放平台
登录地址 [微信开放平台](https://open.weixin.qq.com/).  
1. 打开微信开放平台，点击第三方平台，点击创思感知应用品平台的详情按钮  
!["微信开放平台"](/imgs/微信开放平台.png)  
2. 点击代开发小程序，可以看到上传的版本，点击添加到模板库（普通模板库）  
!["代开发"](/imgs/代开发小程序.png) 
3. 点击模板库查看，版本号、templateID  
!["代开发"](/imgs/模板库.png) 

## VScode工具
1. 打开vscode，点击左侧远程图标，链接服务器：139.224.23.171，打开文件夹：mnt/  
!["代开发"](/imgs/服务器.png)   
!["代开发"](/imgs/连接.png)  


* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.
