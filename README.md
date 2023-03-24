# AI-Plugins

🔥 A registry of plugins that ChatGPT or any GPT can use!

As described in the [ChatGPT docs](https://platform.openai.com/docs/plugins/getting-started), every plugin requires a ai-plugin.json file, which needs to be hosted on the API’s domain. For example, a company called example.com would make the plugin JSON file accessible via an https://example.com domain since that is where their API is hosted. GPT services like ChatGPT look for a file located at /.well-known/ai-plugin.json. Here is a registery so you can discover, compare and develop your own plugins

## Plugins

|  Name     |  ChatGPT launch  |  Docs  |  Manifest  |  OpenAPI spec  |
|-----------|------------------|--------|------------|----------------|
| [Datasette](https://datasette.io/)      | no  | [Blogpost](https://simonwillison.net/2023/Mar/24/datasette-chatgpt-plugin/) | [AI Plugin](https://datasette.io/.well-known/ai-plugin.json) | [YAML](https://datasette.io/-/chatgpt-openapi-schema.yml)  | 
| [Expedia](https://www.expedia.com/)     | yes |   |   |   |
| [FiscalNote](http://wolfram.com/)       | yes |   |   |   |
| [Instacart](https://www.instacart.com/) | yes |   |   |   |
| [Kayak](https://www.kayak.com/)         | yes |   |   |   |
| [Klarna](https://www.klarna.com/)       | yes |   | [AI Plugin](https://www.klarna.com/.well-known/ai-plugin.json) | [JSON](https://www.klarna.com/us/shopping/public/openai/v0/api-docs/) |
| [Milo](https://www.joinmilo.com/)       | yes |   | [AI Plugin](https://www.joinmilo.com/.well-known/ai-plugin.json) | [YAML](https://www.joinmilo.com/openapi.yaml) |
| [OpenTable](https://www.opentable.com/) | yes |   |   |   |
| [Shopify](https://www.shopify.com/)     | yes |   |   |   |
| [Slack](https://slack.com/)             | yes |   | [AI Plugin](https://slack.com/.well-known/ai-plugin.json) | [YAML](https://api.slack.com/specs/openapi/ai-plugin.yaml) | 
| [Speak](https://www.speak.com/)         | yes |   | [AI Pllugin](https://api.speak.com/.well-known/ai-plugin.json) | [YAML](https://api.speak.com/openapi.yaml) |
| [Wolfram](http://wolfram.com/)          | yes | [Blogpost](https://writings.stephenwolfram.com/2023/03/chatgpt-gets-its-wolfram-superpowers/) | [AI Plugin](https://www.wolframalpha.com/.well-known/ai-plugin.json) | [JSON](https://www.wolframalpha.com/.well-known/apispec.json) |
| [Zapier](https://www.speak.com/)        | yes |   | [AI Plugin](https://www.zapier.com/.well-known/ai-plugin.json) | [JSON](https://nla.zapier.com/api/v1/dynamic/openapi.json)  |
