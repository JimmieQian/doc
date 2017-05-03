---
title: 自动化遍历配置接口文档
tags: appium,json
---

## 配置示例
```json
{
  "duration": 60,
  "timeout": 3,
  "interval": 10,
  "packageName": "com.m4399.youpai",
  "launchActivity": "com.m4399.youpai.controllers.launch.LaunchActivity",
  "apkPath": "H:\\workspace\\testHome\\m4399-ui-traverse\\m4399.youpai.apk",
  "capability": {
    "autoLaunch": "true",
    "noReset": "false",
    "unicodeKeyboard": "true",
    "resetKeyboard": "true",
    "noSign": "true"
  },
  "guide": [
    {
      "action": "slideHori",
      "xpath": "//*[@resource-id='com.m4399.gamecenter.plugin.main:id/tv_enter_right_now']"
    },
    {
      "action": "check",
      "xpath": "//*[@resource-id='com.m4399.gamecenter.plugin.main:id/iv_tab_icon']"
    }
  ],
  "login": [
    {
      "action": "click",
      "xpath": "//*[@resource-id='com.m4399.youpai:id/btn_mine']",
      "value": ""
    },
    {
      "action": "click",
      "xpath": "//*[@resource-id='com.m4399.youpai:id/rlBefore']"
    },
    {
      "action": "input",
      "xpath": "//android.widget.EditText[@index='0']",
      "value": "sdktest000",
      "hint": "请输入4399用户名"
    },
    {
      "action": "input",
      "xpath": "//android.widget.EditText[@index='1']",
      "value": "111111"
    },
    {
      "action": "click",
      "xpath": "//android.widget.Button[@content-desc='登 录']"
    }
  ],
  "loginCheck": [
    {
      "action": "click",
      "xpath": "//*[@resource-id='com.m4399.youpai:id/btn_mine']"
    },
    {
      "action": "check",
      "xpath": "//*[@resource-id='com.m4399.youpai:id/tv_uesrName']"
    }
  ],
  "logout": [
    {
      "action": "click",
      "xpath": "//*[@resource-id='com.m4399.youpai:id/btn_mine']"
    },
    {
      "action": "slide",
      "xpath": "//*[@resource-id='com.m4399.youpai:id/btn_setting']"
    },
    {
      "action": "click",
      "xpath": "//*[@resource-id='com.m4399.youpai:id/bt_out']"
    }
  ],
  "alter": [
    "//*[@resource-id='com.m4399.youpai:id/btn_close_guide' and @class='android.widget.Button']",
    "//*[@resource-id='com.m4399.youpai:id/btn_close' and @class='android.widget.Button']",
    "//*[@resource-id='com.m4399.youpai:id/btn_cancel' and @class='android.widget.Button']",
    "//*[@resource-id='com.m4399.youpai:id/tv_close' and @class='android.widget.ImageButton']"
  ],
  "permissionAlter": [
    "//*[@resource-id='com.android.packageinstaller:id/permission_allow_button' and @text='允许']",
    "//*[@resource-id='com.huawei.systemmanager:id/btn_allow' and @text='允许']"
  ],
  "black": [
    {
      "class": "android.widget.RelativeLayout",
      "id": "com.m4399.youpai:id/rl_take_photo",
      "text": ""
    },
    {
      "class": "android.widget.ImageButton",
      "id": "com.m4399.youpai:id/btn_back"
    },
    {
      "class": "android.widget.EditText"
    }
  ],
  "uselessActivity": [
    "com.m4399.youpai.controllers.launch.LaunchActivity",
    "com.m4399.youpai.controllers.mine.SettingGuideActivity",
    "com.youpai.media.live.player.LivePlayerCheckActivity",
    "com.m4399.youpai.controllers.live.LiveInfoActivity",
    "com.youpai.media.hxchat.LiveLoginActivity",
    "com.m4399.youpai.controllers.personal.ClipActivity",
    "com.m4399.youpai.controllers.discover.RankActivity",
    "com.m4399.youpai.controllers.hotrecommend.NewUploadActivity",
    "com.igexin.sdk.PushActivity",
    "com.igexin.sdk.GActivity",
    "com.igexin.getuiext.activity.GetuiExtActivity",
    "com.tencent.tauth.AuthActivity",
    "com.tencent.connect.common.AssistActivity",
    "com.alibaba.sdk.android.feedback.windvane.CustomHybirdActivity",
    "com.alibaba.sdk.android.feedback.impl.ErrorPageActivity",
    "com.umeng.socialize.view.ShareActivity",
    "cn.m4399.operate.controller.OpeHostActivity",
    "com.m4399.youpai.wxapi.WXEntryActivity"
  ],
  "before": [
    {
      "chain": [
        {
          "action": "click",
          "xpath": "//*[@resource-id='com.m4399.youpai:id/tv_mine']",
          "loopTimes": 5,
          "timeSpacing": 1000,
          "errorMessage": "点击我的"
        },
        {
          "action": "click",
          "xpath": "//*[@resource-id='com.m4399.youpai:id/tv_upload']",
          "errorMessage": "点击我的视频"
        },
        {
          "action": "click",
          "xpath": "//*[@resource-id='com.m4399.youpai:id/rl_to_select_local_video']",
          "errorMessage": "选择上传视频"
        },
        {
          "action": "click",
          "xpath": "//*[@resource-id='com.m4399.youpai:id/chkBox' and @index='1' ]",
          "errorMessage": "选择视频"
        },
        {
          "action": "click",
          "xpath": "//*[@resource-id='com.m4399.youpai:id/btn_next' and @text ='下一步']",
          "errorMessage": "点击下一步"
        },
        {
          "action": "input",
          "xpath": "//*[@resource-id='com.m4399.youpai:id/rl_video_title' ]",
          "value": "youpai123",
          "errorMessage": "输入视频标题"
        },
        {
          "action": "click",
          "xpath": "//*[@resource-id='com.m4399.youpai:id/tv_game_category_mobile']",
          "errorMessage": "选择视频分类"
        },
        {
          "action": "input",
          "xpath": "//*[@resource-id='com.m4399.youpai:id/et_game_name' ]",
          "value": "王者荣耀",
          "errorMessage": "选择游戏名称 : 王者荣耀"
        },
        {
          "action": "click",
          "xpath": "//*[@resource-id='com.m4399.youpai:id/tv_search' ]",
          "errorMessage": "点击搜索"
        },
        {
          "action": "click",
          "xpath": "//*[@resource-id='com.m4399.youpai:id/tv_game_name' ]",
          "errorMessage": "点击王者荣耀"
        },
        {
          "action": "click",
          "xpath": "//*[@resource-id='com.m4399.youpai:id/btn_upload_video' ]",
          "errorMessage": "点击立即上传"
        }
      ],
      "reEnter": [
        {
          "action": "click",
          "xpath": "//*[@resource-id='com.m4399.youpai:id/tv_mine']",
          "loopTimes": 5,
          "timeSpacing": 1000,
          "errorMessage": "点击我的"
        },
        {
          "action": "click",
          "xpath": "//*[@resource-id='com.m4399.youpai:id/tv_upload']",
          "errorMessage": "点击我的视频"
        },
        {
          "action": "click",
          "xpath": "//*[@resource-id='com.m4399.youpai:id/rl_to_select_local_video']",
          "errorMessage": "选择上传视频"
        },
        {
          "action": "click",
          "xpath": "//*[@resource-id='com.m4399.youpai:id/chkBox' and @index='1' ]",
          "errorMessage": "选择视频"
        },
        {
          "action": "click",
          "xpath": "//*[@resource-id='com.m4399.youpai:id/btn_next' and @text ='下一步']",
          "errorMessage": "点击下一步"
        },
        {
          "action": "input",
          "xpath": "//*[@resource-id='com.m4399.youpai:id/rl_video_title' ]",
          "value": "youpai123",
          "errorMessage": "输入视频标题"
        },
        {
          "action": "click",
          "xpath": "//*[@resource-id='com.m4399.youpai:id/tv_game_category_mobile']",
          "errorMessage": "选择视频分类"
        },
        {
          "action": "input",
          "xpath": "//*[@resource-id='com.m4399.youpai:id/et_game_name' ]",
          "value": "王者荣耀",
          "errorMessage": "选择游戏名称 : 王者荣耀"
        },
        {
          "action": "click",
          "xpath": "//*[@resource-id='com.m4399.youpai:id/tv_search' ]",
          "errorMessage": "点击搜索"
        },
        {
          "action": "click",
          "xpath": "//*[@resource-id='com.m4399.youpai:id/tv_game_name' ]",
          "errorMessage": "点击王者荣耀"
        },
        {
          "action": "click",
          "xpath": "//*[@resource-id='com.m4399.youpai:id/btn_upload_video' ]",
          "errorMessage": "点击立即上传"
        }
      ],
      "needFinish": true
    }
  ]
}
```

## 字段详解

--- 

### 非功能字段

参数名 | 类型 | 说明 | 备注
-- | -- | -- | --
**apkPath** | 字符串 |  被测apk在本地的路径 | (必填) 该值未填或者填错,程序直接报错,包的路径是一切的开始
**packageName** | 字符串 | 被测应用的包名 | (选填) 该值未填,则不会检测手机上是否安装被测应用,会直接安装传入的apk路径包
**launchActivity** | 字符串 | 被测应用的入口activity名 | (选填)  该值未填,则不会检测手机上是否安装被测应用,会直接安装传入的apk路径包
**capability** | map | appium服务关键字 | (选填) 支持所有的appium服务关键字 [Appium 服务关键字](http://appium.io/slate/cn/master/?ruby#appium-服务关键字)

### 全局字段
参数名 | 类型 | 说明 | 备注
-- | -- | -- | --
**duration** | 整型 | (单位秒) 遍历的最长时间 (建议设置大于5分钟) | (选填) 时间从appium与手机建立起连接时开始算起,<br >如果未填,默认不限制时间,这个时间存在误差(+60s);
**timeout** | 整型 | (单位秒) appium服务找寻控件的最长时间 | (选填) 不填时,默认3秒
**interval** | 整型 | (单位秒) 每次操作的间隔(等待)时间 | (选填) 不填时,默认3秒

### 引导功能
引导的关键字是 ==guide== , 它是一个json 数组 , 使用 `[ ]` 框起来
数组的每一项, 是一个json格式的数据 , 使用 `{}` 框起来
