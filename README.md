# 🌟 Astro 集成 Bootstrap 5 指南

本指南将帮助你快速在 [Astro](https://astro.build) 项目中集成 Bootstrap 5，实现现代化网页的快速开发。

---

## ✅ 步骤 1：创建 Astro 项目

打开终端并运行：

```sh
$ pnpm create astro@latest hello-astro-bootstrap
```

创建完成后，进入项目目录：
```sh
$ cd hello-astro-bootstrap
```

---

## ✅ 步骤 2：添加 Bootstrap 5 依赖

```sh
$ pnpm add bootstrap
```

> 如果你看到以下提示：

```js
Ignored build scripts: esbuild, sharp.
Run "pnpm approve-builds" to pick which dependencies should be allowed to run scripts.
```

请执行：

```sh
$ pnpm approve-builds
```

---

## ✅ 步骤 3：引入 Bootstrap 样式与脚本

在 Astro 布局文件`src/layouts/Layout.astro`中引入样式和脚本，例如：

```html
---
import "bootstrap/dist/css/bootstrap.min.css";
---
<!doctype html>
<html lang="zh">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width" />
    <link rel="icon" type="image/svg+xml" href="/favicon.svg" />
    <meta name="generator" content="Astro" />
    <title>Bootstrap in Astro</title>
  </head>
  <body>
    <slot />
    <script>
        import "bootstrap/dist/js/bootstrap.bundle.min.js";
    </script>
  </body>
</html>
```

---

## ✅ 步骤 4：启动开发服务器

```sh
$ pnpm dev
```

---

## ✅ 步骤 5：访问项目页面

打开浏览器访问：

```js
http://localhost:4321
```

你将看到一个集成了 Bootstrap 5 的 Astro 页面。

---

## 📌 小贴士

- 推荐将 Bootstrap 样式统一引入到 `src/layouts/Layout.astro` 中，便于维护；
- Bootstrap 的 JavaScript 功能（如 modal、dropdown）需引入 `bootstrap.bundle.min.js`；
- 可结合 Vue/React 组件与 `client:load` 等指令增强交互。

---