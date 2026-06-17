# 信披待办 Demo

> 一个静态 HTML / 原生 JS 的"信息披露公告待办"演示项目,无需任何构建工具,双击 HTML 即可运行。

## 包含文件

| 文件 | 角色 |
|---|---|
| `disclosure-mgmt.html` | 首页 / 仪表盘(Row 1 含待办公告提示、信披数据网络、产品任务日历三栏) |
| `todo-list-management.html` | 二级页 / 待办列表管理(支持"待办/已发起/已失效"Tab 切换) |
| `todo-mock-data.js` | 共享 mock 数据源(同时被两页面引用,作为【唯一事实源】) |

## 运行方式

```bash
# 方式 1:直接双击 HTML(最简单的本地预览)
open disclosure-mgmt.html
```

```bash
# 方式 2:起一个本地静态服务(推荐,避免某些浏览器对 file:// 的限制)
python -m http.server 8000
# 然后访问 http://localhost:8000/disclosure-mgmt.html
```

```bash
# 方式 3:Node 用户
npx serve .
```

## 数据约定

两页面通过 `window.__TODO_TASKS__` / `window.__TODO_TODAY__` 共享同一份 mock 数据。
字段契约详见 `todo-mock-data.js` 顶部注释。

## 技术栈

- 纯 HTML + 原生 JavaScript(ES5 兼容语法)
- CSS Grid + Flexbox 布局
- 无任何第三方依赖

## 版本

- 当前演示版本:0617
- 历史快照:0611、0616
