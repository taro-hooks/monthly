<div align="center"><img width="150" src="https://cdn.jsdelivr.net/gh/innocces/DrawingBed/2021-8-16/1629044969573-hook.png" /></div>

10 月, `taro-hooks`又发布了 2 个版本(其中包含 1 个修复补丁和 1 个小版本). `taro-hooks`基本保持着每周发布一个版本的频率在维护更新. 目前`taro-hooks`已经拥有 52+`hooks`可供使用。覆盖了将近 75%的官方`api`.

目前`taro-hooks`最新版本为`v1.5.0`.(这个月比较忙。基本没怎么写东西)

<div align="center"><img width="150" src="https://cdn.jsdelivr.net/gh/innocces/DrawingBed/2021-8-16/1629044960619-hooks.jpeg" /></div>

## 概要

此次更新了近 3 个 `hooks`, 新增`hooks`为:

- [`useBle`](https://taro-hooks-innocces.vercel.app/hooks/device/use-ble): 低功耗蓝牙
- [`useBluetooth`](https://taro-hooks-innocces.vercel.app/hooks/device/use-bluetooth): 蓝牙设备
- [`useFrom`](https://taro-hooks-innocces.vercel.app/hooks/basic/use-from): 路由相关, 扩充`Taro useRouter`, 获取来源页面信息

## 其他

- 扩充[useRouter](https://taro-hooks-innocces.vercel.app/hooks/basic/use-router), 结合`useFrom`增加来源页面信息.
- 修复部分`hook`返回实例定义
- 修复部分`hook`返回默认初始值
- 增加部分[`FAQ`](https://taro-hooks-innocces.vercel.app/quick/faq#6-%E4%B8%BA%E4%BB%80%E4%B9%88%E6%9C%89%E4%BA%9B%E7%B1%BB%E5%9E%8B%E4%BC%9A%E6%8A%A5%E4%B8%8D%E5%AD%98%E5%9C%A8)类型不存在说明.

## 更新日志

### Bugfix & Improvment

- **hook type:** fix default value of some hook instance ([28b96f8](https://github.com/innocces/taro-hooks/commit/28b96f82c020c4dcec5f1c446765e915a35c4c8e))
- **usemenubuttonboundingclientrect:** fix typeof useMenuButtonBoundingClientRect result ([a25d76c](https://github.com/innocces/taro-hooks/commit/a25d76cc14dc45639fbdcb73917d58fc7733a20b))
- **usesysteminfo:** fix typeof useSystemInfo result ([db30a1b](https://github.com/innocces/taro-hooks/commit/db30a1b4ac3099b8dfd06b6077f0c89ecc51ff8a))
- **useupdatemanager:** fix return instance of useUpdateManager ([92d99ca](https://github.com/innocces/taro-hooks/commit/92d99ca691277a5006e87c801d44c97766afb1c0))
- **share & default:** add share func for request feature & fix some default of hooks ([879ca4b](https://github.com/innocces/taro-hooks/commit/879ca4bcaacdadec84d14cd33e8e63898905dd8f))

### Feature

- **useble:** add useBLE ([9d60c08](https://github.com/innocces/taro-hooks/commit/9d60c08e9b16515ec6a4ac65146fbf6545de6d45))
- **useble:** add useEffect code for useBLE ([615a23a](https://github.com/innocces/taro-hooks/commit/615a23a316a0d3e024122f81d2898c7f5857ef38))
- **usebluetooth:** add doc and type for useBluetooth ([7f1b80b](https://github.com/innocces/taro-hooks/commit/7f1b80b9ef3f3d7a2ef5b9fce581c11658d65ffe))
- **usebluetooth:** add useBluetooth ([931d7f4](https://github.com/innocces/taro-hooks/commit/931d7f47495e757eb03423d1f8eff53774141a94))
- **usefrom:** add useFrom hook ([248157d](https://github.com/innocces/taro-hooks/commit/248157d60656a985757b4608623dd429c62b4905))
- **userouter:** add from info for useRouter ([c2631f6](https://github.com/innocces/taro-hooks/commit/c2631f69f6afd044544a3b6126736d16f0da1940))

[更多更新日志请查看](https://github.com/innocces/taro-hooks/releases)

## 推荐

1. [dragula](https://github.com/bevacqua/dragula)  
   兼容性和使用感都不错的拖拽库. 官方还提供了大量示例以及配合框架使用的 demo.  
   ![](https://cdn.jsdelivr.net/gh/innocces/DrawingBed/2021-11-08/1636366142264-demo.png)
2. [淘宝 NPM 镜像站换新域名](https://zhuanlan.zhihu.com/p/430580607)

   - 相关优化

     - 启动新的域名。
     - Registry 全面重构，提升稳定性，降低同步失败率。
     - CLI 优化，提升安装速度，去掉软连接等带来的兼容性问题。
     - 沉淀自企业级大规模应用的使用经验手册。

   - 迁移方案
     - 切换域名为: https://registry.npmmirror.com
     - 重新安装所使用的版本的 patch 版本即可

3. [Toward Hermes being the Default](https://reactnative.dev/blog/2021/10/26/toward-hermes-being-the-default)  
   In this post, we want to highlight some of the most exciting progress we've made over the past two years to push Hermes towards being the best JavaScript engine for React Native. Looking forward, we are confident that with these improvements and more to come, we can make Hermes the default JavaScript engine for React Native across all platforms.

4. [apexcharts](https://github.com/apexcharts/apexcharts.js)  
   📊 Interactive JavaScript Charts built on SVG  
   一个轻量的 SVG 图表解决方案  
   ![](https://cdn.jsdelivr.net/gh/innocces/DrawingBed/2021-11-08/1636365660098-68747470733a2f2f617065786368617274732e636f6d2f6d656469612f617065786368617274732d62616e6e65722e706e67.png)

5. [color](https://github.com/LeaVerou/color.js)  
   Color space conversion & manipulation lib.  
   关于颜色转换的操作库.  
   ![](https://cdn.jsdelivr.net/gh/innocces/DrawingBed/2021-11-08/1636365755063-color.png)

6. [excalidraw-animate](https://github.com/dai-shi/excalidraw-animate)  
   A tool to animate Excalidraw drawings  
   [excalidraw](https://excalidraw.com) 算是笔者最喜欢的流程绘画库了. 而 excalidraw-animate 可操作 excalidraw 产物(画板信息)并利用当前的绘制顺序生成动画 SVG.  
   ![](https://cdn.jsdelivr.net/gh/innocces/DrawingBed/2021-11-08/1636365497193-83698750-332ca080-a63d-11ea-9845-d2442e9b4305.gif)

7. [shoelace](https://github.com/shoelace-style/shoelace)  
   一个多框架适用的 PC 组件库. 风格感觉有点介于 Material 和日常风格之间的感觉.组件比较丰富.  
   ![](https://cdn.jsdelivr.net/gh/innocces/DrawingBed/2021-11-08/1636366744377-WX20211108-181849.png)
