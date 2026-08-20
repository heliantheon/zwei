<p align="center">
  <img src="./assets/brand/hero-ice.png" width="256" alt="Zwei logo" />
</p>

<h1 align="center">Zwei</h1>

Zwei 是一个帮你决定吃什么的小程序。场景化推荐、菜谱和烹饪指引、收藏、历史记录、购物清单、饮食偏好——把这些攒到一块，让每一餐都更省心，也更值得期待。

Zwei is a mini-program for figuring out what to eat: contextual recommendations, recipes and cooking guidance, favorites, history, shopping lists, and dietary preferences in one place.

## 平台

- 抖音小程序是默认的开发与交付目标。
- 微信、支付宝、H5 作为手动兼容构建保留。

## 开发

```bash
pnpm install
pnpm dev          # 默认抖音小程序
pnpm dev:tt
pnpm dev:weapp
pnpm dev:alipay
pnpm dev:h5
```

环境配置由 `scripts/setup-env.js` 生成，公共变量统一用 `TARO_APP_` 前缀。

## 验证

```bash
pnpm type:check
pnpm format:check
pnpm build
```

API 调用收在 `src/services`；页面和组件需要照顾到加载、空、失败、窄屏、触摸目标和弱网这些状态。
