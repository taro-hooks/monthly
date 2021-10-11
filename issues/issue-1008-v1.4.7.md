<div align="center"><img width="150" src="https://cdn.jsdelivr.net/gh/innocces/DrawingBed/2021-8-16/1629044969573-hook.png" /></div>

9月, `taro-hooks`又发布了10个版本(其中包含9个修复补丁和1个小版本). `taro-hooks`基本保持着每周发布一个版本的频率在维护更新. 目前`taro-hooks`已经拥有49+`hooks`可供使用。覆盖了将近70%的官方`api`.    

目前`taro-hooks`最新版本为`v1.4.7`.

<div align="center"><img width="150" src="https://cdn.jsdelivr.net/gh/innocces/DrawingBed/2021-8-16/1629044960619-hooks.jpeg" /></div>

## 概要
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

## 其他
- 修复部分`hook`类型定义
- 增加部分微信小程序`api`参数定义
- 增加部分[`FAQ`](https://taro-hooks-innocces.vercel.app/quick/faq)常见问题.

## 在`taro 2.x`中使用`taro-hooks`
原则上不推荐在小于`3.x`的`taro`项目中使用`taro-hooks`. 但若有希望可以使用的, 还是提供了接入方式, 但是并不是完全可用, 部分`hook`还是受到限制.  
具体使用方式可参考[taro-hooks-demo-for-taro2.x](https://github.com/taro-hooks/taro-hooks-demo-for-taro2.x). 下面简单阐述部分配置:   

1. 由于早版本的`taro`模式还是`nervjs`. 故限制了部分`hooks`需从`@tarojs/taro`中引入. 在经由`taro-cli`来进行分发不同的端匹配. `taro-hooks`初期就是适配`3.x`来进行使用的, 故源码中直接对`react`进行了引用. 这里我们需要转换一下模块, 需要用到配置中的`alias`.
    ```javascript
    // config/index.js 需手动指定端的入口
    const env = process.env.TARO_ENV;
    const config = {
      // ...
      alias: {
        react: resolve(
          __dirname,
          "..",
          "node_modules",
          "@tarojs/taro-" + env,
          env === "h5" ? "src/index.cjs.js" : "index.js"
        ),
      },
      // ...
    }
    ```

2. 由于`taro-hooks`内部不会经由`taro`解析。故部分`api`在`h5`端不会走对应的`default`或者`cjs`的模式, 所以若需要在`h5`端使用, 还需增加`h5`端`webpackChain`的模块解析, 这里简单的为大家提供一个`loader`(实际就是将`@tarojs/taro`替换为了`@tarojs/taro-h5/src/index.cjs.js`):

  - `taro-hooks-loader`

    ```javascript
    // config/taro-hooks-loader.js
    export default function taroHooksLoader(source) {
      return source.replace(
        "@tarojs/taro", 
        "@tarojs/taro-h5/src/index.cjs.js"
      );
    }
    ```

  - `config`

    ```javascript
    // config/index.js
    const config = {
      // ...
      h5: {
        webpackChain(chain) {
          chain.merge({
            module: {
              rule: {
                "taro-hooks-loader": {
                  test: /taro-hooks/,
                  loader: resolve(__dirname, "taro-hooks-loader"),
                },
              },
            },
          });
        },
      }
      // ...
    }
    ```

3. 需要手动配置按需加载
  - 需下载`babel-plugin-import`

    ```bash
    $ npm i babel-plugin-import -D
    ```

  - 配置

    ```javascript
    // config/index.js
    const config = {
      // ...
      plugins: [
        // ...
        [
          "import",
          {
            libraryName: "taro-hooks",
            camel2DashComponentName: false,
          },
          "taro-hooks",
        ],
      ],
      // ...
    }
    ```


## 更新日志
### Bugfix & Improvment
- **build type:** fix build type for namespace error ([05a285b](https://github.com/innocces/taro-hooks/commit/05a285b8d4761bee2c55a9dd7ccb71d53223acfc))
- **deps of hooks:** fix deps to devDeps for hooks force version conflict ([fd72923](https://github.com/innocces/taro-hooks/commit/fd72923453619c1e9c0a8964b36ad0efd221f1d5))
- **type:** fix type of feedback hooks ([4728379](https://github.com/innocces/taro-hooks/commit/4728379aabadc58b8c3b166e65d036d397612369))
- **add create inner:** useWebAudioImplement option add ([9e1254c](https://github.com/innocces/taro-hooks/commit/9e1254c527f6bd1d3ceba24f7338d3dd69242d51))
- **useaudio option:** add option set root for context ([b63567f](https://github.com/innocces/taro-hooks/commit/b63567feec61567e90ccc19c400b48e4a68dad0d))
- **useimage:** fix useImage choose function params partial ([cf7be5f](https://github.com/innocces/taro-hooks/commit/cf7be5f9832e6744d4a1baf5211212b1bb27d33c))
- **usemodal:** fix useModal callback type ([d1e14a7](https://github.com/innocces/taro-hooks/commit/d1e14a7f73dda098ec062b9c3c3173f1eec404f8))

### Feature
- **usebackground:** add useBackground hook ([5f43b0c](https://github.com/innocces/taro-hooks/commit/5f43b0cf66c9d09cfbd63063e08344b6152ebc41))
- **usechooseaddress:** add useChooseAddress hook ([7187d95](https://github.com/innocces/taro-hooks/commit/7187d9587ff5174d038801e43361e81a7fb30db2))
- **useinvoice:** add useInvoice hooks ([c293b1e](https://github.com/innocces/taro-hooks/commit/c293b1e801e5d810b63a3b080654079732eb4460))
- **usemanualpulldownrefresh:** add useManualPullDownRefresh hook ([9b1d18b](https://github.com/innocces/taro-hooks/commit/9b1d18b1914cf275fde4a707d8ce1dd34ee154b7))
- **usemenubuttonboundingclientrect:** add useMenuButtonBoundingClientRect hook ([5c7cde6](https://github.com/innocces/taro-hooks/commit/5c7cde69ef6be79a3699cdb39fa436a363f189b7))
- **userequestsubscribemessage:** add useRequestSubscribeMessage hook & faq for hooks version ([ba3ea2f](https://github.com/innocces/taro-hooks/commit/ba3ea2f583b00d443aad31cab59e60151e1ed873))
- **usetabbar:** add useTabBar hook ([d46240c](https://github.com/innocces/taro-hooks/commit/d46240c915e18ce214070cb2aec005b01029f07e))
- **usetopbartext:** add useTopBarText hook ([cd22332](https://github.com/innocces/taro-hooks/commit/cd22332a8f8fffee5a1ea0b81214b219011afeaa))
- **usewerun:** add useWeRun hook ([951826f](https://github.com/innocces/taro-hooks/commit/951826f4f423d44661be6d5eddca6e693ba68dbd))
- **faq & useapp:** add useApp hooks & faq of useSelectorQuery ([3e0ebea](https://github.com/innocces/taro-hooks/commit/3e0ebeaafffb1279532f25996b69221a3398aa51))
- **usepage:** add usePage hook & useSelectorQuery method scope optional ([35b8ab7](https://github.com/innocces/taro-hooks/commit/35b8ab72b580688292bdb33d06dc6d3530f1844f))   

[更多更新日志请查看](https://github.com/innocces/taro-hooks/releases)

## `taro-hooks`案例

[taro-todolist 💯 ](https://github.com/innocces/taro-todolist):  一款待办事项小程序, 使用taro-hooks开发  
<table>
  <tbody>
    <tr>
      <td align="center">
        <a>
          <img
            width="200"
            src="https://cdn.jsdelivr.net/gh/innocces/DrawingBed/2021-09-27/1632746107141-qrcode.jpg"
          />
          <br>
          <strong>taro-todolist weapp</strong>
        </a>
      </td>
      <td align="center">
        <a target="_blank" href="https://taro-todolist.vercel.app">
          <img
            height="200"
            src="https://cdn.jsdelivr.net/gh/innocces/DrawingBed/2021-10-06/1633494500167-taro-todolist.png"
          />
          <br>
          <strong>taro-todolist h5</strong>
        </a>
      </td>
    </tr>
  </tbody>
</table>

## 推荐

1. [general-tools: github 图床](https://github.com/innocces/general-tools)    
小工具库更新了利用`GitHub` + `jsdelivr`生成图床. 可点击[传送门](https://general-tools.vercel.app/drawer-bed)体验.

2. [react-spring](https://github.com/pmndrs/react-spring)
react-spring is a spring-physics based animation library that should cover most of your UI related animation needs. It gives you tools flexible enough to confidently cast your ideas into moving interfaces.   
实用且扩展性高的`React`动画库. 且在多个平台皆有实现:
    ```txt
    @react-spring/konva
    @react-spring/native
    @react-spring/three
    @react-spring/web
    @react-spring/zdog
    ```
3. [typescript-book](https://github.com/basarat/typescript-book)
📚 The definitive guide to TypeScript and possibly the best TypeScript book 📖. Free and Open Source 🌹

4. [tauri](https://github.com/tauri-apps/tauri)
Tauri is a framework for building tiny, blazing fast binaries for all major desktop platforms. Developers can integrate any front-end framework that compiles to HTML, JS and CSS for building their user interface. The backend of the application is a rust-sourced binary with an API that the front-end can interact with.    
rust 版的 electron ?