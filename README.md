# CET Typing Lab

CET Typing Lab 是一个面向大学英语四级 / 六级备考场景的英文打字练习项目，把句子训练、篇章训练和进度反馈结合在一个轻量的网页应用里。  
CET Typing Lab is a lightweight web app for CET-4 and CET-6 typing practice, combining sentence drills, passage training, and progress feedback in one place.

## 在线访问 | Live Demo

- GitHub Pages 地址：[https://L-zeus.github.io/cet-typing-lab/](https://L-zeus.github.io/cet-typing-lab/)
- Live site on GitHub Pages: [https://L-zeus.github.io/cet-typing-lab/](https://L-zeus.github.io/cet-typing-lab/)

## 最新更新 | Latest Update

- English release notes: [`CHANGELOG.md`](./CHANGELOG.md)
- 中文更新日志：[`CHANGELOG.zh-CN.md`](./CHANGELOG.zh-CN.md)

## 功能特点 | Features

- 支持 CET4 / CET6 句子练习与长篇文章练习。
- Supports both CET-4 / CET-6 sentence drills and long-passage practice.

- 实时统计 WPM、准确率和完成情况，帮助观察打字稳定性。
- Tracks WPM, accuracy, and completion in real time so users can measure typing stability.

- 记录错键、慢词和历史成绩，方便针对薄弱点复盘。
- Highlights weak keys, slow words, and session history for targeted review.

- 提供 Data Bank / Progress / Challenge 等视图，便于持续练习。
- Includes Data Bank, Progress, and Challenge views to support ongoing practice.

- 核心练习仍可依赖浏览器本地存储运行；登录、排行榜和挑战成绩同步现已接入 Supabase。
- Core practice still works with browser storage, while sign-in, leaderboard ranking, and challenge sync now run through Supabase.

- 内置机械键盘风格打字音效，可按需开启或关闭。
- Includes optional mechanical keyboard style typing sounds.

## 技术栈 | Tech Stack

- React 18
- Vite 5
- Tailwind CSS

## 本地运行 | Local Development

```bash
npm install
npm run dev
```

## 云端配置 | Cloud Configuration

如果你需要启用云端登录与挑战排行榜，请在本地 `.env` 中配置以下变量：
If you want cloud sign-in and the challenge leaderboard, configure these variables in your local `.env` file:

```bash
VITE_SUPABASE_URL=
VITE_SUPABASE_PUBLISHABLE_KEY=
```

## 构建 | Build

```bash
npm run build
```

## 数据与隐私 | Data and Privacy

当前版本仍会把练习进度、设置和大部分训练反馈保存在浏览器本地存储中；但云端登录、排行榜、个人最佳成绩和管理员能力依赖外部 Supabase 服务。  
The current version still stores practice progress, settings, and most training feedback in browser local storage, but cloud sign-in, leaderboard data, personal best runs, and admin actions depend on Supabase.
