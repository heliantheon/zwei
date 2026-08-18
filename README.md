<p align="center">
  <img src="./assets/brand/mark.svg" width="112" alt="Zwei logo" />
</p>

<h1 align="center">Zwei</h1>

<p align="center">
  <strong>Make every meal easier to choose and worth looking forward to.</strong><br />
  让每一餐更好选择，也更值得期待。
</p>

## Overview / 项目简介

Zwei is a Taro mini-program for meal discovery, contextual recommendations, recipes, cooking guidance, favorites, history, shopping lists, and dietary preferences.

Zwei 是一个以抖音小程序为默认目标的餐食推荐应用，提供场景化推荐、菜谱与烹饪指引、收藏、历史记录、购物清单和饮食偏好管理。

## Platforms

- Douyin/TikTok mini program is the default development and delivery target.
- WeChat, Alipay, and H5 scripts remain available as manual fallback builds.

## Development

```bash
pnpm install
pnpm dev
pnpm dev:tt
pnpm dev:weapp
pnpm dev:alipay
pnpm dev:h5
```

Environment files are prepared by `scripts/setup-env.js`. All public variables use the `TARO_APP_` prefix.

## Verification

```bash
pnpm type:check
pnpm format:check
pnpm build
```

API access belongs in `src/services`; pages and components must preserve loading, empty, failure, narrow-screen, touch-target, and weak-network states.
