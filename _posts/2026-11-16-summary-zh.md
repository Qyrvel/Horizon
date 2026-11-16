---
layout: default
title: "Horizon Summary: 2026-11-16 (ZH)"
date: 2026-11-16
lang: zh
---

> 从 145 条内容中筛选出 21 条重要资讯。

---

**科技新闻**
1. [uBlock Origin 元素选择器曝通用 XSS，修复版发布](#item-tech-news-1) ⭐️ 8.0/10
2. [Qwen4-Max 上线：2.4 万亿参数 MoE 与 API 降价](#item-tech-news-2) ⭐️ 8.0/10
3. [Meta FAIR/NYU：视觉编码器预训练非必需，视觉专用参数必需](#item-tech-news-3) ⭐️ 8.0/10
4. [美团开源 LongCat-2.5：MIT 许可，称未用英伟达 GPU 训练](#item-tech-news-4) ⭐️ 8.0/10
5. [MacBook Pro OLED 的 PWM 闪烁争议](#item-tech-news-5) ⭐️ 7.0/10
6. [开源工具称将 B300 上 pageable cudaMemcpy 提速约 5 倍](#item-tech-news-6) ⭐️ 7.0/10

**全球时事与国际新闻**
1. [伊朗被指无人机袭击巴林境内美军基地 海湾局势再度紧张](#item-world-news-1) ⭐️ 8.0/10
2. [也门政府军撤出曼德海峡 胡塞武装逼近亚丁](#item-world-news-2) ⭐️ 7.0/10
3. [西班牙定于 11 月 29 日举行提前大选，极右翼可能首次进入政府](#item-world-news-3) ⭐️ 7.0/10
4. [爱沙尼亚称挫败针对无人机厂商的破坏行动，将于 12 月 1 日关闭全部对俄口岸](#item-world-news-4) ⭐️ 7.0/10
5. [捷克布拉格数十万人示威 反对公共广播经费改革](#item-world-news-5) ⭐️ 7.0/10
6. [国际法院将就缅甸是否对罗兴亚人实施种族灭绝作出裁决](#item-world-news-6) ⭐️ 7.0/10
7. [泰国普吉岛帕通商铺火灾致至少 11 人死亡](#item-world-news-7) ⭐️ 7.0/10
8. [半岛电视台实时报道：第三艘美国航母抵达中东，伊朗称不会坐等遭袭](#item-world-news-8) ⭐️ 7.0/10
9. [近 2200 名移民两天内抵达西班牙加那利群岛](#item-world-news-9) ⭐️ 7.0/10
10. [美国全国航班停飞事件预计恢复 政府称系通信线路更换失误](#item-world-news-10) ⭐️ 7.0/10

**财经新闻**
1. [中国 10 月消费、工业与投资数据全面低于预期](#item-finance-news-1) ⭐️ 8.0/10
2. [卢特尼克因英伟达相关风波面临质询，其子经营的坎托申报持股减少](#item-finance-news-2) ⭐️ 8.0/10
3. [美法官驳回美光三星等 DRAM 价格操纵案撤诉动议](#item-finance-news-3) ⭐️ 7.0/10
4. [中美俄领导人拟于 11 月 19 日在深圳 APEC 场边举行首次三方会晤](#item-finance-news-4) ⭐️ 7.0/10
5. [猪肉价格跌至近 10 年低位，11 月 9 日生猪均价每公斤 8.63 元](#item-finance-news-5) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [uBlock Origin 元素选择器曝通用 XSS，修复版发布](https://iter.ca/post/ubo-uxss/) ⭐️ 8.0/10

uBlock Origin 中由网站侧触发的元素选择器被披露存在通用跨站脚本（UXSS）漏洞，网页内容可成为触发路径，而不只限于扩展自身界面。披露包含概念验证，并给出修复版本：uBlock Origin 1.75.4 和 uBO Lite 2026.1110.1816。使用这些版本或更高版本可避开该问题；低于修复版本的用户仍处于受影响范围。

hackernews · zaik · 11月16日 02:04 · [社区讨论](https://news.ycombinator.com/item?id=50513160)

**「背景」** 通用 XSS（UXSS）指不依赖目标网站自身漏洞、借助浏览器或扩展的受信任上下文在页面中执行脚本的一类攻击，影响面通常跨越多个站点。uBlock Origin 的元素选择器要让用户直接在网页元素上点选并生成过滤规则；若这套扩展界面被放进网页 DOM，页面脚本就可能与它发生非预期交互，这也是一部分扩展 UI 设计长期存在的风险面。

**「影响与处置」** 仍在使用旧版的用户应尽快升级到 uBlock Origin 1.75.4 或 uBO Lite 2026.1110.1816 及以上；版本号是判断安装是否仍暴露于该漏洞的直接依据。

**「社区讨论」** 评论者把焦点放在扩展将交互界面放进网页 DOM 的设计上：ByteOfWood 认为元素选择器和密码管理器建议登录框可能让页面窥探扩展界面内容，甚至泄露账号信息；akersten 则追问为何不能把建规则界面放到浏览器 chrome 层。另有评论提醒检查版本，并建议为不同用途使用独立的 Firefox 配置文件。

**标签**: `#browser-security`, `#xss`, `#ublock-origin`, `#browser-extensions`, `#vulnerability-disclosure`

---

<a id="item-tech-news-2"></a>
### [Qwen4-Max 上线：2.4 万亿参数 MoE 与 API 降价](https://qwen.ai/blog?id=qwen4-max) ⭐️ 8.0/10

阿里通义千问正式发布新一代旗舰模型 Qwen4-Max，采用稀疏 MoE 架构，总参数达 2.4 万亿，原生支持视觉理解和百万 Token 长上下文。发布信息称其在编程、办公及长程任务上表现突出，前端编程能力在 Code Arena 盲测中位居全球前列。成本方面，官方称单任务平均费用从 26.58 元降至 11.16 元，降幅近 58%，Token 消耗减少近 50%，API 定价同步下调。模型已上线，团队表示后续将推出更小的 Qwen4 系列并公开权重。

hackernews · ilreb · 11月16日 02:14 · [社区讨论](https://news.ycombinator.com/item?id=50513215)

**「背景：稀疏 MoE 与上一代基线」** Qwen4-Max 采用稀疏 MoE（混合专家）架构：总参数达 2.4 万亿，但每次推理只激活其中一部分专家，所以总参数规模并不等于单次调用的算力成本；这也是理解其“单个任务平均费用从 26.58 元降至 11.16 元、Token 消耗减少近 50%”这类降本说法的前提。来源把这次变化描述为“相比上代”的优化，而社区讨论中则把 Qwen3.8 Max 当作直接对照的上一代模型；至于两代之间的具体版本关系和架构差异，现有材料并未给出细节。

**「对开发者的影响」** Qwen4-Max 已上线且 API 定价下调，需要长上下文、视觉理解和编程能力的团队可以将其纳入成本与延迟测试；但旗舰模型本次未开放权重，团队只承诺后续更小的 Qwen4 系列会公开权重，本地部署计划需相应调整。评论者引用的 Artificial Analysis 数据显示，Qwen4-Max 得分 43、平均成本 3.27 美元，而 GPT-6.1 Sol（medium）为 46 分、0.36 美元，选型时应按具体任务核算，而不只看官方降价幅度。

**「社区讨论」** 评论区的争论集中在开放权重模型是否正在拉大与 Anthropic、OpenAI 的差距：有评论者引用 Artificial Analysis 数据比较 Qwen4-Max 与 GPT-6.1 Sol 的得分和成本，也有人担心开放模型改进速度不及闭源对手。另有开发者肯定 Qwen 对效率和小模型的持续投入，但报告 Qwen 3.8 在 Agent 场景因约 30 tokens/s 的速度明显吃亏（对比 Opus 约 80 tokens/s），并期待后续 Flash 与 27B 版本。

**标签**: `#LLM`, `#Qwen`, `#model release`, `#AI benchmarks`, `#open weights`

---

<a id="item-tech-news-3"></a>
### [Meta FAIR/NYU：视觉编码器预训练非必需，视觉专用参数必需](https://www.reddit.com/r/MachineLearning/comments/1xx1k2o/meta_fair_nyu_unbundling_multimodal_vision/) ⭐️ 8.0/10

Meta FAIR 与 NYU 的作者在一项预印本研究中，用相同数据、把编码器预训练计入同一总计算预算，从零训练 200 多个多模态大模型，并在 16 个 Cambrian VQA 基准（448 px）和 12 个语言基准上评测，拆解了视觉编码器的三个选择。作者报告，单独预训练视觉编码器并非必需：对比学习、自监督和两种描述生成等四种预训练目标，在匹配计算下至多与从零联合训练打平，连“免费”预训练也无增益；把 MetaCLIP 预训练延长 6.5 倍只将 ImageNet 线性探针准确率从 80.4% 提高到 84.4%，VQA 不变。视觉专用参数则不可省：完全无编码器模型在 0.6B–6.4B 各规模均落后，约需 3 倍计算才能追上，而把编码器参数转给 LLM 只改善文本、不改善 VQA。编码器放在 LLM 之前同样可选：作者提出的 in-fusion 在 LLM 前 8 层加入零初始化、仅视觉 token 使用的权重，在 1.7B–6.4B 上与编码器相当，首 token 时间低约 13%。

reddit · r/MachineLearning · /u/trungh98 · 11月15日 17:38

**「背景」** 多模态大模型通常采用这样的视觉编码方案：先单独预训练视觉编码器，再把它放在 LLM 之前，并让视觉 token 使用一组专属参数。该研究指出，这种标准编码器实际上把三个可分开的选择捆绑在一起：是否单独预训练、是否保留视觉专用参数、是否放在 LLM 之前；已发布模型也体现了分歧，例如 Gemma 4 12B 去掉编码器、Kimi K3 从零训练编码器、Inkling 2 Small 重新引入编码器。

**「影响」** 对从零训练多模态模型的团队，这项作者报告的结果支持省去单独的视觉编码器预训练，并用 LLM 前 8 层的视觉专用分支替代前置编码器；但完全无编码器方案在 0.6B–6.4B 均落后、约需 3 倍计算才能追上，采用前仍需按自有数据和算力复现验证。其 in-fusion 变体在测试中把首 token 时间降低约 13%，适合对推理延迟敏感的配置。

**标签**: `#multimodal LLMs`, `#vision encoders`, `#pretraining`, `#ablation study`, `#model scaling`

---

<a id="item-tech-news-4"></a>
### [美团开源 LongCat-2.5：MIT 许可，称未用英伟达 GPU 训练](https://the-decoder.com/meituan-releases-a-1-6-trillion-parameter-agent-model-that-never-touched-an-nvidia-gpu/) ⭐️ 8.0/10

美团 LongCat 团队在模型发布一周后公开了 LongCat-2.5 的权重，这是一个面向自主完成冗长、多步骤任务（尤其是编程）的智能体模型。该模型每个 token 激活约 480 亿参数，支持文本、图像和视频输入，并以 MIT 许可证发布，允许商用。官方称其训练全程使用华为升腾加速卡、未使用英伟达 GPU；这一核心训练说法目前仅为厂商声明，尚未独立验证。在 Terminal Bench v2.1 上，LongCat-2.5 得分 88.4，略低于 Claude Opus 5 的 89.1。

telegram · zaihuapd · 11月15日 11:08

**「背景」** LongCat-2.5 的 1.6 万亿总参数与每 token 约 480 亿激活参数，意味着它采用稀疏混合专家（MoE）架构：推理时只调用部分专家，因此总参数量远大于单次前向实际计算量。此类规模模型的训练长期依赖英伟达 GPU，而在美国收紧高端 AI 芯片对华出口的背景下，华为升腾成为中国最主要的本土替代加速卡，这正是「训练全程未使用英伟达 GPU」这一说法受到关注的原因。

**「影响」** 对需要可商用、可修改开放权重的团队，MIT 许可证降低了部署和二次开发的法律门槛；但若要把“未使用英伟达 GPU 训练”作为选型依据，仍应等待独立复现或更完整的训练栈披露。

**标签**: `#open-source LLM`, `#Meituan LongCat`, `#Huawei Ascend`, `#AI agents`, `#model training`

---

<a id="item-tech-news-5"></a>
### [MacBook Pro OLED 的 PWM 闪烁争议](https://macanorak.com/the-macbook-pros-oled-pwm-problem-when-a-better-display-becomes-worse-to-use/) ⭐️ 7.0/10

MacAnorak 的一篇分析把 MacBook Pro OLED 屏幕的 PWM 闪烁列为实际使用问题，受影响的主要是对闪烁敏感的用户和潜在购买者。评论者围绕文中引用的 240Hz 测量展开争论：有人提出串联 OLED 两层各以 480Hz、相差 180 度工作，在常用亮度下可能形成 960Hz 的有效频率。上述频率来自读者讨论而非独立复测，文章的具体测试条件在现有材料中也未给出。

hackernews · MacAnorak · 11月15日 13:15 · [社区讨论](https://news.ycombinator.com/item?id=50506719)

**「PWM 与闪烁感知」** 这项讨论涉及 PWM 调光：屏幕通过快速开关像素并调整亮/灭占空比来改变亮度，而不是只靠降低驱动电流。人眼对闪烁的感知存在“闪烁融合阈值”，达到一定频率后多数人会看成稳定光源，但该阈值会受亮度、刺激大小和个体状态影响。

**「影响」** 对闪烁敏感的用户，选购前应关注 PWM 频率和调光方式，并尽量实际试用；评论中既有受影响者，也有人表示从未遇到问题，说明个体差异明显。

**「社区讨论」** legitronics 质疑 240Hz 结论，提出 480Hz 双层反相叠加可达 960Hz；achr2 则引用论文称人可感知高于显示屏刷新率两倍以上的闪烁，并表示惊讶 Apple 会采用如此低的 PWM 频率。另有评论者把闪烁敏感扩展到 LED 显色指数和 LCD 运动模糊，还有人报告脑震荡后对所有屏幕都更敏感。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Flicker_fusion_threshold">Flicker fusion threshold - Wikipedia</a></li>
<li><a href="https://opticquiz.com/flicker/">Flicker Fusion Test — Critical Flicker Frequency ... — OpticQuiz</a></li>

</ul>
</details>

**标签**: `#OLED`, `#PWM flicker`, `#display technology`, `#MacBook Pro`, `#hardware`

---

<a id="item-tech-news-6"></a>
### [开源工具称将 B300 上 pageable cudaMemcpy 提速约 5 倍](https://www.reddit.com/r/MachineLearning/comments/1xx2n25/making_cudamemcpy_5x_faster_on_a_b300_p/) ⭐️ 7.0/10

开发者发布开源工具 cudamemcpy-tuner（命令为 \`cmt\`），声称能加速 CUDA 中 pageable（可分页）内存的 cudaMemcpy 传输，并附有技术博客和 GitHub 代码。作者在 B300 上给出的示例是：用 PyTorch 将 1 GB 的 uint8 张量拷贝到 GPU，并运行 \`cmt tune -- python bench.py\`，速度从 10.2 GB/s 提升到 51.5 GB/s，约为 5 倍。这些数字来自作者自测，只覆盖单块 B300 和 CPU→GPU 这一个方向；目前没有第三方复现，也没有与固定内存（pinned memory）传输的对照。

reddit · r/MachineLearning · /u/makneeee · 11月15日 18:20

**「背景」** CUDA 的 cudaMemcpy 对可分页（pageable）主机内存与锁页（pinned）内存采用不同的实现路径：锁页内存可被驱动直接用于 DMA，而可分页内存通常要经过中间缓冲区，因此同样的主机—设备拷贝在两种内存上的带宽差距明显；NVIDIA 的 bandwidthtest 示例正是用来对比这两种传输速率。B300 属于 Blackwell Ultra 一代，其 HBM3e 显存带宽约为每 GPU 8 TB/s，所以主机与设备之间的互连往往才是这类拷贝的实际瓶颈。

**「影响」** 对使用 PyTorch 等框架、在没有固定（pin）主机内存的情况下直接调用 \`.to\(&quot;cuda&quot;\)\` 的开发者来说，这类拷贝走的正是 pageable 路径，因此该工具若确实有效，就能减少数据加载时的等待。但由于结果只在单卡上自测得出，实际使用前应先在目标 GPU 和数据规模上复现；固定内存加异步拷贝仍是常规优化手段，而且原帖没有说明该工具支持的 GPU 型号与 CUDA 版本范围。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.spheron.network/blog/nvidia-rubin-r100-guide/">NVIDIA Vera Rubin GPU Specs : HBM 4, FP4 &amp; Cloud... | Spheron</a></li>
<li><a href="https://developer.nvidia.com/blog/how-optimize-data-transfers-cuda-cc/">How to Optimize Data Transfers in CUDA C/C++ | NVIDIA Technical...</a></li>
<li><a href="https://www.linkedin.com/pulse/supercharging-data-transfers-cuda-power-page-locked-pinned-mohapatra-bejec">Supercharging Data Transfers in CUDA : The Power of Page-Locked...</a></li>

</ul>
</details>

**标签**: `#CUDA`, `#GPU performance`, `#memory transfer`, `#open source`, `#benchmarking`

---

## 全球时事与国际新闻

<a id="item-world-news-1"></a>
### [伊朗被指无人机袭击巴林境内美军基地 海湾局势再度紧张](https://www.theguardian.com/world/2026/nov/15/iran-launches-drone-attacks-against-us-military-base-in-bahrain) ⭐️ 8.0/10

据《卫报》11 月 15 日（周日）报道，伊朗对巴林境内一处美军基地发动无人机袭击，这是三天内第二次此类攻击。巴林外交部表示，当天进入巴林领空的无人机已被防空系统拦截并摧毁，并称伊朗伊斯兰革命卫队已公开宣称对此次袭击及 11 月 13 日的类似袭击负责。沙特阿拉伯、卡塔尔、约旦和埃及等国谴责袭击并表态声援巴林。报道未提供伤亡或设施损毁的评估，也没有给出美方的详细回应，袭击细节尚待独立确认。

rss · The Guardian - World · 11月15日 18:03

**「背景」** 报道称，这轮袭击结束了自 9 月以来海湾地区相对平静的局面；巴林当天两次发布潜在威胁警报，首都麦纳麦传出爆炸声。巴林外交部把袭击称为伊朗“侵略”的延续，称其违反国际法和《联合国宪章》，并称 11 月 13 日黎明来袭的两架无人机同样被拦截。报道指出，结束这场已持续约九个月的中东战争的外交努力仍无突破，美国维持海上封锁，伊朗则保持对霍尔木兹海峡的制约。

**「影响与风险」** 可以观察到的影响是：巴林启动防空拦截并两度发布威胁警报，多个阿拉伯国家公开谴责袭击、表态支持巴林，这说明冲突的外溢效应已直接触及海湾国家本土安全。潜在后果是：若袭击继续，伊朗与美国之间本已停滞的谈判将更难恢复，地区误判及进一步军事回应的风险上升。报道也指出，袭击使双方和平谈判的前景更加不确定。

**标签**: `#Iran-US tensions`, `#Bahrain`, `#drone attacks`, `#military escalation`, `#peace talks`

---

<a id="item-world-news-2"></a>
### [也门政府军撤出曼德海峡 胡塞武装逼近亚丁](https://www.bbc.co.uk/news/articles/cqvg2xgyvnjpo?at_medium=RSS&amp;at_campaign=rss) ⭐️ 7.0/10

沙特支持的也门部队表示，正把兵力从曼德海峡调往亚丁，以加强这座临时首都的防御。也门军方和政府消息人士周日（2026 年 11 月 15 日）称，胡塞武装已推进至距亚丁不足 60 公里处。此前，受国际承认的也门政府宣布，撤出驻曼德海峡的最后一批部队，回防南部沿海的亚丁。胡塞武装是否已完全控制曼德海峡目前未获独立核实，报道也未说明撤军规模、时间安排或当前战线具体位置。

rss · BBC News - World · 11月16日 03:08

**「背景：也门内战与红海航道」** 也门内战始于 2014 年胡塞武装夺取首都萨那，2015 年沙特领导的联军介入，支持国际承认的也门政府；该政府目前以南部城市亚丁作为临时首都。巴布·曼德海峡位于红海南端、连接亚丁湾，是国际航运的关键通道，沿岸控制权直接关系到经红海往返苏伊士运河的商船安全。维基百科相关条目指出，自 2026 年伊朗战争爆发以来，胡塞武装在陆地和海上均加大了对沙特及其他对手的牵制行动。据《纽约时报》对红海战事的梳理，胡塞武装此前已在红海沿岸扩张并夺取战略岛屿，此次向亚丁方向推进延续了这一态势。

**「影响与风险」** 曼德海峡连接红海与亚丁湾，是红海航运的关键咽喉，若该水道实际易手，商船通行安排与地区海上安全格局可能受到影响；但控制权变更尚未经独立确认，相关后果仍属待观察的风险而非既成事实。已确认的影响是，也门政府军从北部战线抽调兵力回防亚丁，显示其对南部据点防御的优先考量。亚丁若面临进一步军事压力，可能加剧本已严峻的人道处境和平民流离失所风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Yemeni_civil_war_%282014%E2%80%93present%29">Yemeni civil war (2014–present) - Wikipedia</a></li>
<li><a href="https://www.nytimes.com/interactive/2026/10/06/world/middleeast/yemen-houthis-reconstruct.html">How the Houthis Triumphed on the Red Sea and Sparked a New War ...</a></li>

</ul>
</details>

**标签**: `#Yemen`, `#Houthis`, `#Bab al-Mandab`, `#Red Sea security`, `#Yemen civil war`

---

<a id="item-world-news-3"></a>
### [西班牙定于 11 月 29 日举行提前大选，极右翼可能首次进入政府](https://www.theguardian.com/world/2026/nov/16/will-spains-snap-election-in-november-bring-a-far-right-party-into-government) ⭐️ 7.0/10

据英国《卫报》11 月 16 日报道，西班牙定于 11 月 29 日举行提前大选，这是该国 11 年内的第六次大选。报道称，此次选举可能终结已持续八年的社会党领导的政府，并可能出现自佛朗哥去世、西班牙恢复民主以来首个进入政府的极右翼政党。该报道属于选前预览，未点名具体政党、候选人，也未提供民调数据或席次预测；目前尚不清楚各党得票前景和可能的组阁组合。

rss · The Guardian - World · 11月16日 05:00

**「背景」** 西班牙众议院共 350 席，全部在大选中改选；参议院 266 席中有 208 席由选举产生。2026 年 11 月 29 日的投票是西班牙 11 年内的第六次大选，可能结束已持续八年的社会党领导政府，并使一个极右翼政党首次进入政府。选前，据《The Olive Press》报道，人民党（PP）正与 Vox 进行联合政府谈判，讨论目标包括收紧无合法居留外国人的公共医疗；民调预测网站 Polling Forecast 预计 PP 将获约 136 席，区间为 116 至 150 席，并提示提前民调存在误差。

**「影响与不确定性」** 选举结果将直接决定西班牙下一届政府的组成，并影响该国在欧盟内部的政策立场；若极右翼政党进入政府，将是西班牙自 1970 年代民主化以来的首次，其政治象征意义可能波及欧洲其他国家的右翼政党格局。报道所述的极右翼入阁目前只是一种可能，而非既成事实：在缺乏民调、席次预测和组阁谈判信息的情况下，何种联盟能够取得议会多数、极右翼是否以及以何种形式参政，均无法确认。

**「后续观察点」** 最直接的观察点是 11 月 29 日的投票与官方计票结果：各党获得的议席数将决定由谁尝试组阁，以及极右翼政党是否成为执政联盟中不可或缺的一方。第二，投票日之后的组阁谈判同样关键——西班牙的议会制安排下，若无单一政党取得多数，政府能否产生取决于政党间的结盟协议，因此谈判进展和最终达成的联盟构成值得关注。报道未提及具体民调数字，选举结果仍属未知。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/April_2019_Spanish_general_election">April 2019 Spanish general election - Wikipedia</a></li>
<li><a href="https://www.pollingforecast.com/es/election-day">Spain : polling -day outlook | Polling Forecast</a></li>
<li><a href="https://www.theolivepress.es/spain-news/2026/10/24/pp-vox-coalition-election-healthcare/">Spain PP - Vox coalition target healthcare for non-resident foreigners</a></li>

</ul>
</details>

**标签**: `#Spain`, `#snap election`, `#far-right politics`, `#European politics`, `#Spanish politics`

---

<a id="item-world-news-4"></a>
### [爱沙尼亚称挫败针对无人机厂商的破坏行动，将于 12 月 1 日关闭全部对俄口岸](https://www.theguardian.com/world/2026/nov/15/estonia-to-close-all-border-crossings-with-russia-after-attack-on-drone-maker) ⭐️ 7.0/10

爱沙尼亚于 11 月 15 日（周日）宣布，将从 12 月 1 日起关闭本国所有与俄罗斯之间的边境口岸。此前在周末，当局在塔林附近的维姆西（Viimsi）制止了一起针对国防无人机企业 Threod Systems 的袭击，拘留八人，并表示公司安保团队作出反应后未出现人员伤亡或损失。爱沙尼亚当局称，此次行动由俄罗斯军事情报机构——俄联邦武装力量总参谋部情报总局（GRU）下令，总理将事件与爱沙尼亚对乌克兰的支持相联系；这一归责目前来自爱沙尼亚官方，尚未见到独立核实的证据。此外，来源报道对涉事工厂是否起火说法不一，调查细节与八名被拘留者的指控情况仍不清楚。

rss · The Guardian - World · 11月15日 22:17

**「背景」** Threod Systems 是一家爱沙尼亚国防企业，生产远程攻击型与侦察型无人机。爱沙尼亚是北约与欧盟成员国，与俄罗斯接壤，两国间的陆路边境口岸是人员往来的主要通道。塔林方面将此类事件称为俄罗斯发动的“混合战争”，即结合情报、破坏与网络手段的非传统对抗方式。爱沙尼亚所指的 GRU，是俄罗斯军方的对外情报机构。

**「影响」** 已确认的直接影响是：自 12 月 1 日起，爱沙尼亚与俄罗斯之间不再有开放的陆路边境口岸，跨境探亲、务工和公路货运将被迫中断或改道，旅客可能需经拉脱维亚等第三国中转。在安全层面，爱沙尼亚把一起未造成损失的事件升级为全面边境管制，这可能进一步加剧北约东翼与俄罗斯之间的紧张。潜在风险包括俄方采取对等或非对等措施，以及边境两侧居民短期滞留；这些后果目前尚未发生，需以后续事态为准。

**「后续观察」** 一是 12 月 1 日口岸关闭生效前后的实际执行情况，以及是否设置人道或货运例外安排。二是爱沙尼亚检方对八名被拘留者的指控、调查进展，以及是否公布可独立核实的证据。三是俄罗斯官方对该事件的回应，以及北约和欧盟是否就这起疑似破坏行动采取集体措施。

**标签**: `#Estonia`, `#Russia`, `#sabotage`, `#border security`, `#Baltic security`

---

<a id="item-world-news-5"></a>
### [捷克布拉格数十万人示威 反对公共广播经费改革](https://www.theguardian.com/world/2026/nov/15/czechia-protest-prague-media-freedom) ⭐️ 7.0/10

2026 年 11 月 15 日周日，数十万人在布拉格集会，反对政府计划取消用于资助捷克公共广播机构的强制性许可费、改为直接从国家预算拨款。组织者称到场人数超过 35 万，并称此次规模超过 3 月一场 20 多万人的抗议，可能成为 1989 年天鹅绒革命以来捷克最大规模的示威。批评者认为，这项经费改革会威胁公共广播的独立性。目前提供的报道未独立核实组织者给出的到场人数，也未详细说明政府如何回应或该计划接下来将如何推进。

rss · The Guardian - World · 11月15日 18:20

**「背景：捷克公共广播的经费之争」** 捷克公共广播机构——捷克电视台（Czech Television）与捷克广播电台（Czech Radio）——长期依靠家庭和企业缴纳的强制性收视收听费运营。由亿万富翁安德烈·巴比什（Andrej Babiš）领导的政府计划取消这项收费，改由国库直接拨款，批评者认为此举会削弱编辑独立性。欧洲已有类似先例：据 BBC 报道，法国于 2022 年取消收视费，公共媒体改由部分增值税收入资助；挪威于 2020 年废除收费，把公共广播机构经费并入国家预算。今年 3 月布拉格曾举行超过 20 万人参加的相关抗议，组织者称本次参加人数超过那次。

**「影响与风险」** 观察到的直接后果是，这场大规模和平示威使公共广播经费问题成为捷克全国政治议程上的突出议题，并显示相关计划面临强烈的公众动员。潜在风险在于，若政府按计划以国家预算取代许可费，公共广播机构与政府的财政联系将更直接，批评者所担忧的编辑独立性受损风险可能上升；方案是否调整、政府作何回应仍有待观察。

**「后续观察」** 接下来最关键的节点是相关立法进程：抗议针对的是政府取消公共广播许可费、改由国家预算直接拨款的计划，《耶路撒冷邮报》在报道标题中将其称为“巴比什媒体法案”。现有报道尚未说明该法案在议会的具体审议与表决时间表，因此一旦进入正式表决阶段，将成为判断该计划能否落地的实质性节点。其次值得关注的是捷克电视台、捷克广播电台等公共广播机构自身的回应，包括它们是否寻求法律途径，或就新的拨款机制与政府谈判，这将直接影响其编辑独立性。第三是抗议组织方是否宣布新的集会或扩大行动；他们此前预期参加人数可达 40 万至 60 万，而不同媒体援引主办方给出的实际人数分别为 35 万以上（《卫报》）和约 40 万（BBC），后续独立核实的人数统计也可能影响公众对该运动规模的判断。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bbc.com/news/articles/cm8e0knr7604o">Czechs rally against plan to switch funding of public media</a></li>
<li><a href="https://www.youtube.com/watch?v=A0B4p2sLXrc">Czechs protest government plan to overhaul public media funding</a></li>
<li><a href="https://www.bbc.com/news/articles/cm8e0knr7604o">Czechs rally against plan to switch funding of public media</a></li>
<li><a href="https://www.jpost.com/international/article-914970">Babis media bill sparks mass Prague protest over Czech TV and...</a></li>
<li><a href="https://www.theguardian.com/world/2026/nov/15/czechia-protest-prague-media-freedom">Protest in Prague over media freedom expected to be... | The Guardian</a></li>

</ul>
</details>

**标签**: `#Czechia`, `#media freedom`, `#protests`, `#public broadcasting`, `#government policy`

---

<a id="item-world-news-6"></a>
### [国际法院将就缅甸是否对罗兴亚人实施种族灭绝作出裁决](https://www.theguardian.com/world/2026/nov/15/myanmar-rohingya-genocide-icj) ⭐️ 7.0/10

《卫报》11 月 15 日报道，国际法院（ICJ，联合国主要司法机关）将于本周就缅甸是否对罗兴亚少数民族实施种族灭绝作出判决。报道称，这将是该法院历史上首次有机会裁定一国犯下种族灭绝罪，并称这可能成为二战结束以来国际法中最重大的时刻之一。报道指出，该判决还将对南非在国际法院起诉以色列的案件产生参照意义。截至报道发布，判决的具体日期、裁决结果以及法院如何认定事实均未公布，这篇报道属于简短预告，未详述双方的证据与主张。

rss · The Guardian - World · 11月15日 06:00

**「案件背景：冈比亚诉缅甸案」** 这起案件的正式名称为“冈比亚诉缅甸案”（The Gambia v Myanmar），由西非国家冈比亚于 2019 年 11 月 11 日向国际法院提起诉讼，主张缅甸违反了其在《防止及惩治灭绝种族罪公约》下承担的义务。公开资料显示，听证会于 2019 年 12 月 10 日开始，为期三天；作为原告，冈比亚须证明缅甸实施了灭绝种族行为，举证责任相当沉重。总部设在荷兰海牙的国际法院审理的是国家责任问题，而与之并行的还有国际刑事法院（ICC）针对孟加拉国与缅甸情形的调查，后者针对的是个人刑事责任。国际法院历史上从未判定任何国家犯下灭绝种族罪，因此本案判决无论结果如何都将成为重要先例。

**「为何重要」** 国际法院的判决对当事国具有约束力，但法院本身没有执行手段，若缅甸被裁定违反《防止及惩治灭绝种族罪公约》，后续执行仍取决于相关国家的政治意愿，并可能涉及联合国安理会。对罗兴亚人而言，裁决关系到其遭受的暴力是否被最高司法机关正式认定，也影响难民安置与追责讨论。在更广层面，报道认为，判决对《防止及惩治灭绝种族罪公约》的解释与证据标准，将被其他同类诉讼引用，包括南非诉以色列案。

**「后续观察」** 国际法院预计本周作出判决，届时将公布 17 名法官组成的合议庭是否认定缅甸对罗兴亚人犯下灭绝种族罪，以及随之而来的赔偿或命令措施。据《卫报》报道，这将是国际法院首次就一个国家是否犯下灭绝种族罪作出裁定，其裁决理由（尤其是对“特定意图”的认定标准）可能影响南非在国际法院对以色列提出的加沙案；《耶路撒冷邮报》亦指出该判决可能为后者确立先例。另一条平行追责渠道是国际刑事法院针对孟加拉国/缅甸境内罗兴亚人所涉罪行的调查，该调查与国际法院这起 2019 年提起的诉讼并非同一程序，其进展值得同步关注。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Rohingya_genocide_case">Rohingya genocide case - Wikipedia</a></li>
<li><a href="https://ohrh.law.ox.ac.uk/the-gambia-v-myanmar-icj-upholds-the-rights-of-rohingyas/">The Gambia v Myanmar : ICJ upholds the rights of Rohingyas | OHRH</a></li>
<li><a href="https://durhamlawreview.squarespace.com/legal-developments/the-gambia-v-myanmar-contemporary-genocide">The Gambia v Myanmar : contemporary genocide ?</a></li>
<li><a href="https://en.wikipedia.org/wiki/Rohingya_genocide_case">Rohingya genocide case - Wikipedia</a></li>
<li><a href="https://www.jpost.com/international/article-914949">ICJ Myanmar genocide ruling could impact Israel &#x27;s Gaza case</a></li>
<li><a href="https://www.theguardian.com/world/2026/nov/15/myanmar-rohingya-genocide-icj">World’s top court to rule if Myanmar committed genocide against...</a></li>

</ul>
</details>

**标签**: `#Myanmar`, `#Rohingya`, `#ICJ`, `#genocide`, `#international law`

---

<a id="item-world-news-7"></a>
### [泰国普吉岛帕通商铺火灾致至少 11 人死亡](https://www.aljazeera.com/video/newsfeed/2026/11/16/shophouse-fire-kills-at-least-11-in-phuket?traffic_source=rss) ⭐️ 7.0/10

据半岛电视台（Al Jazeera）报道，泰国旅游城市普吉岛帕通（Patong）的多栋商铺建筑被大火吞噬，造成至少 11 人死亡，另有多人受伤。报道于 2026 年 11 月 16 日发布，但未指明起火时间、具体地点或伤亡数字的官方来源。目前尚不清楚火灾原因、起火点，以及是否有泰国当地政府部门确认或更新了死亡人数。伤者的具体人数和伤情也没有独立信息可供核实。

rss · Al Jazeera English · 11月16日 03:51

**「背景：帕通店屋火灾与当地建筑风险」** 帕通（Patong）位于泰国普吉岛西海岸，是当地旅游和夜生活最集中的区域。临街建筑多为“店屋”结构：底层用于经营，上层用于居住，因此火势容易沿狭窄街巷和相连建筑蔓延。据泰国媒体《考索英文报》（Khaosod English）同日报道，帕通一家摩托车租赁店铺发生火灾，38 人因吸入浓烟受伤，五栋四层商住两用楼受损，救援人员当时仍在搜寻据称被困人员。该报道与半岛电视台所述火灾在时间和地点上吻合，但报道重点和伤亡统计不同，总死伤人数仍待官方核实。半岛电视台的报道未说明消息来源，起火原因、遇难者身份以及是否存在建筑消防隐患均未公布。

**「密集商住区的安全隐忧」** 帕通是普吉岛游客最集中的区域之一，临街商铺建筑通常下层经营、上层居住，一旦起火，人员疏散和消防救援难度较大。此次事件已造成重大人员伤亡，可能促使当地检视这类建筑的消防通道、报警设备和用电安全管理。若后续证实存在普遍的消防隐患，影响可能波及当地商户、居民和旅游业的日常运营；但这些后果目前尚属推测，需待官方调查结果。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.khaosodenglish.com/news/2026/11/16/patong-motorcycle-rental-shop-fire-injures-38-damages-five-units/">Patong motorcycle rental shop fire injures 38, damages five units</a></li>

</ul>
</details>

**标签**: `#Thailand`, `#Phuket`, `#Patong`, `#deadly fire`, `#disaster`

---

<a id="item-world-news-8"></a>
### [半岛电视台实时报道：第三艘美国航母抵达中东，伊朗称不会坐等遭袭](https://www.aljazeera.com/news/liveblog/2026/11/16/iran-war-live-tehran-warns-it-may-strike-first-before-another-us-attack?traffic_source=rss) ⭐️ 7.0/10

半岛电视台（Al Jazeera）2026 年 11 月 16 日的实时更新报道称，美国海军“西奥多·罗斯福”号（USS Theodore Roosevelt）航母已抵达中东，成为该地区第三艘美国航母。同一报道称，伊朗警告不会坐等遭受攻击，并暗示可能先行采取行动。该实时条目内容简短，未说明航母的具体位置、抵达时间、随行舰艇编成，也未说明伊朗表态的原文措辞、发出者身份与发布时间；美国军方与伊朗官方均未在该报道中直接被引述确认上述细节，报道亦未提及独立信源核实。因此，第三艘航母属于例行轮换、临时增援还是其他性质，以及伊朗表态是否代表官方既定政策，目前仍不明确。

rss · Al Jazeera English · 11月16日 00:00

**「背景：三艘美军航母同处中东战区」** 据半岛电视台援引一名美国官员的说法，“西奥多·罗斯福”号抵达后，美军中央司令部（CENTCOM，负责中东及中亚地区的美军作战司令部）责任区内将同时有三个航母打击群。《耶路撒冷邮报》报道称，此次增派正值美国总统特朗普前往中国、准备与中国国家主席习近平及俄罗斯总统普京讨论伊朗问题之际。第三个航母打击群到位，意味着美军可在不依赖地区陆基机场的情况下增加可出动的舰载机规模；但这些舰艇的具体任务、部署时长，以及是否配合进一步军事行动，目前均未由美方公开说明。

**「影响与风险」** 就已确认的信息而言，可以确认的只是半岛电视台报道了一艘航母抵达及一段伊朗方面的警告性表态，其余后果尚属推测。若部署属实，三艘美国航母同时位于中东，将显著增加该地区可用的舰载航空力量，并被地区各方解读为紧张升级的信号，从而压缩外交回旋空间。可预见的风险包括：双方在高度戒备状态下因误判或偶发摩擦而升级；地区盟友与航运、能源运输相关方被迫调整安全安排。上述均为潜在风险而非已观察到的事实，实际影响取决于部署规模、持续时间以及伊朗表态后续是否转化为具体军事行动。

**「后续观察点」** 一是美国国防部或美军中央司令部是否公开确认第三艘航母的部署与任务性质，这将决定该消息属于例行轮换还是实质性增援。二是伊朗官方通讯社或高级官员是否以正式声明形式重复“可能先发制人”的表述，从而区分媒体转述与官方政策立场。三是该地区是否出现可独立核实的军事活动变化，而非仅由一方发布的说法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.aljazeera.com/news/liveblog/2026/11/16/iran-war-live-tehran-warns-it-may-strike-first-before-another-us-attack">Iran war live: Third US carrier arrives, Iran warns it could strike first</a></li>
<li><a href="https://www.jpost.com/middle-east/article-915003">US sends third aircraft carrier to Middle East as Donald Trump heads...</a></li>

</ul>
</details>

**标签**: `#Iran`, `#US military`, `#Middle East`, `#military escalation`, `#conflict update`

---

<a id="item-world-news-9"></a>
### [近 2200 名移民两天内抵达西班牙加那利群岛](https://www.france24.com/en/europe/20261115-nearly-2200-migrants-reach-spain-canary-islands-in-two-days) ⭐️ 7.0/10

西班牙海岸警卫队 11 月 15 日表示，过去两天约有 2200 名移民抵达西班牙加那利群岛，延续了近期来自西非国家的抵达潮。加那利群岛当局本周早些时候已宣布进入移民紧急状态。现有信息未说明这些移民的具体国籍、出发地点、健康状况以及当地的收容和安置安排。

rss · France 24 - English · 11月15日 21:06

**「背景：大西洋移民路线与当地紧急状态」** 加那利群岛位于西非海岸以西的大西洋上，是来自西非的移民乘船前往欧洲的主要通道之一；半岛电视台报道称，这条“大西洋路线”是全球最致命的移民航线之一。据半岛电视台 11 月 8 日报道，群岛最西端的耶罗岛（El Hierro）因移民和难民涌入宣布进入紧急状态，报道还提到 11 月前六天内当地海域共救起超过 3200 名移民。美联社援引西班牙海上救援与安全机构（Maritime Rescue and Safety Service）的数据报道了此次两天内约 2200 人乘船抵达的情况，但目前尚无关于这些船只出发地、乘客国籍构成及安置安排的详细官方说明。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://report.az/en/other-countries/around-2-200-migrants-arrive-in-spain-s-canary-islands-in-two-days">Around 2 , 200 migrants arrive in Spain &#x27;s Canary Islands in... | Report.az</a></li>
<li><a href="https://www.aljazeera.com/news/2026/11/8/canary-islands-el-hierro-declares-emergency-amid-migrant-refugee-influx">Canary Islands ’ El Hierro declares emergency amid migrant , refugee...</a></li>

</ul>
</details>

**标签**: `#Canary Islands migration`, `#Spain`, `#West Africa migration`, `#migration emergency`, `#humanitarian response`

---

<a id="item-world-news-10"></a>
### [美国全国航班停飞事件预计恢复 政府称系通信线路更换失误](https://www.france24.com/en/us-probes-nationwide-flights-stoppage-as-travel-disruptions-persist) ⭐️ 7.0/10

美国全国航空交通在周五夜间（11 月 13 日）实施地面停飞后，预计于周日（11 月 15 日）恢复正常；此次停飞导致数十万旅客滞留，并扰乱全球旅行。特朗普政府将事件归因于老旧铜线通信线路更换工程出现失误，并表示没有证据表明这是网络攻击。在议员呼吁展开调查之际，事件的技术原因、调查主体和完整范围尚未得到独立确认。

rss · France 24 - English · 11月15日 14:09

**「背景：一次全国性停飞与老化通信设施」** 停飞（ground stop）是航空管理机构要求航班暂停起飞的指令，此次指令于周五夜间在全国范围生效，导致旅客滞留并波及国际航线。特朗普政府将原因归结为对老旧铜线通信线路的更换出现失误，并表示没有证据显示这是一次网络攻击；但具体是哪套系统、如何失效，以及更换工程由哪个机构负责，目前仍未公开说明。事件因此迅速从一次运行中断转为对美国航空通信等老化基础设施的问责议题，多名议员已要求展开调查。法国 24 台报道中的分析来自 Vector Strategic Consulting 航空专家菲利普·曼（Philip Mann）。

**「影响」** 此次事件已造成数十万旅客滞留和全球航空旅行受阻，并促使议员要求审查美国航空通信基础设施的可靠性。若老化通信线路问题不能得到解决，未来可能再次出现类似运行中断，但这一风险尚未被独立评估。

**「后续观察」** 接下来值得关注的是美国联邦航空管理局（FAA）是否会公布更完整的技术说明和事件报告，交代此次电信故障的影响范围、受影响航班数量及停飞决策过程；CNN 报道称，前空管人员指出这些关键问题仍未得到回答。另一个观察点是国会是否启动正式调查，以及调查范围是否涉及老化的通信基础设施。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnn.com/2026/11/14/us/live-news/us-ground-stop-flights">Key questions about FAA ground stop still unanswered as air... | CNN</a></li>
<li><a href="https://www.aljazeera.com/news/2026/11/15/what-forced-the-us-to-ground-all-planes-a-router-switch-we-now-know">What forced the US to ground all planes? A router switch... | Al Jazeera</a></li>

</ul>
</details>

**标签**: `#US aviation`, `#travel disruption`, `#infrastructure failure`, `#investigation`, `#cybersecurity`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [中国 10 月消费、工业与投资数据全面低于预期](https://www.cnbc.com/2026/11/16/china-retail-sales-october-industrial-output-investment.html) ⭐️ 8.0/10

中国 10 月社会消费品零售总额同比增长 0.4%，低于经济学家预期的 0.8%，增速较 9 月的 1.1%放缓；规模以上工业增加值同比增长 4.8%，也低于 5.3%的预期。今年前 10 个月固定资产投资同比下降 8.1%，而分析师预期为下降 7%。

rss · CNBC Finance · 11月16日 03:53

**「背景」** 房地产低迷已连续第五年侵蚀家庭财富并拖累消费，而此轮投资下滑的幅度为新冠疫情以外时期所未见。

**「影响」** 增长愈发依赖外需：10 月出口同比增长 35.2%，但分析人士警告，全球人工智能资本开支回落或欧盟进一步贸易限制可能冲击这一出口引擎。

**标签**: `#China economy`, `#macroeconomic data`, `#retail sales`, `#fixed-asset investment`, `#trade surplus`

---

<a id="item-finance-news-2"></a>
### [卢特尼克因英伟达相关风波面临质询，其子经营的坎托申报持股减少](https://www.cnbc.com/2026/11/13/howard-lutnick-nvidia-jensen-huang-china-cantor-fitzgerald.html) ⭐️ 8.0/10

CNBC 报道称，美国商务部长霍华德·卢特尼克因英伟达相关“间谍风波”面临质询。据 CNBC 对证券申报文件的分析，其子经营的坎托·菲茨杰拉德在 2025 年 9 月底至 2026 年 3 月底期间将申报持有的英伟达股票数量减少约 49%至 178 万股；报道称，目前没有证据表明这一变动与情报警告有关。

rss · CNBC Finance · 11月15日 19:58

**「背景」** 卢特尼克于 2025 年 2 月离开坎托出任商务部长，该部门负责出口管制；据 Axios 报道，他多次抵制对涉嫌将英伟达先进 AI 芯片转运至中国的新加坡公司 Megaspeed 采取更严措施。英伟达 CEO 黄仁勋在有关其与一名疑似中国间谍关系的风波中于周四辞职。

**标签**: `#Nvidia`, `#US export controls`, `#Commerce Department`, `#conflict of interest`, `#semiconductors`

---

<a id="item-finance-news-3"></a>
### [美法官驳回美光三星等 DRAM 价格操纵案撤诉动议](https://www.tomshardware.com/tech-industry/big-tech/judge-denies-motion-to-dismiss-dram-price-fixing-lawsuit-against-micron-samsung-and-sk-hynix-says-chipmakers-acted-like-hawks-flying-in-formation-finds-evidence-of-dram-collusion-plausible-after-500-percent-price-surge) ⭐️ 7.0/10

A federal judge rejected motions to dismiss a class-action lawsuit alleging Micron, Samsung, and SK Hynix colluded to restrict DRAM supply and drive prices up sharply, allowing the case to advance.

telegram · zaihuapd · 11月15日 16:39

**标签**: `#DRAM`, `#price-fixing lawsuit`, `#antitrust`, `#semiconductors`, `#Micron/Samsung/SK Hynix`

---

<a id="item-finance-news-4"></a>
### [中美俄领导人拟于 11 月 19 日在深圳 APEC 场边举行首次三方会晤](https://apnews.com/article/trump-xi-putin-summit-china-5fe92253ef38100bae913834a9b74d72) ⭐️ 7.0/10

中国外交部发言人宣布，中美俄三国领导人计划于 11 月 19 日在深圳 APEC 峰会期间举行三方会晤，会晤安排在场边、不属于 APEC 正式议程。媒体称这将是三国领导人首次专门举行三方会晤，目前尚无议程或成果细节。

telegram · zaihuapd · 11月16日 01:38

**「背景」** 亚太经合组织（APEC）第 33 次领导人会议定于 2026 年 11 月 18 日至 19 日在深圳举行，这场三方会晤被安排在峰会场边；中方在 11 月 4 日曾表示正与有关方就三国领导人会晤“保持沟通”。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nybusinesstimes.com/hollyland-named-official-sponsor-of-apec-2026-shenzhen-meetings/">Hollyland Named Official Sponsor of APEC 2026 Shenzhen Meetings</a></li>
<li><a href="https://paral.news/a/en/2026-11-05/apec-shenzhen-trump-xi-putin-trilateral-2026.html">China Acknowledges Contacts on a Donald Trump – Xi ...</a></li>

</ul>
</details>

**标签**: `#China-US-Russia relations`, `#APEC`, `#summit diplomacy`, `#geopolitical risk`

---

<a id="item-finance-news-5"></a>
### [猪肉价格跌至近 10 年低位，11 月 9 日生猪均价每公斤 8.63 元](https://finance.sina.com.cn/jjxw/2026-11-15/doc-iniyupuh6583194.shtml) ⭐️ 7.0/10

11 月以来，全国猪肉价格跌至近 10 年低位，上海部分菜场的猪肉售价已经低于蔬菜；11 月 9 日生猪均价降至每公斤 8.63 元，福州生猪收购价为每 50 公斤 480 至 550 元，同比下降 20%至 26%。业内人士把猪价下跌归因于需求减弱和生猪供应增加，分析人士预计，未来 6 至 8 个月猪价反弹仍可能乏力。

telegram · zaihuapd · 11月16日 03:45

**「背景」** 生猪行业常被描述为存在“猪周期”：价格上涨刺激养殖扩产，供应过剩又压低价格，直到产能收缩后价格再度回升。

**「影响」** 据大纪元报道，当前生猪价格仍处于养殖亏损区间，这意味着在猪价接近十年低位期间，生猪养殖户将持续承受亏损压力，并可能加快行业被动去产能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.dayoo.com/finance/202604/09/171077_54945983.htm">news.dayoo.com/finance/202604/09/171077_54945983.htm</a></li>
<li><a href="https://www.jbzyw.com/view/523285">2026 年 10 月31日 养 猪 业重要信息汇总 - 行业关注 - 鸡病专业网</a></li>
<li><a href="https://www.epochtimes.com/gb/26/11/9/n14886157.htm">需求持续不振 大陆 生 猪 价 跌破9元 创十 年 新 低 | 大纪元</a></li>

</ul>
</details>

**标签**: `#猪肉价格`, `#生猪市场`, `#农产品供需`, `#居民消费价格`, `#养殖业`

---