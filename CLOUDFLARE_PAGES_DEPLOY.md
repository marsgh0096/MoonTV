# Cloudflare Pages 部署说明（MarsG TV）

本仓库已为 Cloudflare Pages + D1 部署整理好配置说明。

## Pages 构建配置

- Framework preset: `None`
- Build command: `pnpm install --frozen-lockfile && pnpm run pages:build`
- Build output directory: `.vercel/output/static`
- Compatibility flag: `nodejs_compat`

## Pages 环境变量 / Secrets

建议在 Cloudflare Pages 项目中设置：

- `NEXT_PUBLIC_STORAGE_TYPE = d1`
- `USERNAME = marsgh`
- `PASSWORD = 271448`
- `SITE_NAME = MarsG TV`
- `NEXT_PUBLIC_ENABLE_REGISTER = false`
- `NEXT_PUBLIC_SEARCH_MAX_PAGE = 3`
- `ANNOUNCEMENT = 本站仅供个人学习使用，请勿传播或公开分享。`
- `NEXT_PUBLIC_DISABLE_YELLOW_FILTER = false`

## D1 数据库绑定

- Binding name: `DB`

## D1 初始化

创建 D1 数据库后，将 `cloudflare/d1-init.sql` 的内容复制到 D1 控制台执行。
