# 10 款经典网页小游戏 · 纯前端开源

每款游戏就是**一个 `index.html`**: HTML + CSS + JavaScript 写在同一个文件里, 零框架、零依赖、零安装。
双击用浏览器打开就能玩, 不联网也行; 手机 (触屏) 和电脑 (键盘/鼠标) 都支持。

在线玩 / 打包下载: <https://fdesky.com/games/>

## 游戏清单

| # | 游戏 | 操作 | 渲染 | 看点 (源码里能找到的实现) |
|---|---|---|---|---|
| 01 | [2048](01-2048/) | 方向键 / 触屏滑动 | DOM + CSS | `slideRow()` 一行压缩→合并→补零, 四个方向复用同一函数; 合成音效; 最高分存档 |
| 02 | [贪吃蛇](02-snake/) | 方向键 / 屏幕方向键 | Canvas | 15% 概率刷出限时 5 秒的金色食物 (+30 分); 每吃 5 个提速; 切走窗口自动暂停 |
| 03 | [俄罗斯方块](03-tetris/) | 方向键 + Z 旋转 + 空格硬降 / 屏幕按钮 | Canvas ×3 层 | 标准 SRS 旋转 + 踢墙表; 七袋随机 (`BagRandomizer`); 锁定延迟; Hold; 消行粒子特效 |
| 04 | [像素飞鸟](04-flappy-bird/) | 空格 / 点击 / 触屏 | Canvas | 圆-矩形碰撞 (管体、管帽分开判); 每过 10 根管道缝隙收窄, 150px → 120px 封底 |
| 05 | [打砖块](05-breakout/) | 方向键 / 鼠标 / 触屏拖动 | Canvas | 5 种道具 (加长/多球/火球/减速/加命); 连击加分; 关卡进度存档可续玩 |
| 06 | [宝石消消乐](06-match3/) | 点击 / 拖动交换 | Canvas | 横纵双向找三连; 4 连生成条纹宝石、5 连生成彩虹宝石; 穷举可行交换判断是否无解 |
| 07 | [扫雷](07-minesweeper/) | 左键翻 / 右键或长按插旗 / 双击快开 | DOM + CSS | 首次点击后才布雷并避开该格 (首点必不炸); `floodFill` 连片展开; 三档难度各记最佳用时 |
| 08 | [记忆翻牌](08-memory-cards/) | 点击 | DOM + CSS | Fisher-Yates 洗牌; 4 档网格 × 多主题牌面; 按用时与翻牌次数评三星, 每档网格单独存最佳 |
| 09 | [涂鸦跳跃](09-doodle-jump/) | 方向键 / 触屏 / 手机重力感应 | Canvas | 镜头跟随实现无限向上; 平台动态生成与回收; 云层视差滚动; `deviceorientation` 倾斜手机移动 |
| 10 | [五子棋](10-gomoku/) | 点击落子 | Canvas | 三档人机: 简单/中等按棋型评分, 困难用 **负极大值 + Alpha-Beta 剪枝** 搜索; 悔棋; 胜负平战绩存档 |

技术栈: HTML5 · CSS3 · 原生 JavaScript · Canvas 2D · Web Audio (音效全部代码合成, 没有音频文件) · LocalStorage

## 怎么用

```bash
git clone https://github.com/myumdl/mini-games.git
open mini-games/index.html      # 游戏大厅; 或直接打开任意一款的 index.html
```

想改哪款就打开它的 `index.html`, 改完刷新浏览器。

## 目录

```
index.html          游戏大厅 (10 款入口)
logo.png
01-2048/index.html
...
10-gomoku/index.html
```
