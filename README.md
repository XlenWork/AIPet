# 🐾 AI Pet - Your Desktop Companion

A cute AI pet that lives on your desktop. It proactively cares about you, reminds you to take breaks, and keeps you company while you work.

**Not just a chatbot — a living desktop buddy with a soul.**

[中文文档](#中文说明)

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🐱 **Desktop Pet** | Walks around your screen, reacts to your actions |
| 💬 **Proactive Chat** | Initiates conversations, checks on your mood |
| ⏰ **Health Reminders** | Sedentary alerts, hydration reminders, rest prompts |
| 📝 **Mood Diary** | Tracks your emotions, provides comfort when you're down |
| 🎯 **Focus Mode** | Pomodoro timer + pet companionship for productivity |
| 🎨 **Costume System** | Hundreds of outfits to customize your pet |
| 🌤️ **Weather & Schedule** | Morning briefings with weather and daily agenda |
| 🧠 **Behavior Learning** | Adapts to your habits over time |
| 🎵 **Context Music** | Background music that matches your activity |
| 🐸 **Mini Games** | Frog travel & rhythm games for fun breaks |

## 🚀 Quick Start

### Prerequisites

- Python 3.9+
- An AI API key (DeepSeek / OpenAI / GLM / Qwen / Ollama)

### Install

```bash
git clone https://github.com/YOUR_USERNAME/ai-pet.git
cd ai-pet
pip install -r ai_pet/requirements.txt
```

### Run

```bash
python ai_pet/main.py
```

On first launch, a setup wizard will guide you through:
1. Naming your pet
2. Configuring your AI provider & API key
3. Setting your city for weather

### Build (Windows)

```bash
python build.py
```

Output: `dist/AI宠物/AI宠物.exe`

## 🌍 Languages

- 🇨🇳 Chinese (default, fully supported)
- 🇺🇸 English (i18n framework ready, UI translation in progress)

## 💰 Pricing Model

**All local features are FREE. Only AI capabilities require a subscription.**

| | Free | Pro ¥9.9/mo | Ultimate ¥19.9/mo |
|---|---|---|---|
| Local features (costume/diary/focus/social) | ✅ | ✅ | ✅ |
| AI chat | 20/day | 500/day | Unlimited |
| Advanced chat modes | ❌ | ✅ | ✅ |
| Mood diary analysis | ❌ | ✅ | ✅ |
| Smart assistant | ❌ | ✅ | ✅ |
| Custom personality | ❌ | ❌ | ✅ |
| Cloud sync | ❌ | ❌ | ✅ |

Invite 3 friends → unlock 7 days of Pro for free!

## 🏗️ Architecture

```
ai_pet/
├── main.py              # Application entry & orchestration
├── config.py            # Configuration & path management
├── ai_config.py         # AI model provider presets
├── log_utils.py         # Unified logging system
├── core/                # Business logic
│   ├── pet_state.py     # Pet state management (hunger/mood/clean)
│   ├── pet_ai.py        # AI conversation engine
│   ├── pet_widget.py    # Desktop pet widget
│   ├── pet_animation.py # Sprite animation system
│   ├── i18n.py          # Internationalization
│   ├── premium.py       # Subscription & feature gating
│   ├── share_invite.py  # Viral invitation system
│   └── ...              # 20+ feature modules
├── ui/                  # PyQt5 UI components
│   ├── design_system.py # Centralized design tokens
│   ├── welcome_wizard.py
│   ├── chat_window.py
│   ├── upgrade_dialog.py
│   └── ...
├── chat/                # Chat client/server
├── plugins/             # Plugin system
└── assets/              # Pet sprites & icons

ai_pet_cloud_server/     # Optional cloud backend
landing/                 # Product landing page
tests/                   # 66 unit tests
```

## 🧪 Testing

```bash
pip install pytest
python -m pytest tests/ -v
```

## 📦 Supported AI Providers

| Provider | API Base | Model | API Key Required |
|----------|----------|-------|-----------------|
| DeepSeek (Volcengine) | ark.cn-beijing.volces.com | deepseek-v3 | Yes |
| DeepSeek (Official) | api.deepseek.com | deepseek-chat | Yes |
| OpenAI | api.openai.com | gpt-4o-mini | Yes |
| GLM (Zhipu) | open.bigmodel.cn | glm-4-flash | Yes |
| Qwen (Alibaba) | dashscope.aliyuncs.com | qwen-turbo | Yes |
| Ollama (Local) | localhost:11434 | qwen2.5:7b | No |

## 🛡️ Privacy

- All data stored **locally** on your device
- AI conversations use official encrypted APIs
- No data uploaded to any server (unless you self-host the cloud server)
- API keys stored in local `config.json` only

## 📄 License

MIT License - see [LICENSE](LICENSE)

---

<a id="中文说明"></a>

## 🐾 AI宠物 - 你的桌面小伙伴

一只住在你电脑桌面上的AI宠物，会主动关心你、提醒你休息、陪你专注工作。

**不是冷冰冰的AI，是有温度的陪伴。**

### 快速开始

```bash
git clone https://github.com/YOUR_USERNAME/ai-pet.git
cd ai-pet
pip install -r ai_pet/requirements.txt
python ai_pet/main.py
```

首次启动会引导你：命名宠物 → 配置AI模型 → 设置城市

### 变现模式

**本地功能全部免费，只为AI能力付费。**

- 免费版：全部本地功能 + AI对话每日20次
- 专业版 ¥9.9/月：AI对话500次/天 + 高级AI功能
- 旗舰版 ¥19.9/月：无限AI对话 + 全部功能

邀请3位好友 → 免费获得7天专业版！

### 技术栈

- **UI**: PyQt5 + 自定义设计系统
- **AI**: OpenAI SDK (兼容 DeepSeek/GLM/Qwen/Ollama)
- **数据**: SQLite 本地存储
- **打包**: PyInstaller → Windows 可执行文件
- **测试**: pytest (66个测试用例)

### 隐私保护

- 所有数据存储在本地
- AI对话通过官方加密API传输
- 不上传任何用户数据
- API密钥仅保存在本地配置文件
