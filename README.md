# 预览：

<p align="center"><img src="./assets/3.png"></p>

# 项目介绍

# <p align="center">证件照伴侣</p>
<p align="center">我给你的，就是我想要的，我爱你的方式，就是我希望被爱的方式.</p>
<p align="center"><img src="./assets/1.png"></p>

[//]: # (<p align="center">喜欢就点个Star吧</p>)



**相关项目**：

- 小程序前端请前往：https://github.com/no1xuan/photo

------

#  📦前提准备

本项目基于HivisionIDPhotos的2024.09.10更新的版本进行对接开发

理论HivisionIDPhotos不改变入参和返回，即可直接使用最新版

1. 2024.09.10的HivisionIDPhotos（以内置MTCNN+hivision_modnet模型）下载：https://wwba.lanzouq.com/it7LW29ue8yd

2. 鉴黄APi端下载：https://github.com/no1xuan/zjzNsfw

注意:

1. **鉴黄模型目前不怎么精准，建议在小程序过审时打开，其它时间关闭**
2. **需要在HivisionIDPhotos源码的deploy_api.py第23行加入"data:image/png;base64,"+**

<img src="./assets/9.png">









# 🤩功能

##### 现有功能：

- 无需单独购买API
- 本地0成本处理
- 无限免费调用API
- 不保存用户图片，仅保存生成后的最新一张
- 支持水印
- 支持自由开关鉴黄
- 自带758+尺寸
- 支持自定义尺寸
- 支持自定义更换背景色
- 支持普通下载和高清下载
- 支持引导用户打开保存相册
- 支持相机拍摄和相册选择



##### 内测功能列表：

- 14种衣服自由换装
- 更换最新HivisionIDPhotos模型
- 物品自定义抠图
- 黑白图片上色
- 粘土风写真生成
- 新版本个人中心
- 无感登录



##### 排期功能列表：

- 下载接入流量主（暂时没找到开发文档）
- 管理员的后台管理







# 🔧部署

需要：

1. jdk1.8+mysql8.0+redis7.2.4（mysql5.7理论也行）

2. Mysql导入1.sql，然后打开web_set表，把app_id，app_secret配置了，至此Mysql配置完毕

3. IDEA导入项目，打开application.yml，按下图进行一步步配置
<p></p>

##### 修改Redis：

<img src="./assets/5.png">





##### 修改Mysql：

<img src="./assets/6.png">





##### 修改图片存储地址：

<img src="./assets/7.png">

解释：

你需要一个新建一个静态网站，将目录指定：/www/wwwroot/zjzpic/pic

然后，开启https（因为小程序内下载链接只能https请求）并把域名换成你的







##### 修改API接口地址：

<img src="./assets/8.png">

换成你的APi地址即可，然后就可以打包了

如果不想部署API，可以使用我的：

鉴黄APi：http://121.62.63.137:3006/

证件照APi:  http://121.62.63.137:8199/

[README.md](..%2F..%2F..%2FPictures%2F%D0%C2%BD%A8%CE%C4%BC%FE%BC%D0%2FHivisionIDPhotos-master%2FREADME.md)

## ⚡️注意

1. 本项目使用IDEA打包后，会自动把打包后的jar包放入D:\jar2
2. 鉴黄模型目前不怎么精准，建议在小程序过审时打开，其它时间关闭
3. 部署自已鉴黄和证件照APi时，不建议开设外网，防止被抓接口后滥用，yml里面配置127.0.0.1即可本地链接，速度还快，还安全
4. 为什么不把APi地址等参数放入数据库来配置？答：频繁使用的值，不建议与Mysql频繁握手
5. 当你部署到云上（服务器）时，别忘记配置你的小程序域名(如图) <p></p> <img src="./assets/11.png">



## 📧其它

您可以通过以下方式联系我:

QQ: 24677102

微信：webxuan