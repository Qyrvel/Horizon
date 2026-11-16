---
layout: default
title: "Horizon Summary: 2026-11-16 (EN)"
date: 2026-11-16
lang: en
---

> From 145 items, 21 important content pieces were selected

---

**Technology News**
1. [uBlock Origin Element-Picker Universal XSS Fixed in 1.75.4](#item-tech-news-1) ⭐️ 8.0/10
2. [Alibaba launches Qwen4-Max with 2.4T-parameter sparse MoE](#item-tech-news-2) ⭐️ 8.0/10
3. [Meta FAIR/NYU: vision-only parameters matter more than encoder pretraining](#item-tech-news-3) ⭐️ 8.0/10
4. [Meituan releases LongCat-2.5 weights, claims no Nvidia training](#item-tech-news-4) ⭐️ 8.0/10
5. [MacBook Pro OLED PWM flicker and the disputed 240 Hz figure](#item-tech-news-5) ⭐️ 7.0/10
6. [Open-source cmt claims 5x faster pageable cudaMemcpy on B300](#item-tech-news-6) ⭐️ 7.0/10

**Global Affairs &amp; World News**
1. [Iran launches second drone attack on US base in Bahrain in three days](#item-world-news-1) ⭐️ 8.0/10
2. [Yemeni forces pull back from Bab al-Mandab to defend Aden as Houthis advance](#item-world-news-2) ⭐️ 7.0/10
3. [Spain to Hold Snap General Election on 29 November](#item-world-news-3) ⭐️ 7.0/10
4. [Estonia to close all border crossings with Russia from 1 December after suspected sabotage attack on drone maker](#item-world-news-4) ⭐️ 7.0/10
5. [Hundreds of thousands rally in Prague against Czech public media funding overhaul](#item-world-news-5) ⭐️ 7.0/10
6. [ICJ due to rule on whether Myanmar committed genocide against Rohingya](#item-world-news-6) ⭐️ 7.0/10
7. [Shophouse fire in Phuket&\#x27;s Patong kills at least 11](#item-world-news-7) ⭐️ 7.0/10
8. [Third US carrier reported in Middle East as Iran warns it may strike first](#item-world-news-8) ⭐️ 7.0/10
9. [Nearly 2,200 Migrants Reach Spain&\#x27;s Canary Islands in Two Days](#item-world-news-9) ⭐️ 7.0/10
10. [US air travel expected to normalize after nationwide ground stop](#item-world-news-10) ⭐️ 7.0/10

**Financial News**
1. [China’s October Retail Sales, Industrial Output and Investment Miss Estimates](#item-finance-news-1) ⭐️ 8.0/10
2. [Lutnick faces questions over Nvidia ties as Cantor’s reported stake falls](#item-finance-news-2) ⭐️ 8.0/10
3. [美法官驳回美光三星等 DRAM 价格操纵案撤诉动议](#item-finance-news-3) ⭐️ 7.0/10
4. [China, U.S. and Russian Leaders Plan First Trilateral Meeting at Shenzhen APEC](#item-finance-news-4) ⭐️ 7.0/10
5. [China&\#x27;s pork prices fall to near 10-year low](#item-finance-news-5) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [uBlock Origin Element-Picker Universal XSS Fixed in 1.75.4](https://iter.ca/post/ubo-uxss/) ⭐️ 8.0/10

A disclosure describes a universal XSS in uBlock Origin&\#x27;s website-driven element picker, accompanied by a proof of concept, and identifies patched releases: uBlock Origin 1.75.4 and uBlock Origin Lite 2026.1110.1816. The vulnerable path involves a website driving the element picker, according to the disclosure summary. Users on earlier builds of either extension should treat those versions as the minimum fixed releases.

hackernews · zaik · Nov 16, 02:04 · [Discussion](https://news.ycombinator.com/item?id=50513160)

**「Background」** uBlock Origin&\#x27;s element picker lets a user click an element on the page to build a blocking filter, and its overlay interface is injected into the page&\#x27;s own DOM so it can interact with page elements. A universal XSS is one that runs in the extension&\#x27;s privileged context and can therefore affect every site the browser visits, rather than being confined to a single origin. The disclosure&\#x27;s discussion centres on that design choice: extension UI rendered into the page DOM is reachable by page scripts.

**「Impact」** Anyone running an affected uBlock Origin or uBlock Origin Lite build needs to update to 1.75.4 or 2026.1110.1816, respectively; the disclosure identifies those as the fixed versions rather than optional upgrades.

**「Community Discussion」** Commenters focused on the design tradeoff of putting extension UI in the page DOM: ByteOfWood argued this can expose information such as a password manager&\#x27;s suggested logins to the site, and akersten asked why the element-picker rule UI could not live in browser chrome instead. Another commenter flagged uBlock Origin 1.75.4 and uBlock Origin Lite 2026.1110.1816 as the fixed versions to check for.

**Tags**: `#browser-security`, `#xss`, `#ublock-origin`, `#browser-extensions`, `#vulnerability-disclosure`

---

<a id="item-tech-news-2"></a>
### [Alibaba launches Qwen4-Max with 2.4T-parameter sparse MoE](https://qwen.ai/blog?id=qwen4-max) ⭐️ 8.0/10

Alibaba has launched Qwen4-Max, a new flagship model built on a sparse mixture-of-experts architecture with 2.4 trillion total parameters, native visual understanding and a one-million-token context window. The company says the model cuts average cost per task from 26.58 yuan to 11.16 yuan—about 58%—and token consumption by nearly 50%, with API prices lowered accordingly. It is available now, while smaller Qwen4 models and public weights are only planned for later.

hackernews · ilreb · Nov 16, 02:14 · [Discussion](https://news.ycombinator.com/item?id=50513215)

**「Background」** Qwen4-Max is the new flagship in Alibaba&\#x27;s Qwen model line, succeeding earlier Qwen releases. Its sparse mixture-of-experts architecture activates only part of its 2.4 trillion total parameters per token, a design intended to keep inference costs below what a dense model of that size would require; the team says smaller Qwen4 models will later be released with open weights.

**「Impact」** Teams budgeting API workloads can expect lower per-task charges under the new pricing, but they cannot self-host Qwen4-Max or rely on the promised smaller open-weight models until those versions actually ship.

**「Community discussion」** Commenters questioned the value case: one cited an Artificial Analysis score of 43 at $3.27 average cost versus 46 at $0.36 for GPT-6.1 Sol \(medium\), while another said Qwen 3.8&\#x27;s low agent-arena score was largely a speed problem at about 30 tokens per second versus nearly 80 for Opus. Others welcomed the efficiency focus but asked whether the open-weight gap with Anthropic and OpenAI is widening.

**Tags**: `#LLM`, `#Qwen`, `#model release`, `#AI benchmarks`, `#open weights`

---

<a id="item-tech-news-3"></a>
### [Meta FAIR/NYU: vision-only parameters matter more than encoder pretraining](https://www.reddit.com/r/MachineLearning/comments/1xx1k2o/meta_fair_nyu_unbundling_multimodal_vision/) ⭐️ 8.0/10

A Meta FAIR and NYU study trained more than 200 multimodal LLMs from scratch on the same data to unbundle three choices usually packaged as a vision encoder: separate pretraining, vision-only parameters, and placement before the LLM. At matched lifetime compute, encoders pretrained with contrastive, self-supervised, or captioning objectives at best tied an encoder trained from scratch with the LLM; 6.5x longer MetaCLIP pretraining raised ImageNet linear-probe accuracy from 80.4% to 84.4% but did not improve VQA. Encoder-free models trailed across 0.6B–6.4B backbones and needed about 3x the compute to catch up, while the authors&\#x27; &quot;in-fusion&quot; alternative—zero-initialized vision-only weights in the LLM&\#x27;s first eight layers—matched an encoder from 1.7B to 6.4B and cut time to first token by about 13%.

reddit · r/MachineLearning · /u/trungh98 · Nov 15, 17:38

**「Background」** Most multimodal LLMs attach a vision encoder to a language model, and that conventional setup combines three distinct choices: pretraining the encoder, dedicating parameters to visual tokens, and placing vision processing before the LLM. Published systems vary these choices while also differing in training data and compute, and they rarely account for encoder pretraining in the budget, so comparing architectures alone cannot show which choice drives VQA performance.

**「Impact」** For multimodal model designers, the practical takeaway is to allocate parameters to vision-specific capacity rather than assume a separately pretrained encoder is necessary; the authors&\#x27; evidence comes from Qwen3-1.7B/4B configurations with 0.4B vision parameters and 16 Cambrian VQA benchmarks at 448 px, so the tradeoff still needs validation on other architectures and data mixes.

**Tags**: `#multimodal LLMs`, `#vision encoders`, `#pretraining`, `#ablation study`, `#model scaling`

---

<a id="item-tech-news-4"></a>
### [Meituan releases LongCat-2.5 weights, claims no Nvidia training](https://the-decoder.com/meituan-releases-a-1-6-trillion-parameter-agent-model-that-never-touched-an-nvidia-gpu/) ⭐️ 8.0/10

Meituan&\#x27;s LongCat team released the weights for LongCat-2.5 about a week after the model&\#x27;s launch, under an MIT license that permits commercial use. The agent-focused model activates about 48 billion parameters per token and accepts text, image, and video input; it is designed for long, multi-step tasks, especially coding. Meituan says the model was trained entirely on Huawei Ascend chips without Nvidia GPUs, a vendor claim not independently verified in the supplied material. On Terminal Bench v2.1 it scored 88.4, just below Claude Opus 5&\#x27;s 89.1.

telegram · zaihuapd · Nov 15, 11:08

**「Background」** Meituan&\#x27;s LongCat team published the weights about a week after formally launching the model, making this the open follow-up to an earlier announcement. LongCat-2.5 is sparse at runtime: it has 1.6 trillion total parameters but activates roughly 48 billion per token, so total model size and per-token compute are different measures.

**「Impact」** Developers can now use and modify the weights commercially under the MIT license; teams evaluating Huawei Ascend for training have a named example, but should treat the no-Nvidia claim as vendor-stated until technical details or independent tests confirm it.

**Tags**: `#open-source LLM`, `#Meituan LongCat`, `#Huawei Ascend`, `#AI agents`, `#model training`

---

<a id="item-tech-news-5"></a>
### [MacBook Pro OLED PWM flicker and the disputed 240 Hz figure](https://macanorak.com/the-macbook-pros-oled-pwm-problem-when-a-better-display-becomes-worse-to-use/) ⭐️ 7.0/10

An analysis published by MacAnorak examines PWM flicker on the MacBook Pro&\#x27;s OLED display and argues the panel can be worse to use for flicker-sensitive people even as OLED improves image quality. The piece discusses measured PWM frequencies, and its reported 240 Hz figure is contested in the comments. One commenter says the cited source does not support 240 Hz and proposes that the two tandem OLED layers run at 480 Hz out of phase, giving an effective 960 Hz across most usable brightness levels.

hackernews · MacAnorak · Nov 15, 13:15 · [Discussion](https://news.ycombinator.com/item?id=50506719)

**「Context: PWM dimming and flicker perception」** PWM dimming lowers a display&\#x27;s apparent brightness by rapidly switching its light output on and off rather than reducing it steadily, so the flicker rate is set by the panel&\#x27;s driver. What viewers notice depends on the flicker fusion threshold — the frequency at which a flickering light appears steady to the average observer — which varies with brightness, the size of the flickering element, and the observer&\#x27;s own state. Because that threshold and individual sensitivity differ widely, a panel that looks stable to one person can still cause discomfort for another.

**「Impact」** For flicker-sensitive buyers, the practical question is whether the MacBook Pro OLED is comfortable for long sessions, not whether it wins on contrast or color; the frequency dispute matters because the discomfort depends on pulse rate and depth, not just the display&\#x27;s other specifications.

**「Community discussion」** Commenters challenge the 240 Hz figure: one says the cited source does not support it and argues that tandem OLED layers pulsing at 480 Hz out of phase could yield an effective 960 Hz. Others welcome the attention to flicker sensitivity and extend the discussion to CRI and motion blur as related sources of eye strain.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Flicker_fusion_threshold">Flicker fusion threshold - Wikipedia</a></li>
<li><a href="https://opticquiz.com/flicker/">Flicker Fusion Test — Critical Flicker Frequency ... — OpticQuiz</a></li>

</ul>
</details>

**Tags**: `#OLED`, `#PWM flicker`, `#display technology`, `#MacBook Pro`, `#hardware`

---

<a id="item-tech-news-6"></a>
### [Open-source cmt claims 5x faster pageable cudaMemcpy on B300](https://www.reddit.com/r/MachineLearning/comments/1xx2n25/making_cudamemcpy_5x_faster_on_a_b300_p/) ⭐️ 7.0/10

A Reddit post introduced cmt, an open-source tool that tunes pageable CUDA memory copies. In the author&\#x27;s B300 benchmark, copying a 1 GB uint8 tensor from CPU to GPU rose from 10.2 GB/s to 51.5 GB/s after running \`cmt tune\`, roughly a 5x increase. The post links a technical blog and GitHub code and shows the benchmark script and command. These are self-reported results from one GPU and one workload, not an independent measurement.

reddit · r/MachineLearning · /u/makneeee · Nov 15, 18:20

**「Pageable vs. pinned CUDA memory」** CUDA distinguishes pageable host memory, which the operating system may move, from pinned \(page-locked\) memory, which stays resident in RAM. NVIDIA&\#x27;s optimization guidance compares transfer rates for pageable and pinned memory even though both use the same cudaMemcpy syntax. Pinned memory is what enables direct memory access between host and GPU, avoiding intermediate buffers that pageable transfers require.

**「Impact」** CUDA developers whose transfers use pageable memory can test \`cmt tune\` with their existing benchmark commands, but the reported gain is specific to a B300 and a 1 GB CPU-to-GPU copy. Teams should validate it on their own hardware and access patterns before relying on it.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/how-optimize-data-transfers-cuda-cc/">How to Optimize Data Transfers in CUDA C/C++ | NVIDIA Technical...</a></li>
<li><a href="https://www.linkedin.com/pulse/supercharging-data-transfers-cuda-power-page-locked-pinned-mohapatra-bejec">Supercharging Data Transfers in CUDA : The Power of Page-Locked...</a></li>

</ul>
</details>

**Tags**: `#CUDA`, `#GPU performance`, `#memory transfer`, `#open source`, `#benchmarking`

---

## Global Affairs &amp; World News

<a id="item-world-news-1"></a>
### [Iran launches second drone attack on US base in Bahrain in three days](https://www.theguardian.com/world/2026/nov/15/iran-launches-drone-attacks-against-us-military-base-in-bahrain) ⭐️ 8.0/10

Iran launched drone attacks targeting a US military base in Bahrain on Sunday, November 15, 2026, the second such strike in three days, according to The Guardian. Bahrain&\#x27;s foreign ministry said air defence systems intercepted and destroyed the drones in the kingdom&\#x27;s airspace and that the Islamic Revolutionary Guard Corps \(IRGC\) had explicitly claimed responsibility for this attack and for a similar one at dawn on Friday, November 13. Blasts were reported over the capital, Manama, and Bahrain issued two alerts about potential threats, its first such warnings since September. No casualties or damage have been confirmed, and it is not yet established whether any US personnel or facilities were affected.

rss · The Guardian - World · Nov 15, 18:03

**「Background」** The strikes end a lull in attacks during a Middle East war now nearly nine months old, during which negotiations to end the conflict have remained deadlocked. According to the report, Iran described the attacks as retaliation for US strikes inside Iran, while Washington maintains a naval blockade and Tehran continues to exert pressure on the Strait of Hormuz. Bahrain said Friday&\#x27;s incident involved two drones that were also intercepted. Jordan, Egypt, Saudi Arabia and Qatar condemned the strikes and expressed solidarity with Bahrain, whose foreign ministry called them a violation of international law and of the principles of good neighbourliness.

**「Why it matters」** The attacks further complicate efforts to revive talks between Tehran and Washington and raise the risk of a wider military escalation involving Gulf states that host or support US forces. Bahrain&\#x27;s decision to issue public threat alerts points to concrete disruption for residents of Manama, and repeated strikes on Gulf territory could affect aviation and shipping in a region already constrained by the US naval blockade and Iran&\#x27;s posture toward the Strait of Hormuz. The swift condemnations from Jordan, Egypt, Saudi Arabia and Qatar indicate regional governments are aligning behind Bahrain, a dynamic that could narrow diplomatic room for mediation. Whether the strikes were ordered centrally by Iran&\#x27;s leadership or carried out by units acting with discretion remains unconfirmed in the available reporting.

**「What to watch」** Three developments could materially change the story: whether Washington issues an official response or takes military action, whether a third strike follows and whether Bahrain&\#x27;s air defences continue to intercept drones, and whether the peace talks are formally suspended or resumed despite the attacks.

**Tags**: `#Iran-US tensions`, `#Bahrain`, `#drone attacks`, `#military escalation`, `#peace talks`

---

<a id="item-world-news-2"></a>
### [Yemeni forces pull back from Bab al-Mandab to defend Aden as Houthis advance](https://www.bbc.co.uk/news/articles/cqvg2xgyvnjpo?at_medium=RSS&amp;at_campaign=rss) ⭐️ 7.0/10

Saudi-backed Yemeni forces said they are moving troops from the Bab al-Mandab Strait to defend Aden, Yemen&\#x27;s interim capital, according to a BBC report published on 16 November 2026. Military and government sources said Houthi forces had advanced to within 60 kilometres of Aden on Sunday, the report said. The internationally recognised government had earlier announced it was pulling back its last forces from the strait. The supplied account did not make clear whether Houthi forces now control the waterway, how many troops were involved, or what the withdrawal means on the ground.

rss · BBC News - World · Nov 16, 03:08

**「Background to the Bab al-Mandab withdrawal」** Yemen has been divided by civil war since 2014, with the Iran-aligned Houthi movement controlling the north and the internationally recognised government operating from the southern port of Aden; a Saudi-led coalition has backed pro-government forces. The Bab al-Mandab Strait links the Red Sea to the Gulf of Aden and is a chokepoint for commercial and military shipping, which is why control of its shores has become a central battlefield objective. Reporting on the wider conflict says the Houthis have expanded their Red Sea campaign during the 2026 Iran war, and a New York Times reconstruction depicted Houthi-controlled areas extending toward Aden after the seizure of a strategic island near the strait.

**「Significance」** If confirmed, the withdrawal would remove the internationally recognised government&\#x27;s last presence at Bab al-Mandab, a chokepoint on a major maritime route, and could alter security conditions for Red Sea shipping. It also brings the Houthis closer to Aden, where the government is based, raising the risk of further fighting near the city. The source did not provide evidence of Houthi control of the strait or assess the effect on commercial traffic.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Yemeni_civil_war_%282014%E2%80%93present%29">Yemeni civil war (2014–present) - Wikipedia</a></li>
<li><a href="https://www.bbc.com/news/articles/cqvg2xgyvnjpo">Yemeni forces&#x27; retreat leaves Houthis in control of key Red Sea ...</a></li>
<li><a href="https://www.nytimes.com/interactive/2026/10/06/world/middleeast/yemen-houthis-reconstruct.html">How the Houthis Triumphed on the Red Sea and Sparked a New War ...</a></li>

</ul>
</details>

**Tags**: `#Yemen`, `#Houthis`, `#Bab al-Mandab`, `#Red Sea security`, `#Yemen civil war`

---

<a id="item-world-news-3"></a>
### [Spain to Hold Snap General Election on 29 November](https://www.theguardian.com/world/2026/nov/16/will-spains-snap-election-in-november-bring-a-far-right-party-into-government) ⭐️ 7.0/10

Spain is scheduled to hold a snap general election on 29 November 2026, its sixth general election in 11 years, according to The Guardian. The paper reports that the vote could end eight years of socialist-led government and, for the first time since the death of General Franco and Spain&\#x27;s return to democracy, result in a far-right party entering the national government. No results exist yet and no coalition arithmetic has been settled; the item is a preview that frames the election in terms of these possibilities rather than reporting confirmed polling outcomes or party positions. It remains unknown which parties would be able to form a majority, whether any far-right party would in fact be invited into a coalition, and what the final seat distribution will be.

rss · The Guardian - World · Nov 16, 05:00

**「Background」** The Guardian describes the 29 November ballot as Spain&\#x27;s sixth general election in 11 years; that rapid succession includes the April 2019 vote, when all 350 seats in the Congress of Deputies were contested. A single party needs 176 of those 350 seats to govern alone, which is why the pre-election polling and post-election coalition arithmetic matter so much. One polling aggregator&\#x27;s projection ahead of the vote put the conservative Partido Popular \(PP\) on about 136 seats, within a range of 116 to 150, well short of an absolute majority. Spanish media have reported that the PP and the far-right Vox were in talks about forming a coalition government, with public healthcare for foreigners without legal residence among the policy areas under discussion. The Guardian&\#x27;s preview does not set out what triggered the snap election or name the parties beyond referring to a far-right contender.

**「Why it matters」** Because the outcome is undecided, the concrete consequences depend entirely on the result and on post-election coalition negotiations. The stated stakes are twofold: the possible end of a socialist-led government that has been in office for eight years, and the possible first inclusion of a far-right party in Spain&\#x27;s government since the country&\#x27;s transition to democracy following Franco&\#x27;s death — a step with no precedent in the post-1975 period. For Spanish voters, the practical effects would show up in the policy priorities of whichever coalition governs; for European partners, a government including a far-right party would change Spain&\#x27;s alignment within the EU on the issues that coalition agreement covers. These are potential rather than observed consequences, since no vote has yet taken place.

**「What to watch」** The first decisive moment is the vote itself on 29 November, when turnout and the seat breakdown will show whether the socialist-led government can retain power and whether the far-right party gains enough seats to be a plausible coalition partner. Because the source does not indicate any pre-election polling or expected seat ranges, the size of each bloc&\#x27;s caucus is the key unknown to track on results night. If no bloc emerges with a workable parliamentary majority, attention shifts to post-election negotiations and the parliamentary investiture vote that determines who becomes prime minister — the stage at which the far-right party&\#x27;s participation in government would be settled or ruled out. The source names neither the far-right party nor the other contenders, so the specific composition of any coalition remains unconfirmed.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/April_2019_Spanish_general_election">April 2019 Spanish general election - Wikipedia</a></li>
<li><a href="https://www.pollingforecast.com/es/election-day">Spain : polling -day outlook | Polling Forecast</a></li>
<li><a href="https://www.theolivepress.es/spain-news/2026/10/24/pp-vox-coalition-election-healthcare/">Spain PP - Vox coalition target healthcare for non-resident foreigners</a></li>

</ul>
</details>

**Tags**: `#Spain`, `#snap election`, `#far-right politics`, `#European politics`, `#Spanish politics`

---

<a id="item-world-news-4"></a>
### [Estonia to close all border crossings with Russia from 1 December after suspected sabotage attack on drone maker](https://www.theguardian.com/world/2026/nov/15/estonia-to-close-all-border-crossings-with-russia-after-attack-on-drone-maker) ⭐️ 7.0/10

Estonia will close all of its border crossing points with Russia from 1 December, the country&\#x27;s foreign minister said on Sunday, after what Estonian authorities describe as a suspected sabotage attack on a defence drone manufacturer over the weekend. On Saturday morning, eight people were detained during an attempted attack on Threod Systems, an Estonian company that makes long-range attack and reconnaissance drones; the company&\#x27;s security team responded and no injuries or damage were reported. Estonian authorities said the operation was ordered by Russia&\#x27;s GRU, its military intelligence service, and Prime Minister Kaja Kallas-linked statements in the report tie the incident to Tallinn&\#x27;s support for Ukraine — an attribution that has not been independently verified. Estonian officials have not publicly detailed the nationalities or identities of the eight detainees, what charges they may face, or how long the border closure will remain in force; one summary line in the source refers to a drone factory being set alight in Viimsi, while the article body states no damage was reported, and the discrepancy has not been clarified.

rss · The Guardian - World · Nov 15, 22:17

**「Background」** Estonia is a NATO and European Union member that shares a direct land border with Russia, and its crossings are used for both passenger travel and freight. Threod Systems is an Estonian defence firm whose long-range drone production is relevant to regional military capabilities, which is why an attack on the site would be treated by Tallinn as a security matter rather than a purely criminal one. The GRU is Russia&\#x27;s military intelligence directorate, which Western governments have previously accused of sabotage and covert operations in Europe. Estonia has accused Russia of waging hybrid warfare, a term used for hostile activity below the threshold of open armed conflict, such as sabotage, cyber operations or disinformation.

**「Why it matters」** Closing every crossing with Russia is one of the most concrete border measures a Baltic state has taken, and it stands to affect people who rely on the frontier for work, family visits, shopping and fuel: with Estonian crossings shut, such travel would have to be routed through neighbouring Latvia&\#x27;s crossings with Russia, adding distance and cost. The measure also raises the risk of tit-for-tat restrictions on movement and further strains already limited EU-Russia and NATO-Russia channels. For the affected company and its workforce, the incident, if confirmed as a deliberate attack, signals that defence manufacturers in front-line states may face physical threats at home rather than only abroad; no injuries or damage were reported in this case.

**「What to watch」** The closure is scheduled to take effect on 1 December, and Estonian officials have not indicated what conditions would prompt a reopening, so any statement on duration or exemptions for residents and freight will be important. Developments in the investigation of the eight people detained on Saturday — including any charges, custody decisions or identifications — would test the GRU attribution. A public response from Moscow to the closure announcement would also indicate whether further restrictions on movement are likely.

**Tags**: `#Estonia`, `#Russia`, `#sabotage`, `#border security`, `#Baltic security`

---

<a id="item-world-news-5"></a>
### [Hundreds of thousands rally in Prague against Czech public media funding overhaul](https://www.theguardian.com/world/2026/nov/15/czechia-protest-prague-media-freedom) ⭐️ 7.0/10

Hundreds of thousands of people rallied in Prague on Sunday, 15 November 2026, against a government plan to abolish the mandatory licence fees that fund Czechia&\#x27;s public broadcasters and instead finance them directly from the state budget. Organisers put turnout at more than 350,000 and said it exceeded a March demonstration of over 200,000 people, which would make it one of the largest protests in the country&\#x27;s history and potentially the largest since the 1989 Velvet Revolution; the crowd estimate has not been independently verified in the supplied reporting. Participants and critics say the funding change would threaten the broadcasters&\#x27; independence from the government, a charge the report does not attribute to any government response. The supplied account does not include the government&\#x27;s reaction, the precise legislative timetable, or any official assessment of the crowd size.

rss · The Guardian - World · Nov 15, 18:20

**「捷克公共媒体经费之争的背景」** 争议核心是捷克公共广播机构——捷克电视台（Česká televize）和捷克广播电台（Český rozhlas）——长期依靠家庭和雇主缴纳的强制性收视收听许可费运营。现政府计划取消这项收费，改由国家预算直接拨款；批评者认为，这将使公共媒体的经费受制于执政者，削弱其编辑独立性。据BBC报道，欧洲已有先例：法国于2022年取消许可费，公共媒体改由增值税收入的一部分提供资金；挪威于2020年取消许可费，将公共广播机构的经费并入国家预算。组织者称，今年3月一场类似抗议吸引逾20万人参加，因此他们判断周日这场示威可能成为1989年“天鹅绒革命”以来捷克规模最大的集会；上述人数均为组织者估算，未经独立核实。

**「Why it matters」** The dispute goes to how Czech public broadcasting is financed: under the current system, licence fees give broadcasters revenue independent of annual state budget decisions, while the proposed model would make their funding subject to government and parliamentary choices. The size of the demonstration, as claimed by organisers, indicates that the funding plan has become a broad public mobilisation around media independence rather than a narrow budget matter. Whether the change proceeds depends on the legislature, and the supplied reporting does not establish its current status; any effect on editorial independence would follow from the final legal design rather than from the announced plan alone.

**「What to watch」** The decisive next step is whether the Czech government advances its plan to abolish the licence fee and shift public broadcaster funding onto the state budget through parliament, and in what form the legislation emerges; the supplied reports describe the proposal as a government plan but give no timetable for a vote. Also worth watching is whether the government issues any formal response to Sunday&\#x27;s rally, which organisers said drew around 400,000 people, according to the BBC, and which critics — including campaign figure Daniel Stach — have linked to broader opposition to the administration. Any move to revise or delay the funding change in the face of the protests would be a material shift in the story.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theguardian.com/world/2026/nov/15/czechia-protest-prague-media-freedom">Protest in Prague over media freedom expected to be... | The Guardian</a></li>
<li><a href="https://www.bbc.com/news/articles/cm8e0knr7604o">Czechs rally against plan to switch funding of public media</a></li>
<li><a href="https://www.youtube.com/watch?v=A0B4p2sLXrc">Czechs protest government plan to overhaul public media funding</a></li>
<li><a href="https://www.bbc.com/news/articles/cm8e0knr7604o">Czechs rally against plan to switch funding of public media</a></li>
<li><a href="https://www.theguardian.com/world/2026/nov/15/czechia-protest-prague-media-freedom">Protest in Prague over media freedom expected to be... | The Guardian</a></li>

</ul>
</details>

**Tags**: `#Czechia`, `#media freedom`, `#protests`, `#public broadcasting`, `#government policy`

---

<a id="item-world-news-6"></a>
### [ICJ due to rule on whether Myanmar committed genocide against Rohingya](https://www.theguardian.com/world/2026/nov/15/myanmar-rohingya-genocide-icj) ⭐️ 7.0/10

The International Court of Justice is due to deliver a judgment this week on whether Myanmar committed genocide against the Rohingya minority, the Guardian reported on 15 November 2026. The case is being closely watched because the ICJ has never before found a state guilty of genocide. The court has not yet issued its decision, and the report did not specify the exact judgment date, the evidence presented, or the expected outcome. According to the Guardian, the ruling could also have implications for the separate genocide case against Israel.

rss · The Guardian - World · Nov 15, 06:00

**「Background」** The case now before the International Court of Justice was filed by The Gambia in November 2019, alleging that Myanmar breached its obligations under the Genocide Convention; hearings were held that December. The Gambia, which brought the claim on behalf of the convention&\#x27;s state parties, must persuade the court that Myanmar committed genocide. The proceedings are separate from the International Criminal Court&\#x27;s investigation into the situation in Bangladesh and Myanmar, which also focuses on the Rohingya.

**「Significance」** The judgment is seen as a benchmark for international law because the ICJ has never found a state responsible for genocide, so its reasoning could influence how later cases assess genocide claims and state responsibility. The Guardian reports that the outcome may also affect the separate genocide case against Israel, extending the ruling’s relevance beyond Myanmar. Concrete legal or political consequences will depend on the court’s actual findings, which have not yet been delivered.

**「What to watch」** The judgment itself is the next milestone: the Guardian reports the ICJ will deliver its ruling this week in the case brought by The Gambia against Myanmar in 2019, and the court has never before found a state responsible for genocide \(tool-2-1, tool-2-3\). Watch how the bench frames any finding — whether it addresses genocidal intent, which specific acts it attributes to Myanmar&\#x27;s military, and whether it orders any further obligations or remedies beyond the provisional measures the court indicated earlier in the proceedings. Also watch the reaction from Myanmar&\#x27;s government and from Rohingya representatives, since the ruling&\#x27;s practical effect depends on whether the parties accept it and on any follow-up at the UN. Finally, observers will be tracking how the reasoning is received in South Africa&\#x27;s separate genocide case against Israel, which commentators expect to be read in light of this judgment \(tool-2-2, tool-2-3\); the International Criminal Court&\#x27;s parallel investigation into crimes against the Rohingya is a distinct track \(tool-2-1\).

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Rohingya_genocide_case">Rohingya genocide case - Wikipedia</a></li>
<li><a href="https://ohrh.law.ox.ac.uk/the-gambia-v-myanmar-icj-upholds-the-rights-of-rohingyas/">The Gambia v Myanmar : ICJ upholds the rights of Rohingyas | OHRH</a></li>
<li><a href="https://durhamlawreview.squarespace.com/legal-developments/the-gambia-v-myanmar-contemporary-genocide">The Gambia v Myanmar : contemporary genocide ?</a></li>
<li><a href="https://en.wikipedia.org/wiki/Rohingya_genocide_case">Rohingya genocide case - Wikipedia</a></li>
<li><a href="https://www.jpost.com/international/article-914949">ICJ Myanmar genocide ruling could impact Israel &#x27;s Gaza case</a></li>
<li><a href="https://www.theguardian.com/world/2026/nov/15/myanmar-rohingya-genocide-icj">World’s top court to rule if Myanmar committed genocide against...</a></li>

</ul>
</details>

**Tags**: `#Myanmar`, `#Rohingya`, `#ICJ`, `#genocide`, `#international law`

---

<a id="item-world-news-7"></a>
### [Shophouse fire in Phuket&\#x27;s Patong kills at least 11](https://www.aljazeera.com/video/newsfeed/2026/11/16/shophouse-fire-kills-at-least-11-in-phuket?traffic_source=rss) ⭐️ 7.0/10

A fire engulfed shophouse buildings in Patong, a popular tourist town on Thailand&\#x27;s Phuket island, on 16 November 2026, killing at least 11 people and injuring many others, according to Al Jazeera. Shophouses are multi-storey buildings that typically combine ground-floor businesses with residential units above. The report did not name the police, fire service or other officials confirming the death toll, and the cause of the blaze has not been established. The number of injured, the condition of those hurt, the extent of structural damage and whether anyone remains unaccounted for were not specified.

rss · Al Jazeera English · Nov 16, 03:51

**「Patong&\#x27;s dense shophouse district」** Patong is a beach resort town on the Thai island of Phuket and one of the country&\#x27;s busiest tourist areas, where commercial premises are commonly narrow multi-storey shophouses that combine street-level businesses with upper-floor rooms. Also on 16 November 2026, the Thai outlet Khaosod English reported that a fire in Patong swept through a motorcycle rental business, injuring 38 people through smoke inhalation and damaging five four-storey commercial units while rescue workers searched for people reportedly trapped inside. That report gave no death toll, and it could not be immediately established from the available reporting whether it describes the same blaze that Al Jazeera says killed at least 11 people.

**「Why it matters」** Patong is Phuket&\#x27;s main tourism and nightlife district, and a fatal fire in densely packed shophouses directs attention to fire safety, alarms and evacuation routes in buildings that mix commercial and residential use. The confirmed consequence so far is the loss of life and injuries reported by Al Jazeera; displacement of residents, closure of surrounding streets or other disruption to the area have not been reported. Any broader effect on tourism or on enforcement of building-safety rules would depend on the findings of an official investigation, which has not yet been described.

<details><summary>References</summary>
<ul>
<li><a href="https://www.khaosodenglish.com/news/2026/11/16/patong-motorcycle-rental-shop-fire-injures-38-damages-five-units/">Patong motorcycle rental shop fire injures 38, damages five units</a></li>

</ul>
</details>

**Tags**: `#Thailand`, `#Phuket`, `#Patong`, `#deadly fire`, `#disaster`

---

<a id="item-world-news-8"></a>
### [Third US carrier reported in Middle East as Iran warns it may strike first](https://www.aljazeera.com/news/liveblog/2026/11/16/iran-war-live-tehran-warns-it-may-strike-first-before-another-us-attack?traffic_source=rss) ⭐️ 7.0/10

Al Jazeera reported on 16 November 2026 that the USS Theodore Roosevelt has arrived in the Middle East as a third US aircraft carrier in the region, and that Iran warned it would not simply wait for an attack. In the live update, the broadcaster framed the Iranian statement as a suggestion that Tehran could strike first rather than absorb another US attack. The report did not name the Iranian officials or military bodies behind the warning, specify where the Roosevelt is operating, or identify the other two carriers it says are deployed. No direct statement from the US Department of Defense or from named Iranian authorities was quoted, and the carrier&\#x27;s arrival was not independently corroborated in the item. It therefore remains unknown whether the warning reflects an approved change in Iranian military posture or is a declarative message aimed at deterrence.

rss · Al Jazeera English · Nov 16, 00:00

**「Background」** A US official told Al Jazeera that the USS Theodore Roosevelt has arrived in the Middle East and is joining two other US aircraft carriers already operating in the US Central Command area of responsibility. The Jerusalem Post reported that the arrival brings three US carrier strike groups into CENTCOM’s area as Trump travels to China for talks with Xi Jinping and Vladimir Putin, with Iran expected to be on the agenda. Neither account specified the names of the other two carriers or the precise timing of the Roosevelt’s deployment.

**「Significance」** If confirmed, concentrating three US carriers in the Middle East would substantially increase the number of available combat aircraft and the pace of sustained operations the US military could mount, while also enlarging the number of high-value targets and personnel at risk in any exchange. The reported Iranian warning matters because a declared willingness to strike pre-emptively shortens the window for de-escalation and raises the chance that exercises, reconnaissance flights or naval encounters are misread as the opening of hostilities. Gulf states hosting US forces and commercial shipping through the Strait of Hormuz would be most directly exposed to any disruption, though no interruption to shipping or aviation has been reported in this update. These are potential consequences rather than observed ones; the item contains no evidence of active fighting, and the strike-capability and shipping effects described here are analytical inferences, not confirmed developments.

**「What to watch」** Watch for formal confirmation or silence from US Central Command and the Department of Defense on the Roosevelt&\#x27;s arrival and operating area, since official acknowledgement would move the deployment from reported to confirmed. A named statement from Iran&\#x27;s armed forces general staff or the Islamic Revolutionary Guard Corps would clarify whether the warning is a standing instruction to field units or a declarative message intended for foreign audiences, a distinction that materially changes the risk of accidental escalation. Any change in civil aviation notices or maritime security advisories for the Persian Gulf and Strait of Hormuz would indicate that regional authorities are adjusting their own risk assessments.

<details><summary>References</summary>
<ul>
<li><a href="https://www.aljazeera.com/news/liveblog/2026/11/16/iran-war-live-tehran-warns-it-may-strike-first-before-another-us-attack">Iran war live: Third US carrier arrives, Iran warns it could strike first</a></li>
<li><a href="https://www.jpost.com/middle-east/article-915003">US sends third aircraft carrier to Middle East as Donald Trump heads...</a></li>

</ul>
</details>

**Tags**: `#Iran`, `#US military`, `#Middle East`, `#military escalation`, `#conflict update`

---

<a id="item-world-news-9"></a>
### [Nearly 2,200 Migrants Reach Spain&\#x27;s Canary Islands in Two Days](https://www.france24.com/en/europe/20261115-nearly-2200-migrants-reach-spain-canary-islands-in-two-days) ⭐️ 7.0/10

Spain&\#x27;s coastguard said on Sunday, November 15, 2026, that nearly 2,200 migrants had reached the Canary Islands over the previous two days, according to France 24. The arrivals continue a recent surge from West African countries to the Spanish archipelago. Authorities declared a migration emergency earlier in the week. The coastguard figure is the account available so far, and details such as the migrants&\#x27; nationalities, conditions, and a day-by-day or island-by-island breakdown were not provided.

rss · France 24 - English · Nov 15, 21:06

**「Background」** Arrivals on this scale follow weeks of heavy traffic on the Atlantic route from West Africa to the Canary Islands, a crossing Al Jazeera describes as one of the world&\#x27;s deadliest migration routes. Spain&\#x27;s Maritime Rescue and Safety Service \(Salvamento Marítimo\) is the agency whose boat figures underpin the count; the Associated Press, citing the service, reported the same total of about 2,200 people over two days. On 8 November, Al Jazeera reported that authorities on El Hierro, the archipelago&\#x27;s westernmost island, had declared an emergency amid the influx, and that more than 3,200 migrants had been rescued across the Canary Islands in the first six days of November.

**「Significance」** The migration emergency declaration signals that authorities are treating the arrivals as a strain on reception and administrative capacity, though the source did not specify what measures the declaration entails. Because the report gives no breakdown of nationalities, conditions, or destinations, the immediate humanitarian needs of the new arrivals remain unclear.

<details><summary>References</summary>
<ul>
<li><a href="https://report.az/en/other-countries/around-2-200-migrants-arrive-in-spain-s-canary-islands-in-two-days">Around 2 , 200 migrants arrive in Spain &#x27;s Canary Islands in... | Report.az</a></li>
<li><a href="https://www.aljazeera.com/news/2026/11/8/canary-islands-el-hierro-declares-emergency-amid-migrant-refugee-influx">Canary Islands ’ El Hierro declares emergency amid migrant , refugee...</a></li>

</ul>
</details>

**Tags**: `#Canary Islands migration`, `#Spain`, `#West Africa migration`, `#migration emergency`, `#humanitarian response`

---

<a id="item-world-news-10"></a>
### [US air travel expected to normalize after nationwide ground stop](https://www.france24.com/en/us-probes-nationwide-flights-stoppage-as-travel-disruptions-persist) ⭐️ 7.0/10

US air travel was expected to return to normal on Sunday after a nationwide ground stop Friday night stranded hundreds of thousands of passengers and disrupted travel worldwide, France 24 reported. The Trump administration blamed the incident on a botched replacement of old copper communication lines and said there was no evidence it was a cyberattack. Lawmakers are calling for an investigation, and the episode has raised questions about aging US infrastructure. It was not immediately clear which agency ordered the ground stop, the exact technical failure involved, or the full number of flights affected.

rss · France 24 - English · Nov 15, 14:09

**「Background: what is known about the cause」** The ground stop took effect late Friday, at a time when the government was carrying out a replacement of aging copper communication lines; the administration said the replacement work went wrong and that it had found no evidence of a cyberattack. Because the halt covered the national network rather than a single airport, disruption spread into international itineraries, leaving passengers stranded outside the United States as well as inside it. Published information does not yet establish which specific systems failed, how the stop order was issued, or whether outside contractors were involved; those details remain attributed to the government. Lawmakers have called for an investigation and aviation analyst Philip Mann of Vector Strategic Consulting has commented on the incident, but no investigating body, scope or timetable has been announced.

**「Significance」** Beyond the immediate disruption to passengers and international travel, the ground stop has focused attention on the resilience of the communications systems that aviation depends on. Lawmakers&\#x27; calls for an investigation create a formal avenue for establishing accountability and for assessing whether maintenance and replacement work on aging infrastructure needs stronger safeguards; those consequences remain prospective until an inquiry reports.

**「What to watch」** The next concrete signal is whether US lawmakers and aviation committees formally open an investigation into the ground stop, and what scope and subpoena power they claim; the source account says calls for an investigation have already been made but no inquiry has been confirmed. A second milestone is the Federal Aviation Administration&\#x27;s own account of the router and telecommunications switch failure it has blamed, which would clarify how many flights and passengers were affected. Third, track the restoration of schedules: the FAA lifted the ground stop roughly four hours after imposing it on Friday, and carriers are still working through more than 11,000 delayed or canceled flights counted by the tracker FlightAware, so full operational recovery is not yet confirmed.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnn.com/2026/11/14/us/live-news/us-ground-stop-flights">Key questions about FAA ground stop still unanswered as air... | CNN</a></li>
<li><a href="https://www.aljazeera.com/news/2026/11/15/what-forced-the-us-to-ground-all-planes-a-router-switch-we-now-know">What forced the US to ground all planes? A router switch... | Al Jazeera</a></li>
<li><a href="https://www.theguardian.com/world/2026/nov/13/faa-nationwide-ground-stop-flights">Flights slowly resume after US aviation agency lifts nationwide ...</a></li>

</ul>
</details>

**Tags**: `#US aviation`, `#travel disruption`, `#infrastructure failure`, `#investigation`, `#cybersecurity`

---

## Financial News

<a id="item-finance-news-1"></a>
### [China’s October Retail Sales, Industrial Output and Investment Miss Estimates](https://www.cnbc.com/2026/11/16/china-retail-sales-october-industrial-output-investment.html) ⭐️ 8.0/10

China’s October retail sales rose 0.4% from a year earlier, missing a forecast 0.8% rise, while industrial output grew 4.8% versus 5.3% expected. Fixed-asset investment fell 8.1% in the first ten months of the year, worse than analysts’ 7% decline estimate.

rss · CNBC Finance · Nov 16, 03:53

**「Background」** The misses extend a fifth year of property-market weakness that has eroded household wealth, while strong exports and AI-related demand have increasingly carried growth.

**「Impact」** Analysts warn that Chinese exporters, including AI-related equipment suppliers, could be directly exposed if AI capital spending cools or the EU adds trade measures, because external demand has been the main support for growth.

**Tags**: `#China economy`, `#macroeconomic data`, `#retail sales`, `#fixed-asset investment`, `#trade surplus`

---

<a id="item-finance-news-2"></a>
### [Lutnick faces questions over Nvidia ties as Cantor’s reported stake falls](https://www.cnbc.com/2026/11/13/howard-lutnick-nvidia-jensen-huang-china-cantor-fitzgerald.html) ⭐️ 8.0/10

CNBC reported that Cantor Fitzgerald, the firm led by Commerce Secretary Howard Lutnick’s sons, reported holding 1.78 million Nvidia shares at the end of March 2026, down 49% from more than 3.5 million in September 2025, with reported value falling from $652 million to $310 million. The report comes as Lutnick faces questions over U.S. chip-export enforcement and after Nvidia CEO Jensen Huang resigned Thursday amid reports about his ties to a suspected Chinese spy; CNBC said there is no evidence that the share changes were tied to intelligence warnings or that Cantor’s business interests influenced policy.

rss · CNBC Finance · Nov 15, 19:58

**「Background」** Cantor was run by Howard Lutnick until he became commerce secretary in February 2025, and Commerce oversees U.S. export restrictions, including the entity list, which identifies restricted businesses.

**Tags**: `#Nvidia`, `#US export controls`, `#Commerce Department`, `#conflict of interest`, `#semiconductors`

---

<a id="item-finance-news-3"></a>
### [美法官驳回美光三星等 DRAM 价格操纵案撤诉动议](https://www.tomshardware.com/tech-industry/big-tech/judge-denies-motion-to-dismiss-dram-price-fixing-lawsuit-against-micron-samsung-and-sk-hynix-says-chipmakers-acted-like-hawks-flying-in-formation-finds-evidence-of-dram-collusion-plausible-after-500-percent-price-surge) ⭐️ 7.0/10

A federal judge rejected motions to dismiss a class-action lawsuit alleging Micron, Samsung, and SK Hynix colluded to restrict DRAM supply and drive prices up sharply, allowing the case to advance.

telegram · zaihuapd · Nov 15, 16:39

**Tags**: `#DRAM`, `#price-fixing lawsuit`, `#antitrust`, `#semiconductors`, `#Micron/Samsung/SK Hynix`

---

<a id="item-finance-news-4"></a>
### [China, U.S. and Russian Leaders Plan First Trilateral Meeting at Shenzhen APEC](https://apnews.com/article/trump-xi-putin-summit-china-5fe92253ef38100bae913834a9b74d72) ⭐️ 7.0/10

China’s Foreign Ministry said the Chinese, U.S. and Russian leaders plan to hold their first-ever trilateral meeting on Nov. 19 on the sidelines of the APEC summit in Shenzhen, according to a Telegram post citing AP and the ministry.

telegram · zaihuapd · Nov 16, 01:38

**「Background」** Beijing first acknowledged on Nov. 4 that it was maintaining communication about a possible Chinese–Russian–U.S. presidential meeting around the Shenzhen summit, which hosts APEC&\#x27;s 33rd Economic Leaders&\#x27; Meeting on Nov. 18–19.

<details><summary>References</summary>
<ul>
<li><a href="https://www.nybusinesstimes.com/hollyland-named-official-sponsor-of-apec-2026-shenzhen-meetings/">Hollyland Named Official Sponsor of APEC 2026 Shenzhen Meetings</a></li>
<li><a href="https://paral.news/a/en/2026-11-05/apec-shenzhen-trump-xi-putin-trilateral-2026.html">China Acknowledges Contacts on a Donald Trump – Xi ...</a></li>

</ul>
</details>

**Tags**: `#China-US-Russia relations`, `#APEC`, `#summit diplomacy`, `#geopolitical risk`

---

<a id="item-finance-news-5"></a>
### [China&\#x27;s pork prices fall to near 10-year low](https://finance.sina.com.cn/jjxw/2026-11-15/doc-iniyupuh6583194.shtml) ⭐️ 7.0/10

China&\#x27;s national pork prices fell to a near-10-year low in early November, with the average live hog price reaching 8.63 yuan per kilogram on November 9, while purchase prices in Fuzhou dropped 20% to 26% year-on-year to 480-550 yuan per 50 kilograms. Industry figures attribute the decline to weaker demand and larger hog supply, and analysts cited in the report expect any rebound to remain weak over the next six to eight months.

telegram · zaihuapd · Nov 16, 03:45

**「Background」** The hog market is prone to a &quot;pig cycle&quot;: high prices encourage farmers to expand, oversupply drives prices down, and a rebound usually waits for capacity to shrink. Before this fall, industry tracking already showed ample hog and pork supply and high frozen stocks, with demand too weak to absorb it.

**「影响」** Pig farmers are directly affected: Fuzhou purchase prices are down 20–26% year on year, and industry monitoring says prices remain at loss-making levels for farms, while households benefit from cheaper pork.

<details><summary>References</summary>
<ul>
<li><a href="https://news.dayoo.com/finance/202604/09/171077_54945983.htm">news.dayoo.com/finance/202604/09/171077_54945983.htm</a></li>
<li><a href="https://www.jbzyw.com/view/523285">2026 年10月31日养 猪 业 重 要信息汇总 - 行业关注 - 鸡病专业网</a></li>
<li><a href="https://www.epochtimes.com/gb/26/11/9/n14886157.htm">需求持续不振 大陆 生 猪 价 跌破9元 创十 年 新 低 | 大紀元</a></li>

</ul>
</details>

**Tags**: `#猪肉价格`, `#生猪市场`, `#农产品供需`, `#居民消费价格`, `#养殖业`

---