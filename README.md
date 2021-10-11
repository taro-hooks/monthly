# taro-hooks 月刊

每月都记录`taro-hooks`的成长的月刊!  

- 每月第一周到第二周之间更新
- 包含每月`taro-hooks`的更新内容
- 还会自荐一些最近感觉不错的实用库

## 2021
### 十月

- [第3期: taro-hooks v1.4.7](https://github.com/taro-hooks/monthly/blob/main/issues/issue-1008-v1.4.7.md)

  此次更新了近 10+ `hooks`, 新增`hooks`为:    
  - [`useBackground`](https://taro-hooks-innocces.vercel.app/hooks/layout/use-background): 动态设置窗口
  - [`useChooseAddress`](https://taro-hooks-innocces.vercel.app/hooks/wechat/use-choose-address): 获取用户收货地址。调起用户编辑收货地址原生界面，并在编辑完成后返回用户选择的地址
  - [`useManualPullDownRefresh`](https://taro-hooks-innocces.vercel.app/hooks/layout/use-manual-pull-down-refresh): 手动下拉刷新
  - [`useMenuButtonBoundingClientRect`](https://taro-hooks-innocces.vercel.app/hooks/wechat/use-menu-button-bounding-client-rect): 获取菜单按钮（右上角胶囊按钮）的布局位置信息。坐标信息以屏幕左上角为原点
  - [`useRequestSubscribeMessage`](https://taro-hooks-innocces.vercel.app/hooks/wechat/use-request-subscribe-message): 请求订阅消息
  - [`useTabBar`](https://taro-hooks-innocces.vercel.app/hooks/layout/use-tab-bar): 操作 Tab
  - [`useTopBarText`](https://taro-hooks-innocces.vercel.app/hooks/wechat/use-top-bar-text): 动态设置置顶栏文字内容
  - [`useWeRun`](https://taro-hooks-innocces.vercel.app/hooks/wechat/use-we-run): 获取微信运动数据
  - [`useApp`](https://taro-hooks-innocces.vercel.app/hooks/basic/use-app): 获取当前程序的唯一实例以及全局数据
  - [`usePage`](https://taro-hooks-innocces.vercel.app/hooks/basic/use-page): 获取当前页面(栈)

### 九月

- [第2期: taro-hooks v1.3.0](https://github.com/taro-hooks/monthly/blob/main/issues/issue-0911-v1.3.0.md)
  
  此次更新主要以小程序专属`hook`为主, 增加了常用`hook`如:    
  - `useScanCode`: 扫码相关
  - `useAuthorize`: 授权、设置授权相关
  - `useLogin`: 登录相关
  - `useUserInfo`: 获取以及展示用户信息相关

### 八月

- [第1期: taro-hooks v1.0.0](https://github.com/taro-hooks/monthly/blob/main/issues/issue-0815-v1.0.0.md)
  
  目前主要将`taro-hooks`分为:   
  - 基础`Hooks`: 包含事件、调试等
  - 操作反馈`Hooks`: 包含Toast, Modal等
  - 网络`Hooks`: 包含请求、下载等
  - 媒体`Hooks`: 包含图片、音频等
  - 设备`Hooks`: 包含地理位置、电量等
  - 小程序`Hooks`: 包含管理器、API等
  - 环境`Hooks`: 包含环境判断等
