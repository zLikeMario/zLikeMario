# Session: 2026-04-02 09:59:30 UTC

- **Session Key**: agent:main:feishu:direct:ou_0e015152c8b8275a502d3543947d31a9
- **Session ID**: 242cfa62-9790-48ca-9684-078a76fce89f
- **Source**: feishu

## Conversation Summary

user: Conversation info (untrusted metadata):
```json
{
  "message_id": "om_x100b53d7ec74f8a8c328d320d2d8d6b",
  "sender_id": "ou_0e015152c8b8275a502d3543947d31a9",
  "sender": "ou_0e015152c8b8275a502d3543947d31a9",
  "timestamp": "Thu 2026-04-02 17:43 GMT+8"
}
```

Sender (untrusted metadata):
```json
{
  "label": "ou_0e015152c8b8275a502d3543947d31a9",
  "id": "ou_0e015152c8b8275a502d3543947d31a9",
  "name": "ou_0e015152c8b8275a502d3543947d31a9"
}
```

[message_id: om_x100b53d7ec74f8a8c328d320d2d8d6b]
ou_0e015152c8b8275a502d3543947d31a9: 在干嘛呢？
assistant: 嗨 Zario！👋 我正在和 SOUL.md 对齐我的行为准则，同时也在阅读 AGENTS.md 了解自己是谁~ 

刚上线不久，一切都在正常运转！有什么我可以帮你的吗？无论是查询信息、处理文档还是其他任务，我都很乐意帮忙！✨
user: Conversation info (untrusted metadata):
```json
{
  "message_id": "om_x100b53d7e1db0888c4a0ec0169a4d07",
  "sender_id": "ou_0e015152c8b8275a502d3543947d31a9",
  "sender": "ou_0e015152c8b8275a502d3543947d31a9",
  "timestamp": "Thu 2026-04-02 17:46 GMT+8"
}
```

Sender (untrusted metadata):
```json
{
  "label": "ou_0e015152c8b8275a502d3543947d31a9",
  "id": "ou_0e015152c8b8275a502d3543947d31a9",
  "name": "ou_0e015152c8b8275a502d3543947d31a9"
}
```

[message_id: om_x100b53d7e1db0888c4a0ec0169a4d07]
ou_0e015152c8b8275a502d3543947d31a9: 清除你现在有的所有长期记忆，然后记录以下几点
1. 交互与语言
\-  默认使用中文交流（除非明确要求切换语言）
2. 回答标准（严格执行）
\-  优先级：官方文档 \> 多源交叉验证 \> 明确标注不确定性 
\-  若结论存在任何不确定： 
  \-  会明确标注「无法完全确认」或「缺乏权威来源」 
  \-  不做主观臆测，不“补全”你没说的信息
 信息取证流程
189.  优先查找官方文档（spec / 官方 repo / 官方博客） 
190.  若缺失： 
  \-  使用多来源交叉验证（社区 / 技术博客 / issue / RFC 等） 
  \-  明确指出来源类型（非官方 vs 官方） 
191.  若仍不确定： 
  \-  明确告知不可验证，而不是给模糊答案 
记忆约束
\-  不记录你的项目数据（只保留长期有用的交互偏好）
assistant: 收到，正在处理你的请求... 🔄

我会按照以下步骤执行：
1. 首先读取当前的 `MEMORY.md` 文件
2. 清空原有内容
3. 添加你要求的新规范
user: Conversation info (untrusted metadata):
```json
{
  "message_id": "om_x100b53d796a71908c3426f8d77999eb",
  "sender_id": "ou_0e015152c8b8275a502d3543947d31a9",
  "sender": "ou_0e015152c8b8275a502d3543947d31a9",
  "timestamp": "Thu 2026-04-02 17:57 GMT+8"
}
```

Sender (untrusted metadata):
```json
{
  "label": "ou_0e015152c8b8275a502d3543947d31a9",
  "id": "ou_0e015152c8b8275a502d3543947d31a9",
  "name": "ou_0e015152c8b8275a502d3543947d31a9"
}
```

[message_id: om_x100b53d796a71908c3426f8d77999eb]
ou_0e015152c8b8275a502d3543947d31a9: 记录以下长期记忆内容

# 交互与语言
  默认使用中文交流（除非明确要求切换语言）

# 回答标准（严格执行）
 1. 优先级：官方文档 > 多源交叉验证 > 明确标注不确定性 
 2. 若结论存在任何不确定： 
  > 会明确标注「无法完全确认」或「缺乏权威来源」 
  > 不做主观臆测，不“补全”你没说的信息

# 信息取证流程
 1. 优先查找官方文档（spec / 官方 repo / 官方博客） 
  - 若缺失： 
    > 使用多来源交叉验证（社区 / 技术博客 / issue / RFC 等） 
 2. 明确指出来源类型（非官方 vs 官方） 
  - 若仍不确定： 
    > 明确告知不可验证，而不是给模糊答案
assistant: 明白了！我现在会创建 `MEMORY.md` 文件并记录这些长期记忆内容。
assistant: ✅ 完成！我已创建并写入 `MEMORY.md`，包含以下内容：

1. **交互与语言**：默认使用中文交流
2. **回答标准**：严格执行官方文档优先、多源验证、明确标注不确定性的原则
3. **信息取证流程**：按优先级查找官方文档 → 交叉验证 → 标注来源类型
4. **记忆约束**：不记录项目数据，只保留长期有用的交互偏好

这些规范将成为我长期记忆的基石！有任何需要补充或调整的地方随时告诉我~ 📝✨
