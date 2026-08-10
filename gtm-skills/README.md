# GTM Skills 工具包

一套可以在WorkBuddy上复用的GTM技能包，10个skill：市场调研、ICP自动研究、
找公司名单、信息补充、打分、话术库、个性化生成、每日编排、追踪看板、回复处理。

ICP和打分逻辑不是手写进去的，是skill自己跑市场调研（去竞品的case study、
G2/Capterra评论区）研究出来的——每个新项目只需要填两个几行字的小文件，剩下
的skill自己推理。同一套skill可以直接套用在任何新产品上。

这个包已经帮你把文件夹结构建好了，解压后就是这个样子：
```
gtm-skills/
├── skills/                          ← 10个skill，每个一个SKILL.md
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
│   └── dolphin-ai/00_ICP/           ← 一个已经填好的真实案例，照着抄
│       ├── product_seed.md
│       └── operational_config.md
└── README.md                        ← 就是这份文档
```

## 怎么用（团队里任何人，从0开始）

### 第一次使用这个包
1. 解压这个zip，得到`gtm-skills`文件夹
2. 打开`skills/`下每个子文件夹里的`SKILL.md`，把内容复制粘贴到WorkBuddy里，
   存成对应名字的persistent skill（跟建普通skill操作一样，10个都要建）

### 用在一个已有项目上（比如Dolphin AI）
直接跑`gtm-pipeline`，告诉它"project: dolphin-ai"即可——ICP、打分规则、
运营参数都已经在`projects/dolphin-ai/00_ICP/`里配好了。

### 用在一个全新的产品上（比如下次的新项目）
1. 在`projects/`下新建一个文件夹，用产品的英文名命名
2. 参考`projects/dolphin-ai/00_ICP/`里的两个文件，照着格式填自己产品的
   `product_seed.md`（4行：一句话介绍、差异化点、已知客户、硬性约束）和
   `operational_config.md`（找公司的信息来源、每天发送量、渠道、语气规则）
3. 依次跑`market-researcher` → `research-icp`（这两步skill自己研究出ICP和
   打分逻辑，不用手写）→ 打开生成的`icp_confidence_notes.md`看一眼确认没问题
4. 之后每天跑`gtm-pipeline`就行

新项目全程不用建新skill、不用问怎么写ICP——这就是这个包存在的意义。

## 上传到GitHub（给团队共享）

1. github.com 注册账号（没账号的话）
2. 新建一个仓库（New repository），名字建议就叫`gtm-skills`，选Private
3. 进仓库页面，点"Add file" → "Upload files"，把解压出来的`gtm-skills`
   文件夹里的所有内容拖进去（如果网页不支持直接拖文件夹，就把这个zip文件
   本身直接拖上去上传，之后同事下载时也是下载整个zip，一样能用）
4. 填一句提交说明，点绿色"Commit changes"
5. Settings → Collaborators → 加同事的GitHub账号，邀请他们

## 同事怎么用
1. 打开你分享的仓库链接，点"Code" → "Download ZIP"
2. 解压，按上面"第一次使用这个包"的步骤，把10个skill存进自己的WorkBuddy
3. 需要跑自己的新项目，就按"用在一个全新的产品上"那几步操作

## 以后更新
改进某个skill：打开GitHub仓库里对应的SKILL.md文件，点右上角铅笔图标直接在
网页编辑，改完点"Commit changes"，同事重新下载ZIP就能拿到新版。
