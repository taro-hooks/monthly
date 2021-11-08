# taro-hooks 月刊

[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Ftaro-hooks%2Fmonthly.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2Ftaro-hooks%2Fmonthly?ref=badge_shield)

每月都记录`taro-hooks`的成长的月刊!

- 每月第一周到第二周之间更新
- 包含每月`taro-hooks`的更新内容
- 还会自荐一些当月感觉不错的实用库

当然也推荐大家一起贡献比较好的库, 周边以及使用[`taro-hooks`](https://github.com/innocces/taro-hooks)的案例！直接提至[issue](https://github.com/taro-hooks/monthly/issues)即可.

## 2021

### 十一月

- [第 4 期: taro-hooks v1.5.0](https://github.com/taro-hooks/monthly/blob/main/issues/issue-1108-v1.5.0.md)

  此次更新了近 3 个 `hooks`, 新增`hooks`为:

  - [`useBle`](https://taro-hooks-innocces.vercel.app/hooks/device/use-ble): 低功耗蓝牙
  - [`useBluetooth`](https://taro-hooks-innocces.vercel.app/hooks/device/use-bluetooth): 蓝牙设备
  - [`useFrom`](https://taro-hooks-innocces.vercel.app/hooks/basic/use-from): 路由相关, 扩充`Taro useRouter`, 获取来源页面信息
  - 扩充[useRouter](https://taro-hooks-innocces.vercel.app/hooks/basic/use-router), 结合`useFrom`增加来源页面信息.
  - 修复部分`hook`返回实例定义
  - 修复部分`hook`返回默认初始值
  - 增加部分[`FAQ`](https://taro-hooks-innocces.vercel.app/quick/faq#6-%E4%B8%BA%E4%BB%80%E4%B9%88%E6%9C%89%E4%BA%9B%E7%B1%BB%E5%9E%8B%E4%BC%9A%E6%8A%A5%E4%B8%8D%E5%AD%98%E5%9C%A8)类型不存在说

### 十月

- [第 3 期: taro-hooks v1.4.7](https://github.com/taro-hooks/monthly/blob/main/issues/issue-1008-v1.4.7.md)

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
  - [`如何在taro2.x中使用taro-hooks`](https://github.com/taro-hooks/taro-hooks-demo-for-taro2.x)

### 九月

- [第 2 期: taro-hooks v1.3.0](https://github.com/taro-hooks/monthly/blob/main/issues/issue-0911-v1.3.0.md)

  此次更新主要以小程序专属`hook`为主, 增加了常用`hook`如:

  - `useScanCode`: 扫码相关
  - `useAuthorize`: 授权、设置授权相关
  - `useLogin`: 登录相关
  - `useUserInfo`: 获取以及展示用户信息相关

### 八月

- [第 1 期: taro-hooks v1.0.0](https://github.com/taro-hooks/monthly/blob/main/issues/issue-0815-v1.0.0.md)

  目前主要将`taro-hooks`分为:

  - 基础`Hooks`: 包含事件、调试等
  - 操作反馈`Hooks`: 包含 Toast, Modal 等
  - 网络`Hooks`: 包含请求、下载等
  - 媒体`Hooks`: 包含图片、音频等
  - 设备`Hooks`: 包含地理位置、电量等
  - 小程序`Hooks`: 包含管理器、API 等
  - 环境`Hooks`: 包含环境判断等

## License

[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Ftaro-hooks%2Fmonthly.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2Ftaro-hooks%2Fmonthly?ref=badge_large)
