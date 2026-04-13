# 🌅 每日晨报 - 语音新闻报告

## 任务配置

- **触发时间**：每天 8:00（北京时间）
- **新闻源优先级**：
  1. 🌐 国际新闻（全球动态、科技进展）
  2. 💰 财经市场（股市、经济政策、商业资讯）
- **输出方式**：Feishu → TTS 语音消息
- **内容格式**：简洁摘要（每条约 1-2 分钟）

## 实现逻辑

```bash
# 每日清晨触发检查
if [ $(date +%H) == "08" ]; then
  fetch_news --sources="international,finance" --limit=5
  generate_audio --text=$news_summary --provider=openai
  send_message --channel=feishu --tts=true --audio=data:audio/mp3;base64,...
fi
```

## 工作流程

1. ⏰ **8:00** - 定时任务触发，开始检查新闻源
2. 📰 **查询新闻** - 获取最新国际和财经新闻（5-10 条）
3. ✍️ **生成摘要** - 筛选重要事件，撰写简要报道
4. 🎤 **TTS 合成** - 将文本转换为语音
5. 📤 **发送消息** - 通过 Feishu 发送给用户

## 使用说明

- 首次使用需要配置新闻源 API（如 NewsAPI、RSS 聚合等）
- TTS 语音质量：OpenAI ElevenLabs 或 Microsoft Azure
- 如需调整触发时间、新闻源或格式偏好，请编辑此文件

---

*自动创建的定时任务配置 | 最后更新：2026-04-02*