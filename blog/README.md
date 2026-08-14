# 电力电子 × AI 学习博客

LLM / Agent 驱动的微电网与电力电子控制学习笔记，基于 GitHub Pages 发布。

## 目录结构

```
blog/
├── index.html              # 博客首页（文章列表）
├── posts/                  # 博客文章
│   └── 2026-08-14-persona-multiagent.html   # 博客10：PersonaLLM × Multi-Agent
└── README.md               # 本说明
```

## 如何发布到 GitHub Pages

### 方法一：用户主页（推荐，URL 最简洁）

1. 在 GitHub 新建仓库，名字必须是：`你的用户名.github.io`
   （例如用户名是 `zhangsan`，仓库名就是 `zhangsan.github.io`）
2. 把这个 `blog` 文件夹里的**所有内容**推送到仓库根目录
3. 打开仓库 Settings → Pages → Source 选 `Deploy from a branch` → 分支选 `main` → 保存
4. 等 1~2 分钟，访问 `https://你的用户名.github.io` 即可看到博客

### 方法二：普通仓库的 Pages

1. 新建任意仓库（如 `blog`）
2. 推送内容后，Settings → Pages → 选择 `main` 分支 / `root` 目录
3. 访问 `https://你的用户名.github.io/blog`

## 命令速查

```bash
# 首次推送
git init
git add .
git commit -m "init blog"
git branch -M main
git remote add origin https://github.com/你的用户名/你的用户名.github.io.git
git push -u origin main
```

## 添加新博客

1. 把新文章保存为 `posts/YYYY-MM-DD-标题.html`（日期命名，便于排序）
2. 在 `index.html` 的文章列表里加一个新的 `.post-card`
3. 推送即可

## 博客规划（12 篇）

| 编号 | 主题 |
|------|------|
| 2 | PID 参数整定入门 |
| 3 | 逆变器控制入门 |
| 4 | 6月回顾：从变换器到文献矩阵 |
| 5 | MPPT 算法三兄弟对比 |
| 6 | 下垂控制 vs VSG |
| 7 | RL 控制器 vs PI 控制器 |
| 8 | RL vs MPC for Microgrid |
| 9 | LLM 预测替代 LSTM 的可行性 |
| 10 | ✅ RAG 电力故障诊断系统（已写） |
| 11 | ✅ PersonaLLM 驱动的微电网 Multi-Agent（已写） |
| 12 | 约束感知决策的电力安全意义 |
| 13 | 自然语言→微电网控制 |
