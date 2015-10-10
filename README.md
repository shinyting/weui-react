# weui-react


weui 为微信 Web 服务量身设计
概述

WeUI是一套同微信原生视觉体验一致的基础样式库，为微信 Web 开发量身设计，可以令用户的使用感知更加统一。包含button、cell、dialog、toast、article、icon等各式元素。

https://github.com/weui/weui


## 组件(todo)

- Button
- Cell
- Dialog
- Toast
- Msg Page
- Article
- Icon

## 实现

根据https://github.com/weui/weui里的描述，封装成对应的reactjs component

比如dialog

```
<div class="weui_dialog_confirm">
    <div class="weui_mask"></div>
    <div class="weui_dialog">
        <div class="weui_dialog_hd"><strong class="weui_dialog_title">弹窗标题</strong></div>
        <div class="weui_dialog_bd">自定义弹窗内容<br>...</div>
        <div class="weui_dialog_ft">
            <a href="javascript:;" class="weui_btn_dialog default">取消</a>
            <a href="javascript:;" class="weui_btn_dialog primary">确定</a>
        </div>
    </div>
</div>
```

转成reactjs组件

```
var weui        = require('weui-react');
var WDialog     = weui.W-Dialog;
var DialogFoot  = W-Dialog.W-Dialog-Foot;

function cancel_click_cb(e){

}

function sucess_click_cb(e){

}

<WDialog title="弹窗标题">
  自定义弹窗内容
  <Dialog-Foot title="取消" onClick={cancel_click_cb} />
  <Dialog-Foot title="确定" onClick={sucess_click_cb} />
</W-Dialog>
```

