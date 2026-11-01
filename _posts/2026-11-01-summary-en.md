---
layout: default
title: "Horizon Summary: 2026-11-01 (EN)"
date: 2026-11-01
lang: en
---

> From 27 items, 6 important content pieces were selected

---

**Technology News**
1. [Linux IPv4/TCP use-after-free CVE-2026-98432 rated CVSS 9.8](#item-tech-news-1) ⭐️ 8.0/10
2. [Jepsen finds lost committed writes in ParticleDB 1.1.4](#item-tech-news-2) ⭐️ 8.0/10
3. [ChatGPT HTML Preview Exploit Enabled Account Takeover](#item-tech-news-3) ⭐️ 8.0/10
4. [Essay Argues Memory Latency, Not CPU Load, Is the Bottleneck](#item-tech-news-4) ⭐️ 7.0/10
5. [CXMT says sixth-gen 4F² DRAM samples pass validation](#item-tech-news-5) ⭐️ 7.0/10

**Technology Blog**
1. [Fast and Slow Ways to Improve Your Reputation](#item-tech-blog-1) ⭐️ 6.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Linux IPv4/TCP use-after-free CVE-2026-98432 rated CVSS 9.8](https://atlasum.net/blog/cve-2026-98432-linux-ipv4-tcp-uaf) ⭐️ 8.0/10

A Linux IPv4/TCP use-after-free tracked as CVE-2026-98432 is rated CVSS 9.8, putting IPv4/TCP packet handling on affected Linux systems in scope. The available discussion describes exploitation as constrained but serious: commenters say MPTCP is not required, internet exploitation is unlikely where ISP routers drop packets with IP options, and successful exploitation requires multiple CPU cores. Commenters also reported that Ubuntu and Red Hat had no patches at the time of the thread, with Red Hat reportedly calling local IP-option filtering helpful but not a complete mitigation.

hackernews · oger · Oct 31, 19:16 · [Discussion](https://news.ycombinator.com/item?id=50319143)

**「Background」** A use-after-free means code continues to reference memory after it has been freed; this flaw is in Linux&\#x27;s IPv4 TCP path and is reported to involve \`tcp\_v4\_syn\_recv\_sock\(\)\` during the TCP handshake. Remediation is a kernel update, so installing the package is not enough: the host must reboot into the new image, and administrators need to verify the package against their exact distribution release and kernel flavor.

**「Impact」** Administrators running affected Linux distributions should watch for vendor kernel updates; commenters said Ubuntu and Red Hat lacked patches at the time, and that filtering IP-option packets locally helps but is not a full mitigation. Commenters also said systems with one core or packet processing pinned to one core are not affected.

**「Community discussion」** Commenters objected to the HN title edit that removed &quot;Linux,&quot; arguing readers on BSD, macOS, and Windows would incorrectly think they were affected. The thread also added exploitability constraints—MPTCP is not required, IP-option filtering and single-core processing limit exposure—and criticized Ubuntu and Red Hat for lacking patches at the time.

<details><summary>References</summary>
<ul>
<li><a href="https://nolimitcloud.eu/blogs/security/cve-2026-98432-linux-ipv4-uaf">CVE - 2026 - 98432 : Linux IPv 4 TCP Use - After - Free ... | NolimitCloud</a></li>
<li><a href="https://www.penligent.ai/hackinglabs/cve-2026-98432/">CVE - 2026 - 98432 Linux TCP Flaw, Ubuntu Patch and Mitigation Status</a></li>
<li><a href="https://www.youtube.com/watch?v=lVd-40B-DZI">CVE - 2026 - 98432 : Linux Kernel TCP Remote Root Explained - YouTube</a></li>

</ul>
</details>

**Tags**: `#Linux kernel security`, `#TCP/IP`, `#use-after-free`, `#CVE-2026-98432`, `#vulnerability management`

---

<a id="item-tech-news-2"></a>
### [Jepsen finds lost committed writes in ParticleDB 1.1.4](https://jepsen.io/analyses/particledb-1.1.4) ⭐️ 8.0/10

Jepsen published an analysis of ParticleDB 1.1.4 finding frequent transactional anomalies in essentially every workload it measured, including loss of committed writes, internal consistency violations, G1a \(aborted read\), G1b \(intermediate read\) and P4 \(lost update\), with successfully appended values routinely disappearing from later reads of the same key. The report lists 96 issues ranging from crashes, deadlocks and data loss to partially invisible rows that could not be deleted, \`WHERE 4 = 5\` returning rows, dropped tables re-emerging in distorted forms, confused columns and strings turning into integers. Given the severity and the process that produced the errors, Jepsen recommends that users halt further deployment of ParticleDB and migrate to other databases as soon as possible, checking or rebuilding database state from more reliable sources where available. ParticleDB 1.1.4 had claimed Postgres compatibility and a TLA+ &quot;formal proof,&quot; but Jepsen says no TLA+ specification was available during its collaboration, leaving unclear which properties were proven or whether they described the shipped database.

hackernews · aphyr · Oct 31, 13:39 · [Discussion](https://news.ycombinator.com/item?id=50316100)

**「Background」** ParticleDB billed itself as PostgreSQL-compatible and, in its marketing, as “formally proven” with a TLA+ proof; the Jepsen report says no TLA+ specification was available during the collaboration. Jepsen’s review covered ParticleDB 1.1.4 in a single-node configuration and tested whether its documented isolation levels, WAL fsync durability, and transaction modes matched actual behavior.

**「Impact」** Operators running ParticleDB 1.1.4 face a halt-and-migrate decision rather than a patch: Jepsen&\#x27;s recommendation is to stop further deployment and rebuild state from more reliable sources where possible. Teams that selected the database on its advertised Postgres compatibility or TLA+ proof should treat both claims as unverified for this version.

**「Community Discussion」** Commenters treated the findings as a cautionary example of building a database without rigorous design, with one drawing a distinction between software that is correct by construction and software that works only through workarounds around incorrect design — an opinion, not a result of the report. Several commenters singled out the missing TLA+ specification and the 96-issue list as the most damning details.

<details><summary>References</summary>
<ul>
<li><a href="https://proomt.com/item/jepsen-particledb-1-1-4-5e34acb4-6779-46d6-b3b4-2c9cea42d99b">Jepsen: ParticleDB 1.1.4 · proomt</a></li>

</ul>
</details>

**Tags**: `#databases`, `#distributed systems`, `#transaction consistency`, `#Jepsen`, `#software reliability`

---

<a id="item-tech-news-3"></a>
### [ChatGPT HTML Preview Exploit Enabled Account Takeover](https://simonwillison.net/2026/Oct/31/how-we-took-over-chatgpt-accounts/) ⭐️ 8.0/10

Parameter Labs described a now-patched exploit chain that could take over signed-in ChatGPT accounts through the platform&\#x27;s sandboxed HTML previews, formerly called Canvas. The chain abused MathLive&\#x27;s virtual keyboard in the parent page: a sandboxed iframe could send a postMessage that reached an innerHTML sink, inject an unsandboxed iframe, bypass OpenAI&\#x27;s CSP through the YouTube oEmbed endpoint, execute JavaScript, and exfiltrate private data via an image reference. A crafted share URL could then run against another signed-in user and act on their behalf. OpenAI closed the vulnerability and paid a $5,000 bug bounty, according to the report.

rss · Simon Willison · Oct 31, 23:15

**「Background」** ChatGPT&\#x27;s HTML previews—the artifacts feature OpenAI previously called Canvas—render interactive custom HTML in a sandboxed iframe so untrusted code cannot reach OpenAI APIs or private account data. The exploit also depended on a separate feature: ChatGPT&\#x27;s graph support loads MathLive, whose virtual keyboard listens for postMessage commands and can update its layout with HTML. Parameter Labs reported that this receiver was installed by the graph feature while the HTML preview supplied an untrusted sender, connecting the two.

**「Impact」** The exploit shows that a parent-page postMessage handler is part of the HTML preview sandbox boundary: the handler accepted messages from any sandboxed frame and passed their content to innerHTML, so isolating the child iframe was not sufficient. OpenAI has closed the hole, and the report describes no user mitigation.

<details><summary>References</summary>
<ul>
<li><a href="https://www.parameter.ai/labs/we-found-a-gap-at-openai">Do the Math: How We Took Over ChatGPT Accounts - Parameter</a></li>
<li><a href="https://simonwillison.net/2026/Oct/31/how-we-took-over-chatgpt-accounts/">How We Took Over ChatGPT Accounts - simonwillison.net</a></li>

</ul>
</details>

**Tags**: `#ChatGPT security`, `#sandbox escape`, `#web security`, `#postMessage`, `#AI platform security`

---

<a id="item-tech-news-4"></a>
### [Essay Argues Memory Latency, Not CPU Load, Is the Bottleneck](https://pivotlake.io/blog/its-the-memory-latency-stupid/) ⭐️ 7.0/10

A blog post on pivotlake.io, published October 31, 2026, argues that memory latency rather than raw CPU utilization is often the decisive performance bottleneck, and that cache-aware, allocation-conscious coding is the practical response. The post&\#x27;s argument is supported by discussion of how memory access patterns and cache behavior dominate on modern hardware. The supplied excerpt contains no benchmarks, version numbers, or measured results from the author, so the piece reads as an engineering argument rather than a reported experiment. Practitioner accounts in the Hacker News thread are separate from the post&\#x27;s own claims.

hackernews · ntur1337 · Oct 31, 18:38 · [Discussion](https://news.ycombinator.com/item?id=50318720)

**「Background」** Processors execute arithmetic in a handful of cycles, but a fetch from main memory costs orders of magnitude more, so CPUs rely on multi-level caches to hide that gap. When working sets exceed cache capacity or access patterns defeat prefetching, the core stalls waiting on memory and reported CPU utilization can misrepresent where the time actually goes. That makes data layout and allocation strategy — not just instruction count — a primary lever for performance-sensitive software.

**「Impact」** For developers tuning latency-sensitive or cache-constrained systems, the practical takeaway is to profile cache misses and memory-level parallelism before concluding a service is CPU-bound and needs more cores, since access-pattern changes can move throughput without any hardware change. On cache-poor, in-order embedded cores this trade-off is sharper, where the choice between abstraction-heavy containers and inline-allocating structures can determine whether a design fits at all.

**「Community Discussion」** Commenter swiftcoder reported a team convinced its service was maxed out at 100% CPU; cleaning up memory access patterns tripled requests per second without adding hardware. boricj contrasted a neighbouring team&\#x27;s deeply nested virtual methods and off-the-shelf STL containers on a cache-poor in-order Cortex-A7 against inline-allocating custom containers and index-plus-generation object pools on a sub-megabyte STM32H5, while drivebyhooting contended the proposed solution amounts to a clustered or locality-sensitive hash map and is not orders of magnitude better.

**Tags**: `#memory latency`, `#performance engineering`, `#CPU caches`, `#software optimization`, `#embedded systems`

---

<a id="item-tech-news-5"></a>
### [CXMT says sixth-gen 4F² DRAM samples pass validation](https://finance.sina.com.cn/roll/2026-10-31/doc-inixcsqk4704411.shtml) ⭐️ 7.0/10

Changxin Technology \(CXMT\) said on Oct. 31 that its sixth-generation DRAM process platform, based on a 4F² vertical-channel architecture, has completed engineering sample validation, the first time it has confirmed that architecture for the node. The company also plans to launch a new server DDR5 RDIMM incorporating 4F² technology by the end of the year. CXMT said it was the first to complete engineering-sample validation of 4F², a direction Samsung and SK Hynix have also identified as key below the 10nm class; this remains a vendor claim at the sample stage, with no disclosed yield, performance or mass-production timeline.

telegram · zaihuapd · Oct 31, 14:26

**「Background」** 4F² refers to a DRAM cell footprint of four feature squares, and a vertical-channel design changes the transistor orientation to support continued scaling; Samsung and SK Hynix have also identified 4F² as a key direction below the 10nm-class. Changxin had previously said it would launch a server-oriented DDR5 RDIMM using 4F² by the end of the year. Engineering-sample validation is an early step before customer qualification and mass production, so it does not by itself establish yield or volume readiness.

**「Qualification uncertainty remains」** Server OEMs and cloud operators now have a concrete product to track in ChangXin&\#x27;s planned year-end DDR5 RDIMM, but the company has disclosed only engineering-sample validation, with no yield, speed-bin, or mass-production data, so memory qualification and volume sourcing cannot yet rely on it. The immediate consequence is that procurement risk shifts from architecture feasibility to manufacturing ramp and reliability validation.

**Tags**: `#DRAM`, `#4F²架构`, `#长鑫科技`, `#半导体制造`, `#DDR5`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Fast and Slow Ways to Improve Your Reputation](https://seangoedecke.com/how-to-get-assigned-interesting-work/) ⭐️ 6.0/10

rss · Sean Goedecke · Nov 1, 00:00

**「Background」** Engineers need visible, important projects to build a reputation, yet those projects usually go to people who already have one. Sean Goedecke frames this as a problem of “tech company theory of mind”: formal processes may suggest fair rotation, but decisions actually follow managers’ incentives.

**「Solution」** The author argues that managers prioritize protecting their own reputation for delivering. Because high-profile projects fail often and a manager’s tenure may last only a couple of years, handing them to a known reliable engineer is rational in the short term, even though it creates a vicious cycle: the trusted engineer gains more experience while everyone else falls further behind. The slow remedy is a ratchet effect—ship small, low-risk work reliably, communicate it, earn slightly riskier work, and avoid mistakes that label you unreliable. That can take months or years and leaves room for bad luck or a manager change. Faster paths are explicitly “dangerous advice”: build genuine usefulness to your skip-level, who can direct work your way but may distrust persuasion; make self-initiated “side bets,” risking wasted effort and managerial irritation; or impress engineer colleagues, who form technical opinions quickly and may recommend you to their manager. The peer route works best on healthy teams; unhealthy ones may fail to recognize good engineers or actively undermine them.

**「Takeaway」** Goedecke’s conclusion is that trying to persuade a manager that exclusion is unfair is unlikely to work, because companies are meant to make money, not be fair. Instead, engineers should make assigning them interesting work appear to serve their manager’s interests.

**Tags**: `#career-development`, `#engineering-management`, `#organizational-incentives`, `#workplace-politics`, `#reputation`

---