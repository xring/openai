# ChatGPT Plugin
[文档](https://platform.openai.com/docs/plugins/introduction)

## 准备 Plugin manifest 文件
每个 plugin 都要求有一个 `ai-plugin.json` 文件，这个文件需要在 API 的域名上，存放的位置为：https//example.com/.well-known/ai-plugin.json 如果安装 plugin 的时候找不到，则无法安装成功。

plugin 的最小化定义如下：
```json
{
  "schema_version": "v1",
  "name_for_human": "TODO Plugin",
  "name_for_model": "todo",
  "description_for_human": "Plugin for managing a TODO list. You can add, remove and view your TODOs.",
  "description_for_model": "Plugin for managing a TODO list. You can add, remove and view your TODOs.",
  "auth": {
    "type": "none"
  },
  "api": {
    "type": "openapi",
    "url": "http://localhost:3333/openapi.yaml",
    "is_user_authenticated": false
  },
  "logo_url": "https://vsq7s0-5001.preview.csb.app/logo.png",
  "contact_email": "support@example.com",
  "legal_info_url": "http://www.example.com/legal"
}
```
