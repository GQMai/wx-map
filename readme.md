# 福田区附近的幼儿园
根据深圳教育2024年福田区幼儿园名单制作了一个简单的幼儿园地图。

数据来源：https://www.szftedu.cn/gk/xxxx/202302/t20230203_143313.html

2024年福田区幼儿园名单：https://www.szftedu.cn/gk/xxxx/202302/P020240402526108008524.pdf

## 项目介绍
基于微信LBS小程序模板制作

## 部署步骤
- 在左上角点击【云开发】按钮，进入云开发控制台。
- 如果没有环境则按照提示开通云开发环境
- 进入云开发环境，在【设置】页复制`环境ID`
- 前往[腾讯地图控制台](https://lbs.qq.com/dev/console/application/mine)，参照此[文档](https://lbs.qq.com/service/webService/webServiceGuide/webServiceGcoder)申请key
- 将申请的key，填写到 `cloudfunctions/lbs_server/config.json` 文件的 `key` 字段中。
- 右键点击 `cloudfunctions/lbs_server` 文件夹，选择云函数云端安装依赖上传
- 如果在新建项目时，小程序下有云开发环境，则会默认注入第一个环境，如果想更换为自己想要的环境，只需要将 `miniprogram/envList.js` 文件里的内容全部替换成如下，注意替换envId
``` js
module.exports = {
  envList: [{
    envId:'上述步骤中你获得的环境ID'
  }]
}
```
