# Best 桌宠服务器

宇宙第一聪明的桌宠 Otto 的本地大脑。

## 这是什么

一套跑在电脑上的 AI 桌宠后端，让 Otto（ESP32-S3 双足机器人）拥有完整的本地闭环能力：

- 语音识别（本地 SenseVoice）
- 大脑（DeepSeek API + 自定义人格）
- 联网（天气 / 新闻搜索）
- 动作控制（22 种舵机动作）
- 对话记忆
- 本体播报（外部 AI 直接驱动设备说话）

## 技术栈

- Go 后端（WebSocket / MQTT / UDP 多协议接入）
- SenseVoice 本地语音识别
- DeepSeek 大模型
- EdgeTTS 语音合成
- 设备 MCP 工具链（动作 / 状态 / 联网）

## 修改说明

本项目基于开源项目 [xiaozhi-esp32-server-golang](https://github.com/hackers365/xiaozhi-esp32-server-golang) fork 定制，遵循其开源许可协议。主要修改：

1. 修复 assistant 消息重复入历史导致的重复播报
2. 修复跨会话记忆丢失（去掉 session_id 过滤）
3. 自定义欢迎语

## 使用

详见项目文档目录 `doc/`。
