# vuepress-sponsor
[原仓库地址](https://github.com/yokefellow/vuepress-plugin-sponsor)
## 简介
如果你是第一次了解这个打赏插件，请查看原仓库，并按照原仓库使用安装。

本仓库将打赏插件简化，只留了微信和支付宝，

并没有解决打赏在评论的下方的问题，所以建议使用标签引用

## 使用
1. 下载本仓库
2. 将 sponsor.vue放置在components下
3. 将 sponsor-logo放置在 public下
4. 在sponsor.vue中写入自己的二维码图片地址，在六十行和六十二行
5. 在enhanceApp.js中引用
``` js
// 使用异步函数也是可以的
import Sponsor from './components/Sponsor.vue';
export default ({
    Vue, // VuePress 正在使用的 Vue 构造函数
    options, // 附加到根实例的一些选项
    router, // 当前应用的路由实例
    siteData, // 站点元数据
    isServer // 当前应用配置是处于 服务端渲染 或 客户端
  }) => {
    // ...做一些其他的应用级别的优化
    Vue.component('Sponsor',Sponsor);
  }
```
6. 在需要打赏插件的位置上用标签引用即可
``` js
<Sponsor/>
```
