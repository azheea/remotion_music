# remotion_music

仿 Apple Music 风格的歌词视频渲染工程，基于 Remotion + React。该项目通过组合音频与歌词（LRC）生成带动效的歌曲视频输出，适用于批量渲染与本地预览。

**快速指南**

- 环境要求：Node.js 18+，Git
- 安装依赖：

```bash
npm install
```

- 本地预览（开发时查看 composition）：

```bash
npx remotion preview
```

- 渲染单个 composition（示例）：

```bash
npx remotion render <composition> --codec=h264 --output out/video.mp4
```

- 使用仓库内的批量渲染脚本：

```bash
node render-all.mjs
```

将 `<composition>` 替换为 `src/` 中定义的 composition 名称。

**项目结构（常见）**

- `render-all.mjs` — 批量渲染脚本
- `public/` — 放置音频、字体、图片等静态资源
- `src/` — 源代码（组件、工具、类型）
- `package.json` — 依赖与脚本

**使用建议**

- 将音频（如 `.m4a`）和歌词文件（`.lrc`）放入 `public/` 或专门的资源目录，组件从 `src/` 中引用。
- 渲染耗时较长，建议在渲染前先使用 `preview` 检查画面与时间轴同步。
- 

---

更多使用细节和示例可放入 `docs/` 或在 README 中扩展，是否需要我补充示例 composition 与渲染脚本说明？
