# SceneWalk
Bridge the screen and the street. An elegant travel companion app for tracking filming locations, celebrity footprints, and pop culture landmarks.
# 📸 FrameThrough (时空相机)

> **"Step into the scene."**  
> 一款开源的 AI 驱动“圣地巡礼与名场面复刻”旅行导航工具。收集全球电影、动画、历史事件与经典建筑的绝佳拍照机位，带你穿越时空，1:1 精准重现视觉名场面。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Build Status](https://img.shields.io/badge/build-passing-brightgreen)](#)

---

## 🌟 为什么发起这个项目？

旅行不仅仅是“我到过这里”，更是“我与这个地方产生过共鸣”。
我们经常在电影、动漫或历史老照片里被某个画面深深震撼，但当我们亲自到达那座城市时，却往往因为找不到确切的**拍摄机位、角度与焦段**而留下遗憾。

**FrameThrough** 旨在结合 AI 技术与社区的力量，建立全球最大的**时空名场面机位库**。通过 AR 叠图相机、机位识别与路线规划，让每一次打卡都变成一场穿越时空的仪式。

---

## 🚀 核心功能亮点

* **📍 精准时空机位库 (Pilgrimage Spot Directory)**：收录影视取景地、历史名场面、知名建筑与小众震撼视角，标注精确经纬度与推荐拍摄时间。
* **📸 AR 半透明对齐相机 (Overlaid Frame Camera)**：取景器实时叠加经典剧照/原图，支持透明度自由调节，助你 1:1 完美复刻名场面。
* **🤖 AI 图搜机位 (AI Spot Finder)**：上传任意电影截图或老照片，AI 自动反向识别其在真实世界中的拍摄地点与大概视角。
* **🎞️ 穿越打卡卡片 (Pass-Through Card Generator)**：一键合成“经典原图 vs 现地复刻照”对比图，自带城市气泡与专属印章，方便分享至社交平台。

---

## 🛠️ 技术栈

* **Front-end**: React Native (Expo) / Next.js (PWA)
* **Styling**: Tailwind CSS
* **Mapping**: Mapbox GL / Leaflet.js
* **Backend & DB**: Supabase (PostgreSQL + PostGIS)
* **AI Engine**: Vision LLMs (GPT-4o / Claude 3.5 Sonnet) + Vector Search

---

## 📦 数据格式规范 (Spot Schema Specification)

本项目非常依赖社区的力量来扩充机位库！所有机位数据存放在 `/data/spots/` 目录下，以 JSON 格式存储。

数据格式示例如下：

```json
{
  "id": "tokyo-suga-shrine-01",
  "title": "须贺神社阶梯",
  "source": {
    "type": "anime",
    "name": "《你的名字。》",
    "scene_description": "立花泷与宫水三叶在阶梯擦身而过的经典结尾画面"
  },
  "location": {
    "country": "Japan",
    "city": "Tokyo",
    "address_zh": "东京都新宿区须贺町 5-6",
    "coordinates": {
      "latitude": 35.685382,
      "longitude": 139.722883
    }
  },
  "shooting_guide": {
    "reference_image_url": "[https://assets.framethrough.org/spots/suga-shrine.jpg](https://assets.framethrough.org/spots/suga-shrine.jpg)",
    "recommended_focal_length": "50mm",
    "camera_height": "eye-level",
    "best_time_of_day": "15:00 - 17:00 (Sunset)",
    "tips": "站在阶梯底部朝上拍摄，避开早晚高峰人流。"
  },
  "contributor": "@github_handle" 
}
