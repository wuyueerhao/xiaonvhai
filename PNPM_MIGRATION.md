# PNPM 迁移说明

## 迁移完成

项目已成功从 npm 迁移到 pnpm。

## 主要变更

1. **删除的文件**：
   - `package-lock.json` (npm 锁定文件)
   - `node_modules/` (重新安装)

2. **新增的文件**：
   - `.npmrc` (pnpm 配置)
   - `pnpm-lock.yaml` (pnpm 锁定文件)

3. **更新的文件**：
   - `package.json` (添加 packageManager 和 engines 字段)
   - `.gitignore` (添加 pnpm 相关忽略规则)

## 常用命令对照

| npm 命令 | pnpm 命令 |
|---------|----------|
| `npm install` | `pnpm install` |
| `npm run build` | `pnpm build` |
| `npm run server` | `pnpm server` |
| `npm run clean` | `pnpm clean` |
| `npm run deploy` | `pnpm deploy` |

## 优势

- 更快的安装速度
- 更少的磁盘空间占用
- 更严格的依赖管理
- 更好的 monorepo 支持