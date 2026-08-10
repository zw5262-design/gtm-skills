# GTM Skills 工具包

一套可以在WorkBuddy上复用的GTM技能包，10个skill：市场调研、ICP自动研究、
找公司名单、信息补充、打分、话术库、个性化生成、每日编排、追踪看板、回复处理。

```
gtm-skills/
├── skills/                          
│   ├── 01-market-researcher/
│   ├── 02-research-icp/
│   ├── 03-list-builder/
│   ├── 04-enrich-basic/
│   ├── 05-score-leads/
│   ├── 06-template-library/
│   ├── 07-sequence-builder/
│   ├── 08-gtm-pipeline/
│   ├── 09-run-tracker/
│   └── 10-reply-handler/
├── projects/
│   └── dolphin-ai/00_ICP/           ← Dolphin AI真实案例，供参考
│       ├── product_seed.md
│       └── operational_config.md
└── README.md                        
```

## 怎么用

### 第一次使用这个包
1. 解压这个zip，得到`gtm-skills`文件夹
2. 打开`skills/`下每个子文件夹里的`SKILL.md`，把内容复制粘贴到WorkBuddy里，
   存成对应名字的persistent skill（跟建普通skill操作一样，10个都要建）

### 用在一个全新的产品上
1. 在`projects/`下新建一个文件夹，用产品的英文名命名
2. 参考`projects/dolphin-ai/00_ICP/`里的两个文件，照着格式填自己产品的
   `product_seed.md`（4行：一句话介绍、差异化点、已知客户、硬性约束）和
   `operational_config.md`（找公司的信息来源、每天发送量、渠道、语气规则）
3. 依次跑`market-researcher` → `research-icp`（这两步skill自己研究出ICP和
   打分逻辑，不用手写）→ 打开生成的`icp_confidence_notes.md`看一眼确认没问题
4. 之后每天跑`gtm-pipeline`就行
