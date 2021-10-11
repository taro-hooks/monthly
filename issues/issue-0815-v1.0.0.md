
<div align="center"><img width="150" src="https://cdn.jsdelivr.net/gh/innocces/DrawingBed/2021-8-16/1629044969573-hook.png" /></div>

## Taro-hooks V1.0 🎉
`taro-hooks` 是一个将`taro api`以`hooks`的形式改写的工具库。仅可在`React`中使用。    
在`v1.0`版本中, 主要实现了35个`hook`。    
部分`api`被合并, 故覆盖率还是很高的。其中还整合了`ahooks`中的`useRequest`, 使其更加适配`taro`。   
以及`api`的`Promise`化。并且部分`h5`不支持的`api`也做了一定的补齐。大家详情可以查看[`taro-hooks`官网](https://taro-hooks.vercel.app)

## 作用
可以称之为: 为什么要写`taro-hooks`?   
其实原因有两个:
- 更佳便捷、直观、函数化的调用
- 与其说是加工, 不如说是简化
大部分的`api`使用了初始配置。以及引用抛出的做法。比如类似`audio`、`record`诸如此类的全局唯一管理实例, 在使用对应`hook`的同时就相应的实例化了对应的全局实例。当然这并不是强制性的, 同时还提供了手动创建的方法。此外比如反馈型的`Toast`、`Modal`等。初始配置可以贯穿整个内部使用的过程, 很大程度减少了部分代码量的冗余。还方便了参数的传递。

## 分类
目前主要将`taro-hooks`分为:
- 基础`Hooks`: 包含事件、调试等
- 操作反馈`Hooks`: 包含Toast, Modal等
- 网络`Hooks`: 包含请求、下载等
- 媒体`Hooks`: 包含图片、音频等
- 设备`Hooks`: 包含地理位置、电量等
- 小程序`Hooks`: 包含管理器、API等
- 环境`Hooks`: 包含环境判断等

## 快速体验
项目文档使用了`dumi`进行开发。这当中直接使用`taro3.3.1`进行了文档`demo`的书写。故侧面生成了两个使用`taro-hooks`的示例。大家可参考对应的项目来体验`taro-hooks`。也欢迎大家来[`github`](https://github.com/innocces/taro-hooks)多多`pr`和`issue`。
<table>
  <tbody>
    <tr>
      <td align="center">
        <a href="javascript:;">
          <img
            width="150"
            src="https://cdn.jsdelivr.net/gh/innocces/DrawingBed/2021-8-16/1629044960619-hooks.jpeg"
          >
          <br>
          <strong>Taro-hooks weapp</strong>
        </a>
      </td>
      <td align="center">
        <a target="_blank" href="https://taro-hooks-h5.vercel.app/#/pages/index/index">
          <img
            height="150"
            style="vertical-align: -0.32em; margin-right: 8px;"
            src="https://cdn.jsdelivr.net/gh/innocces/DrawingBed/2021-8-16/1629044960613-hooksite.png"
          />
          <br>
          <strong>Taro-hooks h5</strong>
        </a>
      </td>
    </tr>
  </tbody>
</table>

## 截图展示
<section style="overflow-x: scroll!important;"> 
  <p style="width: 2435px;white-space: nowrap!important; ">
    <img style="float: left!important;width: 300px !important; margin-right: 5px; visibility: visible !important; height: auto !important;" data-ratio="0.6533333333333333" data-w="300" width="300px" src="https://cdn.jsdelivr.net/gh/innocces/DrawingBed/2021-8-15/1629041766989-taro-hooks-index.PNG" /> 
    <img style="float: left!important;width: 300px !important; margin-right: 5px; visibility: visible !important; height: auto !important;" data-ratio="0.6533333333333333" data-w="300" width="300px" src="https://cdn.jsdelivr.net/gh/innocces/DrawingBed/2021-8-15/1629041766944-device.PNG" /> 
    <img style="float: left!important;width: 300px !important; margin-right: 5px; visibility: visible !important; height: auto !important;" data-ratio="0.6533333333333333" data-w="300" width="300px" src="https://cdn.jsdelivr.net/gh/innocces/DrawingBed/2021-8-15/1629041766951-env.PNG" /> 
    <img style="float: left!important;width: 300px !important; margin-right: 5px; visibility: visible !important; height: auto !important;" data-ratio="0.6533333333333333" data-w="300" width="300px" src="https://cdn.jsdelivr.net/gh/innocces/DrawingBed/2021-8-15/1629041766976-network.PNG" /> 
    <img style="float: left!important;width: 300px !important; margin-right: 5px; visibility: visible !important; height: auto !important;" data-ratio="0.6533333333333333" data-w="300" width="300px" src="https://cdn.jsdelivr.net/gh/innocces/DrawingBed/2021-8-15/1629041766936-basic.PNG" /> 
    <img  style="float: left!important;width: 300px !important; margin-right: 5px; visibility: visible !important; height: auto !important;" data-ratio="0.6533333333333333" data-w="300" width="300px" src="https://cdn.jsdelivr.net/gh/innocces/DrawingBed/2021-8-15/1629041766970-mini-pro.PNG" /> 
    <img  style="float: left!important;width: 300px !important; visibility: visible !important; height: auto !important;" data-ratio="0.6533333333333333" data-w="300" width="300px" src="https://cdn.jsdelivr.net/gh/innocces/DrawingBed/2021-8-15/1629041766963-media.PNG" />
    <img  style="float: left!important;width: 300px !important; visibility: visible !important; height: auto !important;" data-ratio="0.6533333333333333" data-w="300" width="300px" src="https://cdn.jsdelivr.net/gh/innocces/DrawingBed/2021-8-15/1629041783589-feedback.PNG" />
  </p>
</section>

## 交流
1. [`issue`](https://github.com/innocces/taro-hooks/issues)
2. [`discussions`](https://github.com/innocces/taro-hooks/discussions)
3. 欢迎大家进入`taro-hooks 交流群`
<div align="center">
  <img width="250" src="https://cdn.jsdelivr.net/gh/innocces/DrawingBed/2021-8-16/1629044960609-qrcode.jpg" />
</div>