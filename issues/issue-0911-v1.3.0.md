<div align="center"><img width="150" src="https://cdn.jsdelivr.net/gh/innocces/DrawingBed/2021-8-16/1629044969573-hook.png" /></div>

距离`taro-hooksv1.0.0`发布已经过去将近一个月的时间。期间`taro-hooks`又发布了6个版本(其中包含三个修复补丁和3个小版本). `taro-hooks`基本保持着每周发布一个版本的频率在维护更新. 目前`taro-hooks`已经拥有37+`hooks`可供使用。覆盖了将近60%的官方`api`.    

目前`taro-hooks`最新版本为`v1.3.0`.

<div align="center"><img width="150" src="https://cdn.jsdelivr.net/gh/innocces/DrawingBed/2021-8-16/1629044960619-hooks.jpeg" /></div>

## 概要
此次更新主要以小程序专属`hook`为主, 增加了常用`hook`如: 
- `useScanCode`: 扫码相关
- `useAuthorize`: 授权、设置授权相关
- `useLogin`: 登录相关
- `useUserInfo`: 获取以及展示用户信息相关

## 其他
- 增加脚手架模板
增加了`taro init`初始化创建模板. 具体使用方式如下: 
  ```bash
  // 确保node版本在12+
  $ node -v
  $ v12.22.1
  $ npx @tarojs/cli init taro-hooks-demo
  // 框架选择React
  $ ? 请选择框架 React
  // 模板源选择: github (确保可拉取到 taro-hooks 模板)
  $ ? 请选择模板源
  $   Gitee（最快）
  $ ❯ Github（最新）
  // 后面提示选择模板时: 选择 taro-hooks 模板
  $ ? 请选择模板
  $   mobx
  $   react-native
  $   redux
  $ ❯ taro-hooks（使用 taro-hooks 的模板）
  $   taro-ui（使用 taro-ui 的模板）
  // 后面等待安装成功, 运行对应端命令即可查看模板示例
  $ cd taro-hooks-demo
  $ yarn dev:weapp
  $ yarn dev:h5
  ```


- tree shaking    
关于`tree shaking`是大家比较关心的一个问题. `taro-hooks` 的 `js` 代码默认支持基于 `ES modules` 的 `tree shaking` . 但你依然可以显式的使用[`babel-plugin-import`](https://github.com/ant-design/babel-plugin-import)去设置按需加载, 设置方式如下:
  ```js
  // babel.config.js
  module.exports = {
    plugins: [
      [
        'import',
        {
          libraryName: 'taro-hooks',
          camel2DashComponentName: false,
        },
        'taro-hooks',
      ],
    ],
  };
  ```

## 更新日志
### Bugfix & Improvment
- update useSystemInfo and useLaunchOptions ([6c08d96](https://github.com/innocces/taro-hooks/commit/6c08d96ac4ffaf4fa1bf102d6327146b151b6ba2))
- update useStorage to sync ([18f96f4](https://github.com/innocces/taro-hooks/commit/18f96f4fb8d864d485286b5840db6cc795954cb8))
- fix useBattery ios level async problem ([5c3d937](https://github.com/innocces/taro-hooks/commit/5c3d9379dad538c1701f67e5ad970dda560c7713))
- fix useVibrate interval to auto close ([8e4808e](https://github.com/innocces/taro-hooks/commit/8e4808ecf5cede53b123a0d2a2ce3c2ee3638edf))
- improve useUpdateManager behavior and app index check update ([411684c](https://github.com/innocces/taro-hooks/commit/411684ceb83c09b7f5dea9d647c8e5899ca9bbb5))

### Feature
- update taro version to 3.3.6(latest) ([547080a](https://github.com/innocces/taro-hooks/commit/547080a7adc5c9cbc0ba55c0a046378d29f21868))
- add useAccountInfo hook ([cd8aa61](https://github.com/innocces/taro-hooks/commit/cd8aa61950a2666383cbe19ef91303e61303862f))
- add useAuthorize hook ([c0ec57c](https://github.com/innocces/taro-hooks/commit/c0ec57c0359eee64926dc101dbdb2903d38e0f40))
- add useLogin, useUserInfo hooks ([fa74d86](https://github.com/innocces/taro-hooks/commit/fa74d860c9627794678d1dc2498bb869b3b8e823))
- add useScanCode hook ([1a55a65](https://github.com/innocces/taro-hooks/commit/1a55a659e9da63af6a9cbd80add0eb054d5878ee))    

[更多更新日志请查看](https://github.com/innocces/taro-hooks/releases)

## 推荐

有一个idea, 也开始着手开发了, 就写一个前端的工具小网站. 目前实现了常用的图片压缩. 后面还会丰富更多常用的工具.  
希望大家可以多多提`issue`、`pr`一起丰富!  

- [网站地址](https://general-tools.vercel.app/compress-image)
- [GITHUB-general-tools](https://github.com/innocces/general-tools)
