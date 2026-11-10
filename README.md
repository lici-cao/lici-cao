# 你好，我是 lici-cao 👋

*[English](README.en.md) · 简体中文*

我做能落到桌面上、被人真正用起来的产品：用 Spring Boot + Vue 搭前后端分离的系统，再用 GitHub Actions 云端构建、jpackage 打包成双击即用的 Windows 安装程序。比起把 demo 跑通，我更在意它在别人的电脑上能不能顺利装起来、用得下去、出问题能不能自己恢复。

[全部项目](https://github.com/lici-cao?tab=repositories) · [AI 应用](#-ai-应用) · [课程与系统实践](#-课程与系统实践) · [技术栈](#-常用技术)

---

## 📝 目前在做的：FitLife

把训练计划从「凭感觉」变成「可执行」。FitLife 是一套基于 AI 的健身运动计划智能生成系统，以 100 条已审核的动作库为知识源，把用户画像、规则筛选和大模型编排串成一条可校验的链路，最后产出每天能照着练的动作、组次、RPE 与预估热量。

[fitlife-desktop](https://github.com/lici-cao/fitlife-desktop) · Spring Boot 3 + Vue 3

饮食与运动记录、热量收支可视化、BMI / BMR / TDEE 测算，以及一个工作台式的 AI 对话页。

对话即执行：说「帮我生成一周减脂计划，只有哑铃，膝盖不好」，系统会真的按限制条件选出动作、编排成一周计划并落库；说「今天练胸怎么搭配」，它会从动作库里挑出一组带组次和动作要领的结构化动作卡。

模型自选与降级设计：对话页底部可切换 DeepSeek、豆包、GLM；没配 Key 的模型置灰提示，AI 不可用时自动回落到内置规则引擎，功能依然完整，界面不会白屏。

面向交付而不是演示：一键脚本做幂等数据库迁移，后端启动自动补齐动作库；桌面版走云端构建打成 Windows 安装包，仓库里不存任何明文 Key。

---

## 🧠 AI 应用

让模型做它擅长的事，把校验和兜底留在工程这一侧。

🍎 [**FitLife**](https://github.com/lici-cao/fitlife-desktop) · Java

AI 健身计划生成系统。动作库检索增强（RAG）+ 规则筛选 + 大模型编排，exerciseId 越界即丢弃；统一 `LlmGateway` 对接多家 OpenAI 兼容模型，支持 SSE 流式输出与对话页自选模型。

🤖 [**ASu-skills**](https://github.com/lici-cao/ASu-skills)

面向求职与开发场景的实用 AI Skills 集合，支持简历优化、岗位投递、面试准备与开发提效。

---

## 🖥️ 课程与系统实践

把课本上的分层架构写成能跑、能演示的完整系统。

📦 [**jxcexample**](https://github.com/lici-cao/jxcexample) · Java

进销存管理系统示例，包含商品、库存、单据与统计的完整业务闭环，可直接作为课程设计基础。

📚 [**booksmanagement**](https://github.com/lici-cao/booksmanagement) · Java

图书管理系统，用于补齐课程作业的经典增删改查与权限练习。

🎵 [**licimusic**](https://github.com/lici-cao/licimusic) · JavaScript

一款以电影镜头、粒子视觉和歌词舞台为核心的沉浸式音乐播放器。

---

## 🛠️ 常用技术

| 层次 | 技术 |
| --- | --- |
| 后端 | Java 17、Spring Boot 3、Spring Security、JWT、Spring Data JPA |
| 前端 | Vue 3、TypeScript、Vite、Element Plus、Pinia、ECharts |
| 数据 | MySQL 8（utf8mb4）、幂等迁移脚本 |
| AI | DeepSeek、豆包（火山方舟）、智谱 GLM，统一 OpenAI 兼容网关 + SSE 流式 |
| 交付 | GitHub Actions 云端构建、jpackage 打包 Windows 安装包、一键启动脚本 |

---

如果你在这里找到能解决自己问题的项目，欢迎直接试用，并在对应仓库的 Issues 里告诉我哪里不好用。真实的反馈，往往就是下一次改进的起点。
