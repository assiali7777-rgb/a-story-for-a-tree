[README.md](https://github.com/user-attachments/files/28179854/README.md)
# 三个 HTML 拼接项目 设计灵感来源于博主希彼赫(小红书号:6287924779)

## 使用方式

1. 解压本项目。
2. 双击 `index.html`，或用 VS Code / 本地服务器打开。
3. 左侧可在三个页面之间切换；也可以点击「单独打开」查看原始页面。

## 文件结构

```text
combined_html_project/
├─ index.html                         # 统一入口页
├─ phoenix_tree.html                  # 原 HTML 1：一棵凤凰木
├─ waqwaq_tree.html                   # 原 HTML 2：瓦克瓦克树 · 3D 插画书
├─ cross_cultural_mirror.html         # 原 HTML 3：跨文化之镜 · 三语融合版电子绘本
├─ source_manifest.json               # 来源和资源引用清单
└─ ASSETS_GO_HERE.txt                 # 资源放置说明
```

## 重要说明

这次拼接采用「统一入口 + iframe 切换」的方式，而不是把三份 HTML 的 CSS/JS 强行写进同一个 DOM。这样可以避免三个页面里重复的 `#canvas`、`#overlay`、音频 ID、全局变量和动画循环互相覆盖。

原始 HTML 中引用了一些图片和音频文件，但本次上传内容只有三个 `.html` 文件。如果你有原项目的素材，请把图片/音频按原来的相对路径放回项目根目录或对应文件夹，例如：

- `fn-background-1.png`
- `fn-background-3.png`
- `fn-background-4.png`
- `fh-assets/layers_2/...`
- `waq-assets/background_1.png`
- `waq-assets/waq_tree_1.png` 到 `waq_tree_5.png`
- `waq-assets/waq_fruit_0.png` 到 `waq_fruit_2.png`
- `waq-assets/waq_girl_0.png` 到 `waq_girl_5.png`
- `天气 环境 风暴 小雨 大雷 隆隆声-隆隆声-雷裂纹-自然环_爱给网_aigei_com.mp3`
- `天堂中的鸟类(Birds in heaven)_爱给网_aigei_com.mp3`
- `musicword-lovely-spring-304672.mp3`

如果素材缺失，页面仍能打开，但对应背景图、角色图或音频可能不会显示/播放。


## 2026-05-23 更新

已补入凤凰木页面所需背景图：

- `fn-background-4.png`：开场背景
- `fn-background-3.png`：正文过程背景
- `fn-background-1.png`：结尾背景

同时在 `fh-assets/layers_2/` 下放置了同名副本，以匹配原 HTML 中的备用路径。
