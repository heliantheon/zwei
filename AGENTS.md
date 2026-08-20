# Zwei

Zwei 是基于 Taro 4、React 和 TypeScript 的多端菜品推荐应用，默认面向抖音小程序；微信、支付宝和 H5 构建作为按需兼容目标。

## 技术栈

- Taro 4.1.8
- React 18
- TypeScript
- Taro UI
- Sass
- pnpm

## 常用命令

```bash
pnpm install
pnpm dev          # 默认启动抖音小程序开发构建
pnpm dev:tt
pnpm dev:weapp
pnpm dev:alipay
pnpm dev:h5
pnpm build        # 默认构建抖音小程序
pnpm build:tt
pnpm build:weapp
pnpm build:alipay
pnpm build:h5
pnpm type:check
pnpm format:check
```

## 项目边界

- `src/pages/` 存放页面级业务模块。
- `src/components/` 存放跨页面复用组件。
- `src/services/` 负责 API 调用，不要在页面组件中散落底层请求。
- `src/utils/` 存放无业务状态的通用工具。
- `src/types/` 维护共享 TypeScript 类型。
- 环境配置通过 `scripts/setup-env.js` 和现有变量约定生成，不提交密钥或平台私密配置。

## 开发规则

- 抖音小程序是默认开发与 CI/CD 目标；调整默认平台时同步修改 scripts、workflow 和 README。
- 平台专属 API 必须隔离，并为其他保留平台提供明确降级行为。
- 推荐、菜谱和用户偏好数据通过 service 层访问，保持加载、失败和空状态完整。
- UI 改动同时考虑小程序安全区、窄屏、触摸目标和弱网场景。

## 验证 Checklist

1. 运行 `pnpm type:check`。
2. 运行 `pnpm format:check`。
3. 至少执行受影响平台的开发或生产构建。
4. 涉及平台配置时检查抖音默认路径，并确认其他平台脚本仍可手动运行。
