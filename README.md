# icpc-gfw
Banning common websites via Clash in the ICPC.

## 一、实际屏蔽的内容

**1. 搜索引擎（11）**
Bing（bing.com/bingapis）、百度（整域，同时覆盖知道/百科/经验/文库/网盘/贴吧）、搜狗（含微信搜索）、360搜索、神马、夸克（含网盘/题库）、秘塔AI搜索、纳米AI搜索、头条搜索、Yahoo Japan

**2. 国内 AI 大模型**
DeepSeek、通义千问（tongyi/qianwen/qwen.ai）、Kimi、智谱GLM（zhipuai/chatglm/bigmodel）、豆包、文心一言、腾讯元宝、腾讯混元、讯飞星火、天工、360智脑、商汤日日新/商量、海螺/MiniMax、百川、零一万物、阶跃星辰、面壁、扣子Coze、可灵、即梦、Liblib、魔搭ModelScope、小米MiMo、无问芯穹、hf-mirror、Trae、GitHub Copilot

**3. 大模型 API 中转站 / 聚合平台（48）**
ChatAnywhere、AiHubMix、302.AI、OhMyGPT、CloseAI、OpenAI-HK（open-hk/openai-hk）、API2D、GPTGOD、V3API、硅基流动、API易、HenAPI、非线、Ofox、PoloAPI、4SAPI、147API、V-API(gpt.ge)、AICodeMirror、AnyAIGC、code0、接口AI、WenModel、aiberm、deepkey、SkyHope、星链API、FK Claude、IKunCode、X-aio、Alsa、小米API、APIMan、QQQRouter、老张API、兔子API、CatRouter、PackyAPI、DMXAPI，以及官方端点：DashScope/百炼、火山方舟、千帆、混元API、星火API

**4. 视频与流媒体**
B站（含 bilivideo CDN）、抖音、快手、优酷、爱奇艺、腾讯视频、芒果TV、搜狐视频、乐视、西瓜、梨视频、AcFun、抖音火山版、微视、微信视频号、PPTV、斗鱼、虎牙

**5. 社区**
知乎（含直答/专栏）、小红书、微博（.com/.cn）、豆瓣

**6. 博客**
CSDN、博客园、掘金、思否、简书、OSCHINA、51CTO、InfoQ、Stack Overflow、Stack Exchange 全系、菜鸟教程、W3School、GeeksforGeeks、DEV、新浪博客、微信公众号文章、看云

**7. 文库与搜题软件**
豆丁、道客巴巴、原创力Book118、人人文库、360doc、爱问共享、MBA智库、作业帮（zybang/zuoyebang）、小猿/猿辅导、学小易、Chegg、Course Hero、StuDocu、Scribd、Quizlet、Brainly

**8. 在线文档 / 云笔记**
MS365/Office、OneDrive（含1drv）、SharePoint、OneNote、WPS、金山文档kdocs、docer、飞书（整域，含邮箱）、Lark、腾讯文档、石墨、语雀、Notion（含 notion.site 发布页）、Obsidian（Sync/Publish）、HackMD、印象/Evernote、有道云笔记、为知、幕布、Confluence/Jira、ProcessOn、boardmix、Logseq、XMind

**9. 网盘 / 在线粘贴板**
阿里云盘（含旧域）、微云、115、蓝奏云、奶牛快传、文叔叔、迅雷云盘、123云盘、天翼云盘、移动云盘、AirDroid、Send Anywhere、SM.MS 图床、Pastebin、JustPaste

**10. PDF批注软件**
GoodNotes、Notability、MarginNote、Noteshelf、CollaNote、LiquidText、AnkiWeb、RemNote、MindNode

**11. 代码托管仓库**
GitHub 全系（含 usercontent/assets/io）、Gitee、GitLab、极狐GitLab（gitlab.cn/jihulab）、Bitbucket、CODING、阿里云效Codeup、Azure DevOps/Visual Studio、Gitea、Codeberg、SourceHut、Launchpad、SourceForge、GNU Savannah、GitCode、AtomGit、OpenI、GitLink，及镜像加速 kkgithub/gitclone/ghproxy/gh-proxy

**12. 邮箱**
QQ邮箱、腾讯企业邮、Foxmail、网易系（163/126/yeah/188/企业邮）、新浪、搜狐、139邮箱（含10086/wapmail）、189邮箱（含wapmail）、沃邮箱、阿里邮箱（个人/企业）、21cn、TOM（含163.net）、263（个人/企业263xmail）、Outlook/Hotmail（含 live/office365）

## 二、注释掉的规则

| 分区 | 注释域名 | 注释原因 |
|---|---|---|
| AI（21） | openai、chatgpt、oaistatic、oaiusercontent、Google AI（generativelanguage/aistudio）、copilot（microsoft/.com）、claude.ai、anthropic、perplexity、grok、x.ai、character.ai、poe、huggingface、cursor（.com/.sh）、windsurf、codeium、openrouter | 国内直连不通，代理常开时再开启 |
| 视频（4） | youtube、ytimg、twitch、nicovideo | 同上 |
| 社交（2） | reddit、quora | 同上 |
| 博客（3） | medium、wordpress.com、blogspot | 同上 |
| 云文档（4） | Google Drive/Docs、Dropbox、icloud.com | 前三个直连不通；icloud 会连带屏蔽 Apple 备忘录/无边记 |
| 邮箱（5） | gmail、googlemail、proton.me、protonmail、yahoo.com | 国内直连不通 |
| 数学工具（5） | Wolfram Alpha、Symbolab、Mathway、Desmos、GeoGebra | 非不可访问，而是**考试若禁止计算器/数学工具才开启** |
