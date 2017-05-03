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
---

### 引导功能
引导的关键字是  `guide` , 它是一个json 数组 , 使用 `[ ]` 框起来
数组的每一项, 是一个json格式的数据 , 使用 `{}` 框起来
```json
 // 首次进入的引导,使其进入应用主页
  "guide": [
    {
      "action": "slideHori",
      "xpath": "//*[@resource-id='com.m4399.gamecenter.plugin.main:id/tv_enter_right_now']"
    },
    {
      "action": "check",
      "xpath": "//*[@resource-id='com.m4399.gamecenter.plugin.main:id/iv_tab_icon']"
    }
  ]
```
除了上诉示例中,提到的 `action`,`xpath` 关键字外,还有 `hint`,`value`,`loopTimes`,`timeSpacing`,`errorMessage`,`enableAlter`

#### 字段详解

>  这些关键字只适用于 配置中的用例,不适用于 程序的默认遍历

参数名 | 类型 | 说明 | 备注
---|---|---|---
**action** | 字符串 | 动作类型 (必填) | 目前支持 `click`,`input`,`slide`,`slideHori`,`check`五种类型 <br /> 详情见下一张表格
**xpath** | 字符串 | 控件的唯一路径标识(必填) | 需要遵循 XML 中的 XPath 语法 <br /> 该路径出错则元素无法找到
**hint** | 字符串 | 输入框的提示语 | (只用于input类型)用于判断 输入框是否已经被清空
**value** | 字符串 | 输入的文字内容 | (只用于input类型)
**loopTimes** | 整型 | 寻找控件的循环次数 | 未填写,则默认值1
**timeSpacing** | 整型 | (单位毫秒) 找寻控件的间隔时间 | 需要配合 **loopTimes**使用
**enableAlter** | 布尔值 | 允许配置路径,自己处理对话框 | true : 表示配置自己处理
**errorMessage** | 字符串 | 当路径出错时,自定义的提示语

---

**action**字段详解 :

类型 | 说明 |备注
---|---|---
**click** | 点击操作 | 需要配置 `xpath`
**input** | 输入操作 | 需要配置 `xpath`,`hint` ,`value`
**slide** | 滑动 (上下滑动寻找控件) | 需要配置 `xpath` <br /> `loopTimes` 在这个动作下表示滑动次数
**slideHori** | 左右滑动 | 需要配置 `xpath` <br /> `loopTimes` 在这个动作下表示滑动次数
**check** | 检查 | 需要配置 `xpath`  <br /> 表示控件是否存在,存在返回真,不存在返回假<br /> `errorMessage`在此类型下无效

> *注释* : `guide` 配置,需要在最后一项, 使用 `check` 类型, 检查的元素是跳过引导页之后的首页元素,
> 
> 这么做是因为 非首次进入应用,是不需要做引导操作 , 即检测到首页元素,则不再进行引导操作

---

### 登录功能

登录功能包含三个关键字 `login` (登录),`loginCheck`(登录检查),`logout`(注销)

登录逻辑 :
1. 先 `loginCheck` 检查用户是否登录
2. 用户已经登录,则 `logout` 注销 , 注销后 `login` 登录到指定账号
3. 用户未登录,则 直接 `login` 登录到指定账号

三个关键字的结构都一样, 外层是一个 json数组 `[ ]`,每一个子项的操作是一个json格式 `{ }`
```json
  "logout / login / loginCheck": [
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
  ]
```
**每个操作的关键字与 上述 引导 `guide` 类型的操作一致**

> *注释* :  `loginCheck` 关键字,最后一项,是查查登录后的某个ID,是否存在,
> 
> 存在,则表示已经登录了; 不存在,表示还未登录,
>
> 所以  `loginCheck` 的最后一项 应该为 `check` 类型

---

### 对话框处理

