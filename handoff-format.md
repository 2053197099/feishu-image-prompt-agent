# 排版交接格式

JSON 与 image-prompt-layout 的输入结构兼容：

```json
{"items":[{"id":"record-001","image":"images/001.png","prompt":"原始提示词 --ar 3:4","label":"prompt","title":"可选作品名","description":"可选说明"}]}
```

每项一张完整原图与一段原文；ID 保留飞书来源记录 ID，数组顺序即排版顺序。图片路径相对清单文件，使用下载到当前交付包的文件，不填附件 token、未授权 URL 或另一个云任务的路径。

交付时把清单和 images 目录一起打包，由用户明确交给排版对话；也可在同一个已授权任务中调用排版 Skill。不能自动向其他聊天发消息。源提示词不翻译、删减或补写，读取失败与跳过记录另行报告。

禁止清单中包含 app_secret、access_token、cookie、授权头或带秘密参数的临时 URL。示例 ID 与提示词为虚构，不代表真实飞书数据。
