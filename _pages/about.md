---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<style>
/* Research roadmap and industry project styles */
.research-intro {
  font-size: 1.02em;
  line-height: 1.72;
  color: #24292e;
  margin-bottom: 1rem;
}
.research-intro strong { color: #012F63; }
.language-switcher {
  margin: 1rem 0 1.4rem 0;
}
.language-tabs {
  display: inline-flex;
  gap: 0.35rem;
  padding: 0.28rem;
  border-radius: 999px;
  background: #f6f8fa;
  border: 1px solid rgba(1,47,99,0.08);
  box-shadow: 0 4px 14px rgba(1,47,99,0.05);
  margin-bottom: 1rem;
}
.lang-tab {
  border: 0;
  border-radius: 999px;
  padding: 0.42rem 0.92rem;
  background: transparent;
  color: #586069;
  font-size: 0.86rem;
  font-weight: 850;
  cursor: pointer;
  transition: all 0.2s ease;
}
.lang-tab:hover,
.lang-tab.active {
  color: #fff;
  background: linear-gradient(135deg, #FE667B 0%, #6aa9ff 100%);
  box-shadow: 0 6px 16px rgba(254,102,123,0.18);
}
.lang-panel { display: none; }
.lang-panel.active { display: block; }
/* Global bilingual blocks controlled by the top language tabs */
.i18n-zh,
.i18n-zh-inline,
.i18n-zh-flex,
.i18n-zh-list { display: none !important; }
body.lang-zh .i18n-en,
body.lang-zh .i18n-en-inline,
body.lang-zh .i18n-en-flex,
body.lang-zh .i18n-en-list { display: none !important; }
body.lang-zh .i18n-zh { display: block !important; }
body.lang-zh .i18n-zh-inline { display: inline !important; }
body.lang-zh .i18n-zh-flex { display: inline-flex !important; }
body.lang-zh .i18n-zh-list { display: list-item !important; }
body.lang-en .i18n-en { display: block !important; }
body.lang-en .i18n-en-inline { display: inline !important; }
body.lang-en .i18n-en-flex { display: inline-flex !important; }
body.lang-en .i18n-en-list { display: list-item !important; }
.industry-project-title {
  margin-bottom: 0.75rem;
  color: #24292e;
  line-height: 1.55;
}
.open-science-note {
  margin: 1rem 0 1.8rem 0;
  padding: 1rem 1.1rem;
  border-left: 4px solid #0366d6;
  border-radius: 12px;
  background: linear-gradient(180deg, #f8fbff 0%, #ffffff 100%);
  box-shadow: 0 6px 18px rgba(1,47,99,0.06);
  color: #012F63;
}
.open-science-note p {
  margin: 0.35rem 0;
  line-height: 1.65;
}
.research-map {
  margin: 1.4rem 0 1.8rem 0;
  padding: 1.2rem;
  border: 1px dashed rgba(1,47,99,0.22);
  border-radius: 18px;
  background: linear-gradient(180deg, #fff 0%, #f8fbff 100%);
  box-shadow: 0 10px 30px rgba(1,47,99,0.06);
}
.research-map-caption {
  text-align: center;
  font-weight: 700;
  color: #012F63;
  margin-bottom: 0.9rem;
}
.research-lane-label {
  display: inline-block;
  font-size: 0.82rem;
  font-weight: 700;
  border-radius: 999px;
  padding: 0.28rem 0.75rem;
  margin: 0.2rem 0 0.65rem 0;
}
.research-map > .research-lane-label {
  display: table;
  margin-left: auto;
  margin-right: auto;
  text-align: center;
  margin-top: 0.35rem;
  margin-bottom: 0.85rem;
}
.research-lane > .research-lane-label {
  grid-column: 1 / -1;
  justify-self: center;
  text-align: center;
  margin-top: 1.25rem;
  margin-bottom: 0;
}
.research-lane.bottom-lane > .research-lane-label.blue {
  transform: translateY(-1.2rem);
}
.research-lane-label.orange { color: #a54816; background: #fff0e6; border: 1px dashed #ffc7a0; }
.research-lane-label.blue { color: #174f91; background: #eaf4ff; border: 1px dashed #a9cff7; }
.research-lane {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 0.85rem;
}
.research-lane.top-lane { margin-bottom: 2.75rem; }
.research-lane.bottom-lane { margin-top: 2.75rem; }
.research-node {
  display: block;
  position: relative;
  min-height: 132px;
  padding: 0.85rem 0.8rem;
  border-radius: 14px;
  text-decoration: none !important;
  color: inherit !important;
  background: #fff;
  border: 1px solid rgba(1,47,99,0.08);
  box-shadow: 0 6px 18px rgba(1,47,99,0.07);
  transition: transform 0.25s ease, box-shadow 0.25s ease, border-color 0.25s ease;
}
.research-node:hover {
  transform: translateY(-6px);
  box-shadow: 0 14px 32px rgba(1,47,99,0.14);
  border-color: rgba(254,102,123,0.35);
}
.research-node.orange { background: linear-gradient(180deg, #fffaf6, #ffffff); }
.research-node.blue { background: linear-gradient(180deg, #f6fbff, #ffffff); }
.research-node.orange:before,
.research-node.blue:before {
  content: '';
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  width: 12px;
  height: 12px;
  border-radius: 50%;
  background: #fff;
  z-index: 3;
}
.research-node.orange:after,
.research-node.blue:after {
  content: '';
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  width: 0;
  height: 2.75rem;
  z-index: 2;
}
.research-node.orange:before {
  bottom: -1.08rem;
  border: 2px solid #f39a54;
  box-shadow: 0 0 0 4px rgba(243,154,84,0.10);
}
.research-node.orange:after {
  bottom: -2.75rem;
  border-left: 2px dashed rgba(243,154,84,0.78);
}
.research-node.blue:before {
  top: -1.08rem;
  border: 2px solid #4d96dd;
  box-shadow: 0 0 0 4px rgba(77,150,221,0.10);
}
.research-node.blue:after {
  top: -2.75rem;
  border-left: 2px dashed rgba(77,150,221,0.78);
}
.node-title { font-weight: 800; color: #012F63; margin-bottom: 0.32rem; }
.node-desc { font-size: 0.78rem; color: #586069; line-height: 1.42; min-height: 2.2rem; }
.node-papers { margin-top: 0.55rem; font-size: 0.78rem; font-weight: 700; color: #FE667B; line-height: 1.35; }
.node-paper-link {
  display: inline-block;
  margin: 0.12rem 0.16rem 0.12rem 0;
  padding: 0.16rem 0.42rem;
  border-radius: 999px;
  color: #FE667B !important;
  background: rgba(254,102,123,0.08);
  border: 1px solid rgba(254,102,123,0.16);
  text-decoration: none !important;
  transition: all 0.22s ease;
}
.node-paper-link:hover {
  color: #fff !important;
  background: #FE667B;
  border-color: #FE667B;
}
.roadmap-back-btn {
  position: fixed;
  right: 24px;
  bottom: 24px;
  z-index: 999;
  display: none;
  align-items: center;
  gap: 0.35rem;
  padding: 0.65rem 1rem;
  border-radius: 999px;
  border: 1px solid rgba(1,47,99,0.12);
  background: linear-gradient(135deg, #012F63 0%, #2f6fb3 100%);
  color: #fff !important;
  font-size: 0.86rem;
  font-weight: 800;
  text-decoration: none !important;
  box-shadow: 0 10px 28px rgba(1,47,99,0.22);
  opacity: 0;
  transform: translateY(10px);
  transition: opacity 0.22s ease, transform 0.22s ease, box-shadow 0.22s ease;
}
.roadmap-back-btn.show {
  display: inline-flex;
  opacity: 1;
  transform: translateY(0);
}
.roadmap-back-btn:hover {
  color: #fff !important;
  box-shadow: 0 14px 36px rgba(1,47,99,0.30);
  transform: translateY(-2px);
}
.research-arrow {
  position: relative;
  margin: 1rem 2.4rem 1rem 0;
  height: 56px;
  border-radius: 999px 0 0 999px;
  background: linear-gradient(90deg, #ffd6b5 0%, #ffd3dc 42%, #9ec7ff 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  color: #fff;
  font-weight: 800;
  letter-spacing: 0.01em;
  text-shadow: 0 1px 5px rgba(1,47,99,0.28);
  box-shadow: inset 0 0 0 1px rgba(255,255,255,0.45), 0 8px 24px rgba(1,47,99,0.08);
}
.research-arrow:after {
  content: '';
  position: absolute;
  right: -38px;
  top: -7px;
  width: 0;
  height: 0;
  border-top: 35px solid transparent;
  border-bottom: 35px solid transparent;
  border-left: 40px solid #9ec7ff;
}
.huawei-highlights {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 0.55rem 1rem;
  margin-top: 0.75rem;
  font-size: 0.9em;
}
.huawei-highlights span {
  display: block;
  background: #f6f8fa;
  border: 1px solid #eaecef;
  border-radius: 10px;
  padding: 0.45rem 0.6rem;
  line-height: 1.55;
  min-width: 0;
  overflow-wrap: anywhere;
}
.huawei-highlights span span {
  display: inline;
  background: transparent;
  border: 0;
  border-radius: 0;
  padding: 0;
  line-height: inherit;
  overflow-wrap: normal;
}
.opensource-section {
  margin: 2rem 0 2.2rem 0;
  padding: 1.2rem;
  border-radius: 18px;
  border: 1px solid rgba(1,47,99,0.08);
  background: linear-gradient(180deg, #ffffff 0%, #f8fbff 100%);
  box-shadow: 0 10px 30px rgba(1,47,99,0.06);
}
.section-kicker {
  display: inline-flex;
  align-items: center;
  gap: 0.45rem;
  padding: 0.28rem 0.75rem;
  border-radius: 999px;
  background: rgba(254,102,123,0.08);
  color: #FE667B;
  font-size: 0.78rem;
  font-weight: 800;
  letter-spacing: 0.02em;
  text-transform: uppercase;
}
.opensource-title {
  margin: 0.65rem 0 0.3rem 0;
  color: #012F63;
  font-size: 1.45rem;
  font-weight: 850;
}
.opensource-subtitle {
  margin: 0 0 1.05rem 0;
  color: #586069;
  line-height: 1.65;
}
.opensource-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 0.85rem;
  max-height: calc(225px * 2 + 0.85rem);
  overflow-y: auto;
  padding-right: 0.35rem;
  scroll-behavior: smooth;
}
.opensource-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  min-height: 225px;
  padding: 1rem 0.85rem;
  border-radius: 15px;
  border: 1px solid rgba(1,47,99,0.08);
  background: #fff;
  box-shadow: 0 6px 18px rgba(1,47,99,0.07);
  text-decoration: none !important;
  color: inherit !important;
  transition: transform 0.24s ease, box-shadow 0.24s ease, border-color 0.24s ease;
}
.opensource-card:hover {
  transform: translateY(-6px);
  box-shadow: 0 14px 32px rgba(1,47,99,0.14);
  border-color: rgba(254,102,123,0.32);
}
.opensource-grid::-webkit-scrollbar,
.news-grid::-webkit-scrollbar { width: 8px; }
.opensource-grid::-webkit-scrollbar-thumb,
.news-grid::-webkit-scrollbar-thumb {
  background: linear-gradient(180deg, #FE667B 0%, #6aa9ff 100%);
  border-radius: 999px;
}
.opensource-grid::-webkit-scrollbar-track,
.news-grid::-webkit-scrollbar-track {
  background: #f1f5f9;
  border-radius: 999px;
}
.opensource-card img {
  width: auto;
  height: 98px;
  max-width: 80%;
  object-fit: contain;
  border-radius: 8px;
  margin-bottom: 0.75rem;
  transform: none !important;
  box-shadow: none !important;
  transition: none !important;
}
.opensource-card:hover img {
  transform: none !important;
  box-shadow: none !important;
}
.opensource-card-title,
.opensource-card-meta,
.opensource-card-links { position: relative; z-index: 2; }
.opensource-card-title {
  color: #012F63;
  font-size: 0.95rem;
  font-weight: 850;
  margin-bottom: 0.25rem;
}
.opensource-card-meta {
  color: #FE667B;
  font-size: 0.78rem;
  font-weight: 750;
  margin-bottom: 0.4rem;
}
.opensource-card-links {
  margin-top: auto;
  display: flex;
  flex-wrap: wrap;
  gap: 0.3rem;
  justify-content: center;
}
.opensource-card-links a {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: 0.18rem 0.52rem;
  border-radius: 999px;
  border: 1px solid rgba(3,102,214,0.16);
  background: rgba(3,102,214,0.06);
  color: #0366d6 !important;
  font-size: 0.72rem;
  font-weight: 750;
  text-decoration: none !important;
  cursor: pointer;
  transition: all 0.2s ease;
}
.opensource-card-links a:hover {
  transform: translateY(-2px);
  background: #0366d6;
  border-color: #0366d6;
  color: #fff !important;
  box-shadow: 0 6px 16px rgba(3,102,214,0.22);
}
.news-section {
  margin: 2rem 0 2.2rem 0;
  padding: 1.2rem;
  border-radius: 18px;
  border: 1px solid rgba(1,47,99,0.08);
  background: linear-gradient(180deg, #ffffff 0%, #f8fbff 100%);
  box-shadow: 0 10px 30px rgba(1,47,99,0.06);
}
.news-title {
  margin: 0.65rem 0 1rem 0;
  color: #012F63;
  font-size: 1.45rem;
  font-weight: 850;
}
.news-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 0.75rem;
  max-height: 430px;
  overflow-y: auto;
  padding-right: 0.35rem;
  scroll-behavior: smooth;
}
.news-card {
  position: relative;
  display: grid;
  grid-template-columns: 6.8rem 1fr;
  gap: 0.8rem;
  align-items: start;
  padding: 0.9rem 0.95rem;
  border-radius: 14px;
  border: 1px solid rgba(1,47,99,0.08);
  background: #fff;
  box-shadow: 0 6px 18px rgba(1,47,99,0.06);
  transition: transform 0.22s ease, box-shadow 0.22s ease, border-color 0.22s ease;
}
.news-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 12px 28px rgba(1,47,99,0.12);
  border-color: rgba(254,102,123,0.22);
}

.news-date {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  min-height: 2rem;
  padding: 0.26rem 0.5rem;
  border-radius: 999px;
  color: #fff;
  background: linear-gradient(135deg, #FE667B 0%, #6aa9ff 100%);
  font-size: 0.78rem;
  font-weight: 850;
  box-shadow: 0 5px 14px rgba(254,102,123,0.18);
}
.news-text {
  color: #24292e;
  font-size: 0.92rem;
  line-height: 1.55;
}
.news-text strong { color: #012F63; }

.highlight-red { color: #FE667B; font-weight: 850; }
.highlight-blue { color: #0366d6; font-weight: 850; }
.highlight-gold { color: #b7791f; font-weight: 850; }
.award-ribbon {
  display: flex;
  flex-wrap: wrap;
  gap: 0.45rem;
  margin: 0.65rem 0 0.8rem 0;
}
.award-ribbon span {
  display: inline-flex;
  align-items: center;
  padding: 0.34rem 0.72rem;
  border-radius: 999px;
  color: #7a4b00;
  background: linear-gradient(135deg, #fff7d6, #ffe5a3);
  border: 1px solid rgba(183,121,31,0.22);
  font-size: 0.82rem;
  font-weight: 850;
}
.benchmark-orgs {
  margin-top: 0.8rem;
  padding: 0.85rem;
  border-radius: 14px;
  background: linear-gradient(180deg, #f8fbff 0%, #ffffff 100%);
  border: 1px solid rgba(1,47,99,0.08);
}
.benchmark-orgs-title {
  color: #012F63;
  font-weight: 850;
  margin-bottom: 0.55rem;
}
.org-logo-strip {
  display: flex;
  flex-wrap: wrap;
  gap: 0.55rem;
  align-items: center;
}
.org-logo-card {
  display: inline-flex;
  align-items: center;
  gap: 0.35rem;
  min-height: 34px;
  padding: 0.32rem 0.58rem;
  border-radius: 10px;
  background: #fff;
  border: 1px solid rgba(1,47,99,0.08);
  box-shadow: 0 3px 10px rgba(1,47,99,0.05);
  color: #24292e;
  font-size: 0.78rem;
  font-weight: 750;
}
.org-logo-card img {
  width: 22px;
  height: 22px;
  object-fit: contain;
}
@media (max-width: 720px) {
  .research-lane { grid-template-columns: 1fr; }
  .research-lane.top-lane, .research-lane.bottom-lane { margin: 0; }
  .research-node.orange:before, .research-node.orange:after, .research-node.blue:before, .research-node.blue:after { display: none; }
  .research-arrow { height: auto; min-height: 58px; padding: 0.75rem 1rem; text-align: center; border-radius: 18px; }
  .research-arrow:after { display: none; }
  .huawei-highlights { grid-template-columns: 1fr; }
  .opensource-grid { grid-template-columns: 1fr; }
  .news-grid { grid-template-columns: 1fr; }
  .news-card { grid-template-columns: 1fr; }
  .roadmap-back-btn { right: 14px; bottom: 14px; padding: 0.55rem 0.8rem; font-size: 0.78rem; }
}

/* 动态标签和过滤器按钮的预设样式 */
#filter-container {
  margin: 20px 0;
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
}
.filter-btn {
  padding: 6px 14px;
  border: 1px solid #e1e4e8;
  border-radius: 20px;
  background-color: #f6f8fa;
  color: #586069;
  font-size: 0.85em;
  cursor: pointer;
  transition: all 0.2s ease;
}
.filter-btn:hover {
  background-color: #eaecef;
  color: #24292e;
}
.filter-btn.active {
  background: linear-gradient(135deg, #38ef7d, #11998e);
  color: white;
  border-color: transparent;
  box-shadow: 0 2px 8px rgba(17, 153, 142, 0.3);
}
.badge-container {
  margin-top: 8px;
  margin-bottom: 8px;
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
}
.inner-tag-badge {
  font-size: 0.75em;
  padding: 2px 8px;
  background-color: #f1f3f5;
  color: #495057;
  border-radius: 4px;
  border: 1px solid #e9ecef;
  transition: all 0.2s ease;
}
.inner-tag-badge.active {
  background-color: #e8f5e9;
  color: #2e7d32;
  border-color: #a5d6a7;
  font-weight: bold;
}
.venue-full-name {
  font-size: 0.85em;
  color: #6a737d;
  font-style: italic;
  margin: 4px 0;
}
.paper-link-container {
  margin-top: 8px;
}
.paper-link-btn {
  font-size: 0.85em;
  padding: 2px 8px;
  margin-right: 4px;
  background-color: #fff;
  border: 1px solid #0366d6;
  color: #0366d6 !important;
  border-radius: 4px;
  text-decoration: none !important;
}
.paper-link-btn:hover {
  background-color: #0366d6;
  color: #fff !important;
}
.author-self {
  font-weight: bold;
  text-decoration: underline;
}
.floating-card {
  transition: opacity 0.3s ease;
}
.paper-box {
  border: 2px solid transparent !important;
  background: linear-gradient(#ffffff, #ffffff) padding-box,
              linear-gradient(135deg, rgba(1,47,99,0.08), rgba(1,47,99,0.08)) border-box !important;
}
.paper-box::before {
  display: none !important;
}
.paper-box:hover {
  background: linear-gradient(#ffffff, #ffffff) padding-box,
              linear-gradient(135deg, #FE667B 0%, #ff8599 45%, #a29bfe 100%) border-box !important;
  border-color: transparent !important;
}
</style>
 
{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>

Hi, I am Zixu Li (李子旭).
=====
 
<!-- I am a Ph.D. student in Artificial Intelligence at [Shandong University](https://www.sdu.edu.cn), under the supervision of Prof. [Liqiang Nie](https://liqiangnie.github.io/index.html) and Prof. [Yupeng Hu](https://faculty.sdu.edu.cn/huyupeng1/zh_CN/index.htm). In 2023, I received my Bachelor's degree in Data Science and Big Data Technology from [Shandong University](https://www.sdu.edu.cn). -->

<div class="language-switcher" id="research-language-switcher">
  <div class="language-tabs" role="tablist" aria-label="Research introduction language selector">
    <button class="lang-tab active" type="button" data-lang="en" role="tab" aria-selected="true">English</button>
    <button class="lang-tab" type="button" data-lang="zh" role="tab" aria-selected="false">中文</button>
  </div>

  <div class="lang-panel active" data-lang-panel="en" role="tabpanel">
    <div class="research-intro">
      <p>Welcome to my homepage! I am currently a Ph.D. student in Artificial Intelligence at <a href="https://www.sdu.edu.cn">Shandong University</a>, and I am honored to be advised by Prof. <a href="https://liqiangnie.github.io/index.html">Liqiang Nie</a> and Prof. <a href="https://faculty.sdu.edu.cn/huyupeng1/zh_CN/index.htm">Yupeng Hu</a>. Prior to this, I received my Bachelor's degree in Data Science and Big Data Technology from <a href="https://www.sdu.edu.cn">Shandong University</a> in 2023. My research interests mainly focus on <strong>large multimodal models, robust representation learning, and trustworthy AI</strong>.</p>
      <p>In my research, I systematically explore the main theme of <strong>from multimodal understanding to evidence-driven large model evaluation</strong>. As first author or Project Leader, I have published more than ten papers in CCF-A international conferences and journals, including <strong>CVPR, ACL, AAAI, ACM MM, TIP, and TKDE</strong>. I have also won champion, runner-up, and third-place awards multiple times in top-tier conference challenges such as CVPR. In addition, I have long served as a PC Member for <strong>CVPR, ECCV, ICLR, NeurIPS, AAAI, ACM MM, and SIGIR</strong>, and as a reviewer for journals including <strong>IEEE TIP</strong> and <strong>IEEE TIFS</strong>.</p>
      <p>For industrial deployment, I served as the student lead of a Huawei collaboration project on general-purpose vector retrieval, where I led the design and optimization of the <strong>QSGNGT</strong> algorithm. Since 2023, this work has continuously ranked first worldwide on the official <strong>ANN-Benchmarks</strong> leaderboard, outperforming competing algorithms from Google, Microsoft, Meta, Yahoo, JD.com, Alibaba, and other companies. The algorithm has also been successfully deployed as the retrieval core of Huawei Cloud GaussDB's hundred-billion-scale vector database. For these technical breakthroughs, I received the <strong>Huawei Outstanding Technical Collaboration Award</strong> and the <strong>Huawei Outstanding Student Award</strong>.</p>
    </div>
    <div class="research-map" id="research-map">
      <div class="research-map-caption">From Multimodal Understanding to Evidence-driven Large Model Evaluation</div>
      <div class="research-lane-label orange">Representation Optimization and Algorithm Design for Multimodal Understanding</div>
      <div class="research-lane top-lane">
        <div class="research-node orange">
          <div class="node-title">Multimodal Semantic Fusion</div>
          <div class="node-desc">Designing entity-attribute-relation alignment algorithms to optimize cross-modal semantic interaction structures.</div>
          <div class="node-papers"><a class="node-paper-link" href="#paper-encoder">ENCODER [AAAI 2025]</a><a class="node-paper-link" href="#paper-temp-ret">TempRet [CVPRW 2026]</a></div>
        </div>
        <div class="research-node orange">
          <div class="node-title">Complex-scene Intent Feature Disentanglement</div>
          <div class="node-desc">Developing robust denoising and feature extraction algorithms for complex noise and intent distortion.</div>
          <div class="node-papers"><a class="node-paper-link" href="#paper-habit">HABIT [AAAI 2026]</a><a class="node-paper-link" href="#paper-intent">INTENT [AAAI 2026]</a><a class="node-paper-link" href="#paper-egoaction">EgoAction [CVPRW 2026]</a></div>
        </div>
        <div class="research-node orange">
          <div class="node-title">Attribute-aware Efficient Representation</div>
          <div class="node-desc">Building lightweight yet accurate representation learning with attribute-neighborhood topology and acceleration strategies.</div>
          <div class="node-papers"><a class="node-paper-link" href="#paper-combiner">COMBINER [TIP 2026]</a><a class="node-paper-link" href="#paper-stable">STABLE [TKDE 2026]</a><a class="node-paper-link" href="#paper-refine">REFINE [ToMM 2026]</a><a class="node-paper-link" href="#paper-omniego">OmniEgo-R<sup>2</sup> [CVPRW 2026]</a></div>
        </div>
      </div>
      <div class="research-arrow">From Multimodal Understanding to Evidence-Driven Evaluation of Large Models</div>
      <div class="research-lane bottom-lane">
        <div class="research-node blue">
          <div class="node-title">Evidence-driven Hallucination Diagnosis and Disambiguation</div>
          <div class="node-desc">Constructing multimodal external evidence chains to evaluate and mitigate model uncertainty and hallucination.</div>
          <div class="node-papers"><a class="node-paper-link" href="#paper-retrack">ReTrack [AAAI 2026]</a><a class="node-paper-link" href="#paper-hud">HUD [ACM MM 2025]</a><a class="node-paper-link" href="#paper-r3">R<sup>3</sup> [CVPRW 2026]</a></div>
        </div>
        <div class="research-node blue">
          <div class="node-title">Trustworthy Knowledge Calibration</div>
          <div class="node-desc">Building noise-separation frameworks for calibrated and trustworthy alignment of large-model outputs.</div>
          <div class="node-papers"><a class="node-paper-link" href="#paper-conesep">ConeSep [CVPR 2026]</a><a class="node-paper-link" href="#paper-airknow">Air-Know [CVPR 2026]</a><a class="node-paper-link" href="#paper-offset">OFFSET [ACM MM 2025]</a></div>
        </div>
        <div class="research-node blue">
          <div class="node-title">Fine-grained Evaluation Benchmark Construction</div>
          <div class="node-desc">Constructing fine-grained multimodal benchmarks for complex contextual and open-world scenarios.</div>
          <div class="node-papers"><a class="node-paper-link" href="#paper-tema">TEMA [ACL 2026 Main]</a><a class="node-paper-link" href="#paper-finecir">FineCIR [Preprint]</a><a class="node-paper-link" href="#paper-egoadapt">EgoAdapt [CVPRW 2026]</a></div>
        </div>
      </div>
        <div class="research-lane-label blue">Diagnostic Frameworks and Benchmark Evaluation for Trustworthy Large Models</div>
    </div>
  </div>

  <div class="lang-panel" data-lang-panel="zh" role="tabpanel">
    <div class="research-intro">
      <p>欢迎来到我的主页！我目前是山东大学人工智能专业的博士生，很荣幸师从 Prof. <a href="https://liqiangnie.github.io/index.html">Liqiang Nie</a> 与 Prof. <a href="https://faculty.sdu.edu.cn/huyupeng1/zh_CN/index.htm">Yupeng Hu</a>。在此之前，我于2023年在山东大学获得数据科学与大数据技术专业学士学位。我的研究兴趣主要聚焦于<strong>多模态大模型、鲁棒表征学习、可信AI</strong>。</p>
      <p>在科研探索中，我紧密围绕“<strong>从多模态理解到证据驱动的大模型评测</strong>”这一主线展开系统性研究，以第一作者/Project Leader身份在 <strong>CVPR、ACL、AAAI、ACM MM、TIP、TKDE</strong> 等CCF A类国际会议与期刊上发表论文10余篇，并多次获得CVPR等顶会挑战赛的获冠、亚、季军。此外，我长期担任 <strong>CVPR, ECCV, ICLR, NeurIPS, AAAI, ACM MM, SIGIR</strong> 等会议的PC Member和 <strong>IEEE TIP、IEEE TIFS</strong> 等期刊的审稿人。</p>
      <p>在产业落地方面，我曾作为学生负责人参与华为通用向量检索合作项目，主导了<strong>QSGNGT</strong>算法的设计与优化，该成果于2023年至今蝉联ANN-Benchmarks官方测评世界第一，算法性能超越谷歌、微软、Meta、雅虎、京东、阿里巴巴等企业的竞品算法。同时，该算法已作为检索核心成功应用于华为云GaussDB千亿级向量数据库。凭借上述技术突破，我荣获“<strong>华为优秀技术合作成果奖</strong>”与“<strong>华为优秀学生奖</strong>”。</p>
    </div>
    <div class="research-map">
      <div class="research-map-caption">从多模态理解到证据驱动的大模型评测</div>
      <div class="research-lane-label orange">面向多模态理解的表征优化与算法设计</div>
      <div class="research-lane top-lane">
        <div class="research-node orange">
          <div class="node-title">多模态融合语义理解</div>
          <div class="node-desc">设计实体-属性-关系对齐算法，优化跨模态语义交互结构。</div>
          <div class="node-papers"><a class="node-paper-link" href="#paper-encoder">ENCODER [AAAI 2025]</a><a class="node-paper-link" href="#paper-temp-ret">TempRet [CVPRW 2026]</a></div>
        </div>
        <div class="research-node orange">
          <div class="node-title">复杂场景意图特征解耦</div>
          <div class="node-desc">针对复杂噪声与意图畸变，设计鲁棒的去噪与特征提取算法。</div>
          <div class="node-papers"><a class="node-paper-link" href="#paper-habit">HABIT [AAAI 2026]</a><a class="node-paper-link" href="#paper-intent">INTENT [AAAI 2026]</a><a class="node-paper-link" href="#paper-egoaction">EgoAction [CVPRW 2026]</a></div>
        </div>
        <div class="research-node orange">
          <div class="node-title">属性感知高效表征</div>
          <div class="node-desc">基于属性邻域拓扑与加速策略，实现轻量化高精度的表征学习。</div>
          <div class="node-papers"><a class="node-paper-link" href="#paper-combiner">COMBINER [TIP 2026]</a><a class="node-paper-link" href="#paper-stable">STABLE [TKDE 2026]</a><a class="node-paper-link" href="#paper-refine">REFINE [ToMM 2026]</a><a class="node-paper-link" href="#paper-omniego">OmniEgo-R<sup>2</sup> [CVPRW 2026]</a></div>
        </div>
      </div>
      <div class="research-arrow">从多模态理解到证据驱动的大模型评测</div>
      <div class="research-lane bottom-lane">
        <div class="research-node blue">
          <div class="node-title">证据驱动的幻觉诊断与消歧</div>
          <div class="node-desc">构建多模态外部证据链，评估并消除模型的不确定性与幻觉。</div>
          <div class="node-papers"><a class="node-paper-link" href="#paper-retrack">ReTrack [AAAI 2026]</a><a class="node-paper-link" href="#paper-hud">HUD [ACM MM 2025]</a><a class="node-paper-link" href="#paper-r3">R<sup>3</sup> [CVPRW 2026]</a></div>
        </div>
        <div class="research-node blue">
          <div class="node-title">可信知识校准</div>
          <div class="node-desc">构建噪声分离框架，实现大模型输出的校准与可信对齐。</div>
          <div class="node-papers"><a class="node-paper-link" href="#paper-conesep">ConeSep [CVPR 2026]</a><a class="node-paper-link" href="#paper-airknow">Air-Know [CVPR 2026]</a><a class="node-paper-link" href="#paper-offset">OFFSET [ACM MM 2025]</a></div>
        </div>
        <div class="research-node blue">
          <div class="node-title">细粒度评测基准构建</div>
          <div class="node-desc">针对复杂上下文场景，构建细粒度多模态评测基准。</div>
          <div class="node-papers"><a class="node-paper-link" href="#paper-tema">TEMA [ACL 2026 Main]</a><a class="node-paper-link" href="#paper-finecir">FineCIR [Preprint]</a><a class="node-paper-link" href="#paper-egoadapt">EgoAdapt [CVPRW 2026]</a></div>
        </div>
      </div>
      <div class="research-lane-label blue">面向可信大模型的诊断框架与基准评测</div>
    </div>
  </div>
</div>

<a class="roadmap-back-btn" id="roadmap-back-btn" href="#research-map" aria-label="Back to research roadmap"><span class="i18n-en-inline">↩ Back to Roadmap</span><span class="i18n-zh-inline">↩ 返回研究路线图</span></a>

<div class="open-science-note">
  <div class="i18n-en">
    <p><strong>Open Science.</strong> I firmly believe in the power of open science. Currently, all the major projects I am involved in are fully open source. Additionally, as a member of the Intelligent Media Research Center (iLearn), all of our lab’s papers and code are open source. Please visit <a href="https://github.com/iLearn-Lab">iLearn Lab</a> and feel free to share your valuable feedback.</p>
  </div>
  <div class="i18n-zh">
    <p><strong>开放科学.</strong> 作为开放科学的坚定拥趸，我致力于将研究成果开源，以促进社区的交流与发展。</p>
    <p><strong>💻 个人项目：</strong>我主要参与的项目均已全面开源，欢迎访问我们的项目主页，非常期待您的真实反馈（欢迎提出 Issue 或 PR）！</p>
    <p><strong>🏫 实验室组织：</strong>我隶属于智能媒体研究中心 (iLearn)，实验室的论文代码与相关项目也已悉数开源，欢迎访问 <a href="https://github.com/iLearn-Lab">iLearn Lab</a> 并提供宝贵意见。</p>
  </div>
</div>

<div class="opensource-section" id="open-source-projects">
  <div class="section-kicker"><span class="i18n-en-inline">💻 Open Science</span><span class="i18n-zh-inline">💻 开放科学</span></div>
  <div class="opensource-title"><span class="i18n-en-inline">Our Open Source Projects</span><span class="i18n-zh-inline">我们的开源项目</span></div>
  <p class="opensource-subtitle i18n-en">I believe open-source research makes multimodal learning more reproducible and collaborative. Below are representative project pages and repositories from my recent works.</p>
  <p class="opensource-subtitle i18n-zh">我相信开源研究能够提升多模态学习的可复现性与协作性。以下是我近期代表性工作的项目主页与代码仓库。</p>
  <div class="opensource-grid" id="opensource-grid">
    <div class="opensource-card">
      <img src="../images/combiner-logo.png" alt="COMBINER">
      <div class="opensource-card-title">COMBINER</div>
      <div class="opensource-card-meta"><span class="i18n-en-inline">TIP 2026 · Attribute-aware Efficient Representation</span><span class="i18n-zh-inline">TIP 2026 · 属性感知高效表征</span></div>
      <div class="opensource-card-links">        <a href="https://ieeexplore.ieee.org/abstract/document/11534406" target="_blank" title="Open COMBINER paper"><span class="i18n-en-inline">Paper</span><span class="i18n-zh-inline">论文</span></a>
        <a href="https://lee-zixu.github.io/COMBINER.github.io/" target="_blank" title="Open COMBINER project page"><span class="i18n-en-inline">Project</span><span class="i18n-zh-inline">项目</span></a>
        <a href="https://github.com/Lee-zixu/COMBINER" target="_blank" title="Open COMBINER code repository"><span class="i18n-en-inline">Code</span><span class="i18n-zh-inline">代码</span></a>
      </div>
    </div>
    <div class="opensource-card">
      <img src="../images/tema-logo.png" alt="TEMA">
      <div class="opensource-card-title">TEMA</div>
      <div class="opensource-card-meta"><span class="i18n-en-inline">ACL 2026 Main · Benchmark</span><span class="i18n-zh-inline">ACL 2026 Main · 评测基准</span></div>
      <div class="opensource-card-links">        <a href="https://arxiv.org/abs/2604.21806" target="_blank" title="Open TEMA paper"><span class="i18n-en-inline">Paper</span><span class="i18n-zh-inline">论文</span></a>
        <a href="https://lee-zixu.github.io/TEMA.github.io/" target="_blank" title="Open TEMA project page"><span class="i18n-en-inline">Project</span><span class="i18n-zh-inline">项目</span></a>
        <a href="https://github.com/Lee-zixu/ACL26-TEMA" target="_blank" title="Open TEMA code repository"><span class="i18n-en-inline">Code</span><span class="i18n-zh-inline">代码</span></a>
      </div>
    </div>
    <div class="opensource-card">
      <img src="../images/consep-logo.png" alt="ConeSep">
      <div class="opensource-card-title">ConeSep</div>
      <div class="opensource-card-meta"><span class="i18n-en-inline">CVPR 2026 · Robust Unlearning</span><span class="i18n-zh-inline">CVPR 2026 · 鲁棒噪声遗忘</span></div>
      <div class="opensource-card-links">        <a href="https://arxiv.org/abs/2604.20358" target="_blank" title="Open ConeSep paper"><span class="i18n-en-inline">Paper</span><span class="i18n-zh-inline">论文</span></a>
        <a href="https://lee-zixu.github.io/ConeSep.github.io/" target="_blank" title="Open ConeSep project page"><span class="i18n-en-inline">Project</span><span class="i18n-zh-inline">项目</span></a>
        <a href="https://github.com/Lee-zixu/ConeSep" target="_blank" title="Open ConeSep code repository"><span class="i18n-en-inline">Code</span><span class="i18n-zh-inline">代码</span></a>
      </div>
    </div>
    <div class="opensource-card">
      <img src="../images/airknow-logo.png" alt="Air-Know">
      <div class="opensource-card-title">Air-Know</div>
      <div class="opensource-card-meta"><span class="i18n-en-inline">CVPR 2026 · Knowledge Calibration</span><span class="i18n-zh-inline">CVPR 2026 · 知识校准</span></div>
      <div class="opensource-card-links">        <a href="http://arxiv.org/abs/2604.19386" target="_blank" title="Open Air-Know paper"><span class="i18n-en-inline">Paper</span><span class="i18n-zh-inline">论文</span></a>
        <a href="https://zhihfu.github.io/Air-Know.github.io/" target="_blank" title="Open Air-Know project page"><span class="i18n-en-inline">Project</span><span class="i18n-zh-inline">项目</span></a>
        <a href="https://github.com/ZhihFu/Air-Know" target="_blank" title="Open Air-Know code repository"><span class="i18n-en-inline">Code</span><span class="i18n-zh-inline">代码</span></a>
      </div>
    </div>
    <div class="opensource-card">
      <img src="../images/habit-logo.png" alt="HABIT">
      <div class="opensource-card-title">HABIT</div>
      <div class="opensource-card-meta"><span class="i18n-en-inline">AAAI 2026 · Robust Progressive Learning</span><span class="i18n-zh-inline">AAAI 2026 · 鲁棒渐进学习</span></div>
      <div class="opensource-card-links">        <a href="https://arxiv.org/abs/2604.18037" target="_blank" title="Open HABIT paper"><span class="i18n-en-inline">Paper</span><span class="i18n-zh-inline">论文</span></a>
        <a href="https://lee-zixu.github.io/HABIT.github.io/" target="_blank" title="Open HABIT project page"><span class="i18n-en-inline">Project</span><span class="i18n-zh-inline">项目</span></a>
        <a href="https://github.com/Lee-zixu/HABIT" target="_blank" title="Open HABIT code repository"><span class="i18n-en-inline">Code</span><span class="i18n-zh-inline">代码</span></a>
      </div>
    </div>
    <div class="opensource-card">
      <img src="../images/retrack-logo.png" alt="ReTrack">
      <div class="opensource-card-title">ReTrack</div>
      <div class="opensource-card-meta"><span class="i18n-en-inline">AAAI 2026 · Evidence-driven Reliable Reasoning</span><span class="i18n-zh-inline">AAAI 2026 · 证据驱动可靠推理</span></div>
      <div class="opensource-card-links">        <a href="http://arxiv.org/abs/2604.17898" target="_blank" title="Open ReTrack paper"><span class="i18n-en-inline">Paper</span><span class="i18n-zh-inline">论文</span></a>
        <a href="https://lee-zixu.github.io/ReTrack.github.io/" target="_blank" title="Open ReTrack project page"><span class="i18n-en-inline">Project</span><span class="i18n-zh-inline">项目</span></a>
        <a href="https://github.com/Lee-zixu/ReTrack" target="_blank" title="Open ReTrack code repository"><span class="i18n-en-inline">Code</span><span class="i18n-zh-inline">代码</span></a>
      </div>
    </div>
    <div class="opensource-card">
      <img src="../images/intent-logo.png" alt="INTENT">
      <div class="opensource-card-title">INTENT</div>
      <div class="opensource-card-meta"><span class="i18n-en-inline">AAAI 2026 · Intent Disentanglement</span><span class="i18n-zh-inline">AAAI 2026 · 意图解耦</span></div>
      <div class="opensource-card-links">        <a href="https://arxiv.org/abs/2604.18051" target="_blank" title="Open INTENT paper"><span class="i18n-en-inline">Paper</span><span class="i18n-zh-inline">论文</span></a>
        <a href="https://zivchen-ty.github.io/INTENT.github.io/" target="_blank" title="Open INTENT project page"><span class="i18n-en-inline">Project</span><span class="i18n-zh-inline">项目</span></a>
        <a href="https://github.com/ZivChen-Ty/INTENT" target="_blank" title="Open INTENT code repository"><span class="i18n-en-inline">Code</span><span class="i18n-zh-inline">代码</span></a>
      </div>
    </div>
    <div class="opensource-card">
      <img src="../images/hud-logo.png" alt="HUD">
      <div class="opensource-card-title">HUD</div>
      <div class="opensource-card-meta"><span class="i18n-en-inline">ACM MM 2025 · Uncertainty Disambiguation</span><span class="i18n-zh-inline">ACM MM 2025 · 不确定性消歧</span></div>
      <div class="opensource-card-links">        <a href="https://arxiv.org/abs/2512.02792" target="_blank" title="Open HUD paper"><span class="i18n-en-inline">Paper</span><span class="i18n-zh-inline">论文</span></a>
        <a href="https://zivchen-ty.github.io/HUD.github.io/" target="_blank" title="Open HUD project page"><span class="i18n-en-inline">Project</span><span class="i18n-zh-inline">项目</span></a>
        <a href="https://github.com/ZivChen-Ty/HUD" target="_blank" title="Open HUD code repository"><span class="i18n-en-inline">Code</span><span class="i18n-zh-inline">代码</span></a>
      </div>
    </div>
    <div class="opensource-card">
      <img src="../images/encoder-logo.png" alt="ENCODER">
      <div class="opensource-card-title">ENCODER</div>
      <div class="opensource-card-meta"><span class="i18n-en-inline">AAAI 2025 · Multimodal Semantic Fusion</span><span class="i18n-zh-inline">AAAI 2025 · 多模态语义融合</span></div>
      <div class="opensource-card-links">        <a href="https://ojs.aaai.org/index.php/AAAI/article/view/32541" target="_blank" title="Open ENCODER paper"><span class="i18n-en-inline">Paper</span><span class="i18n-zh-inline">论文</span></a>
        <a href="https://sdu-l.github.io/ENCODER.github.io/" target="_blank" title="Open ENCODER project page"><span class="i18n-en-inline">Project</span><span class="i18n-zh-inline">项目</span></a>
        <a href="https://github.com/Lee-zixu/ENCODER" target="_blank" title="Open ENCODER code repository"><span class="i18n-en-inline">Code</span><span class="i18n-zh-inline">代码</span></a>
      </div>
    </div>
    <div class="opensource-card">
      <img src="../images/offset-logo.png" alt="OFFSET">
      <div class="opensource-card-title">OFFSET</div>
      <div class="opensource-card-meta"><span class="i18n-en-inline">ACM MM 2025 · Trustworthy Knowledge Calibration</span><span class="i18n-zh-inline">ACM MM 2025 · 可信知识校准</span></div>
      <div class="opensource-card-links">        <a href="https://arxiv.org/abs/2507.05631" target="_blank" title="Open OFFSET paper"><span class="i18n-en-inline">Paper</span><span class="i18n-zh-inline">论文</span></a>
        <a href="https://zivchen-ty.github.io/OFFSET.github.io/" target="_blank" title="Open OFFSET project page"><span class="i18n-en-inline">Project</span><span class="i18n-zh-inline">项目</span></a>
        <a href="https://github.com/ZivChen-Ty/OFFSET" target="_blank" title="Open OFFSET code repository"><span class="i18n-en-inline">Code</span><span class="i18n-zh-inline">代码</span></a>
      </div>
    </div>
  </div>
</div>



<!-- I warmly welcome academic discussions and potential collaborations. Please feel free to contact me if you are interested in my research or possible cooperation.

欢迎就我的研究方向展开学术交流与合作，如果您有相关研究兴趣或合作意向，欢迎随时联系我。-->

 
<div class="news-section" id="news">
  <div class="section-kicker"><span class="i18n-en-inline">🔥 Updates</span><span class="i18n-zh-inline">🔥 最新动态</span></div>
  <div class="news-title"><span class="i18n-en-inline">News</span><span class="i18n-zh-inline">新闻动态</span></div>
  <div class="news-grid">
    <div class="news-card">
      <div class="news-date">2026.06.10</div>
      <div class="news-text"><span class="i18n-en-inline">🎉🎉 I was honored to receive the Shandong University Graduate Academic Star Award (Practical Application Category, 18 people in the whole university).</span><span class="i18n-zh-inline">🎉🎉 我荣获山东大学研究生学术之星（实践应用类，全校18人）。</span></div>
    </div>
    <div class="news-card">
      <div class="news-date">2026.06.02</div>
      <div class="news-text"><span class="i18n-en-inline">🎉🎉 Thrilled to share that our team won the <strong>1st Place</strong>🏅 in the Reasoned-Aware Composed Video Retrieval (CoVR-R) Challenge at the VidLLMs Workshop @ CVPR 2026! Congratulations to all members!</span><span class="i18n-zh-inline">🎉🎉 我们团队在 CVPR 2026 VidLLMs Workshop 的 Reasoned-Aware Composed Video Retrieval (CoVR-R) Challenge 中获得<strong>冠军</strong>🏅！祝贺所有成员！</span></div>
    </div>
    <div class="news-card">
      <div class="news-date">2026.05.14</div>
      <div class="news-text"><span class="i18n-en-inline">🎉🎉 Thrilled to share that our team won <strong>1st places</strong>🏅✖️2, <strong>2nd places</strong>🥈✖️2, and <strong>3rd place</strong>🥉✖️1 across multiple Challenges (HD-EPIC, EPIC-KITCHENS, and EgoCross) at the EgoVis Workshop @ CVPR 2026! Congratulations to all members!</span><span class="i18n-zh-inline">🎉🎉 我们团队在 CVPR 2026 EgoVis Workshop 的多个挑战赛（HD-EPIC、EPIC-KITCHENS 和 EgoCross）中获得<strong>冠军</strong>🏅✖️2、<strong>亚军</strong>🥈✖️2 和<strong>季军</strong>🥉✖️1！祝贺所有成员！</span></div>
    </div>
    <div class="news-card">
      <div class="news-date">2026.04.30</div>
      <div class="news-text"><span class="i18n-en-inline">🎉🎉 One paper (COMBINER), was accepted by <strong>TIP 2026</strong>! Thanks to all co-authors!</span><span class="i18n-zh-inline">🎉🎉 一篇论文（COMBINER）被 <strong>TIP 2026</strong> 接收！感谢所有合作者！</span></div>
    </div>
    <div class="news-card">
      <div class="news-date">2026.04.07</div>
      <div class="news-text"><span class="i18n-en-inline">🎉🎉 One paper (TEMA), was accepted by <strong>ACL 2026 Main</strong>! Thanks to all co-authors!</span><span class="i18n-zh-inline">🎉🎉 一篇论文（TEMA）被 <strong>ACL 2026 Main</strong> 接收！感谢所有合作者！</span></div>
    </div>
    <div class="news-card">
      <div class="news-date">2026.03.17</div>
      <div class="news-text"><span class="i18n-en-inline">🎉🎉 One paper (STABLE), was accepted by <strong>TKDE 2026</strong>! Congratulations to all co-authors!</span><span class="i18n-zh-inline">🎉🎉 一篇论文（STABLE）被 <strong>TKDE 2026</strong> 接收！祝贺所有合作者！</span></div>
    </div>
    <div class="news-card">
      <div class="news-date">2026.02.21</div>
      <div class="news-text"><span class="i18n-en-inline">🎉🎉 Two papers (ConeSep, Air-Know), were accepted by <strong>CVPR 2026</strong>! Thanks and Congratulations to all co-authors!</span><span class="i18n-zh-inline">🎉🎉 两篇论文（ConeSep、Air-Know）被 <strong>CVPR 2026</strong> 接收！感谢并祝贺所有合作者！</span></div>
    </div>
    <div class="news-card">
      <div class="news-date">2025.11.08</div>
      <div class="news-text"><span class="i18n-en-inline">🎉🎉 Three papers (ReTrack, INTENT, HABIT), were accepted by <strong>AAAI 2026</strong>! Thanks and Congratulations to all co-authors!</span><span class="i18n-zh-inline">🎉🎉 三篇论文（ReTrack、INTENT、HABIT）被 <strong>AAAI 2026</strong> 接收！感谢并祝贺所有合作者！</span></div>
    </div>
    <div class="news-card">
      <div class="news-date">2025.10.18</div>
      <div class="news-text"><span class="i18n-en-inline">🎉🎉 As the project leader, I led our team won the <strong>Grand Prize (特等奖)</strong> in the CICAS Smart Power Scenario Competition. Congratulations to all team members!</span><span class="i18n-zh-inline">🎉🎉 作为项目负责人，我带领团队获得 CICAS 智能电力场景竞赛<strong>特等奖</strong>！祝贺所有团队成员！</span></div>
    </div>
    <div class="news-card">
      <div class="news-date">2025.07.05</div>
      <div class="news-text"><span class="i18n-en-inline">🎉🎉 Two papers (OFFSET, HUD), were accepted by <strong>ACM MM 2025</strong>! Congratulations to all co-authors!</span><span class="i18n-zh-inline">🎉🎉 两篇论文（OFFSET、HUD）被 <strong>ACM MM 2025</strong> 接收！祝贺所有合作者！</span></div>
    </div>
    <div class="news-card">
      <div class="news-date">2024.12.10</div>
      <div class="news-text"><span class="i18n-en-inline">🎉🎉 One paper (ENCODER) was accepted by <strong>AAAI 2025</strong>! Thanks to all co-authors!</span><span class="i18n-zh-inline">🎉🎉 一篇论文（ENCODER）被 <strong>AAAI 2025</strong> 接收！感谢所有合作者！</span></div>
    </div>
    <div class="news-card">
      <div class="news-date">2024.09.13</div>
      <div class="news-text"><span class="i18n-en-inline">🎉🎉 I was honored to receive the <strong>Huawei Outstanding Student Award (Top 30 globally per year)</strong>, as well as the <strong>Huawei Outstanding Technical Collaboration Award (Top 10 globally per year)</strong>.</span><span class="i18n-zh-inline">🎉🎉 我荣获<strong>华为优秀学生奖（全球每年 Top 30）</strong>以及<strong>华为优秀技术合作成果奖（全球每年 Top 10）</strong>。</span></div>
    </div>
  </div>
</div>

# 📝 Publications
<div class="paper-note">⚓️ denotes project leader; 📧 denotes corresponding author.</div>

<div id="publications-wrapper">
<div id="filter-container"></div>

<h1 style="font-size: 1.25em; font-weight: bold; margin-top: 35px; margin-bottom: 15px; border-bottom: 1px solid #eaecef; padding-bottom: 5px;">📝 Selected Publications</h1>


<div id='paper-combiner' class='paper-box floating-card' data-tags="TIP 2026, First Author, CCF A, Multimodal Understanding"><div class='paper-box-image'><div><div class="badge">TIP 2026</div><img src='images/COMBINER-TIP26.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">
  
**COMBINER: Composed Image Retrieval Guided by Attribute-based Neighbor Relations** [[Paper]](https://arxiv.org/abs/2606.04604) [[Project]](https://lee-zixu.github.io/COMBINER.github.io/) [[Code]](https://github.com/Lee-zixu/COMBINER) [[Official Version]](https://ieeexplore.ieee.org/abstract/document/11534406)

[***Zixu Li***](https://lee-zixu.github.io), [Yupeng Hu](https://faculty.sdu.edu.cn/huyupeng1/zh_CN/index.htm)✉, [Zhiwei Chen](https://zivchen-ty.github.io/), [Haokun Wen](https://haokunwen.github.io/), [Xuemeng Song](https://xuemengsong.github.io/), [Liqiang Nie](https://liqiangnie.github.io/index.html)



</div>
</div>


<div id='paper-tema' class='paper-box floating-card' data-tags="ACL 2026, First Author, CCF A, Multimodal Understanding"><div class='paper-box-image'><div><div class="badge">ACL 2026</div><img src='images/TEMA-ACL26.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**TEMA: Anchor the Image, Follow the Text for Multi-Modification Composed Image Retrieval** [[Paper]](https://arxiv.org/abs/2604.21806) [[Project]](https://lee-zixu.github.io/TEMA.github.io/) [[Code]](https://github.com/Lee-zixu/ACL26-TEMA)

[***Zixu Li***](https://lee-zixu.github.io), [Yupeng Hu](https://faculty.sdu.edu.cn/huyupeng1/zh_CN/index.htm)✉, [Zhiheng Fu](https://zhihfu.github.io), [Zhiwei Chen](https://zivchen-ty.github.io/), [Yongqi Li](https://liyongqi67.github.io/), [Liqiang Nie](https://liqiangnie.github.io/index.html)


 
</div>
</div>


<div id='paper-conesep' class='paper-box floating-card' data-tags="CVPR 2026, First Author, CCF A, Multimodal Understanding, Robustness"><div class='paper-box-image'><div><div class="badge">CVPR 2026</div><img src='images/ConeSep-CVPR26.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**ConeSep: Cone-based Robust Noise-Unlearning Compositional Network for Composed Image Retrieval** [[Paper]](https://arxiv.org/abs/2604.20358) [[Project]](https://lee-zixu.github.io/ConeSep.github.io/) [[Code]](https://github.com/Lee-zixu/ConeSep) [[Official Version]](https://openaccess.thecvf.com/content/CVPR2026/html/Li_ConeSep_Cone-based_Robust_Noise-Unlearning_Compositional_Network_for_Composed_Image_Retrieval_CVPR_2026_paper.html)

[***Zixu Li***](https://lee-zixu.github.io), [Yupeng Hu](https://faculty.sdu.edu.cn/huyupeng1/zh_CN/index.htm)✉, [Zhiwei Chen](https://zivchen-ty.github.io/), [Mingyu Zhang](https://zh-mingyu.github.io/), [Zhiheng Fu](https://zhihfu.github.io), [Liqiang Nie](https://liqiangnie.github.io/index.html)

</div>
</div>


<div id='paper-airknow' class='paper-box floating-card' data-tags="CVPR 2026, Project Leader, Core Contributor, CCF A, Multimodal Understanding, Robustness"><div class='paper-box-image'><div><div class="badge">CVPR 2026</div><img src='images/AirKnow-CVPR26.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**Air-Know: Arbiter-Calibrated Knowledge-Internalizing Robust Network for Composed Image Retrieval** [[Paper]](http://arxiv.org/abs/2604.19386) [[Project]](https://zhihfu.github.io/Air-Know.github.io/) [[Code]](https://github.com/ZhihFu/Air-Know) [[Official Version]](https://openaccess.thecvf.com/content/CVPR2026/html/Fu_Air-Know_Arbiter-Calibrated_Knowledge-Internalizing_Robust_Network_for_Composed_Image_Retrieval_CVPR_2026_paper.html)
<span style="color: #0366d6; font-weight: bold; display: block; margin-top: 5px; font-size: 0.95em;">First-authored by undergraduate student</span>

[Zhiheng Fu](https://zhihfu.github.io), [Yupeng Hu](https://faculty.sdu.edu.cn/huyupeng1/zh_CN/index.htm)✉, Qianyun Yang, Shiqi Zhang, [Zhiwei Chen](https://zivchen-ty.github.io/), [***Zixu Li***](https://lee-zixu.github.io)†


 
</div>
</div> 



<div id='paper-retrack' class='paper-box floating-card' data-tags="AAAI 2026, First Author, CCF A, Multimodal Understanding"><div class='paper-box-image'><div><div class="badge">AAAI 2026</div><img src='images/2026-ReTrack-AAAI26.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">
  
**ReTrack: Evidence-Driven Dual-Stream Directional Anchor Calibration Network for Composed Video Retrieval** [[Paper]](http://arxiv.org/abs/2604.17898) [[Project]](https://lee-zixu.github.io/ReTrack.github.io/) [[Code]](https://github.com/Lee-zixu/ReTrack) [[Official Version]](https://ojs.aaai.org/index.php/AAAI/article/view/39507) 

[***Zixu Li***](https://lee-zixu.github.io), [Yupeng Hu](https://faculty.sdu.edu.cn/huyupeng1/zh_CN/index.htm)✉, [Zhiwei Chen](https://zivchen-ty.github.io/), [Qinlei Huang](https://windlikeo.github.io/HQL.github.io/), Guozhi Qiu, [Zhiheng Fu](https://zhihfu.github.io), [Meng Liu](https://mengliu1991.github.io)


 
</div>
</div>


<div id='paper-habit' class='paper-box floating-card' data-tags="AAAI 2026, First Author, CCF A, Multimodal Understanding, Robustness"><div class='paper-box-image'><div><div class="badge">AAAI 2026</div><img src='images/2026-HABIT-AAAI26.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">
  
**HABIT: Chrono-Synergia Robust Progressive Learning Framework for Composed Image Retrieval** [[Paper]](https://arxiv.org/abs/2604.18037) [[Project]](https://lee-zixu.github.io/HABIT.github.io/) [[Code]](https://github.com/Lee-zixu/HABIT) [[Official Version]](https://ojs.aaai.org/index.php/AAAI/article/view/37608) 

[***Zixu Li***](https://lee-zixu.github.io), [Yupeng Hu](https://faculty.sdu.edu.cn/huyupeng1/zh_CN/index.htm)✉, [Zhiwei Chen](https://zivchen-ty.github.io/), Shiqi Zhang, [Qinlei Huang](https://windlikeo.github.io/HQL.github.io/), [Zhiheng Fu](https://zhihfu.github.io), [Yinwei Wei](https://weiyinwei.github.io)


 
</div>
</div>


<div id='paper-encoder' class='paper-box floating-card' data-tags="AAAI 2025, First Author, CCF A, Multimodal Understanding"><div class='paper-box-image'><div><div class="badge">AAAI 2025</div><img src='images/ENCODER-AAAI25.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**ENCODER: Entity Mining and Modification Relation Binding for Composed Image Retrieval** [[Paper]](https://ojs.aaai.org/index.php/AAAI/article/view/32541) [[Project]](https://sdu-l.github.io/ENCODER.github.io/) [[Code]](https://github.com/Lee-zixu/ENCODER) [[Official Version]](https://ojs.aaai.org/index.php/AAAI/article/view/32541)

[***Zixu Li***](https://lee-zixu.github.io), [Zhiwei Chen](https://zivchen-ty.github.io/), [Haokun Wen](https://haokunwen.github.io/), [Zhiheng Fu](https://zhihfu.github.io), [Yupeng Hu](https://faculty.sdu.edu.cn/huyupeng1/zh_CN/index.htm)✉, [Weili Guan](https://faculty.hitsz.edu.cn/guanweili)


 
</div>
</div>


<div id='paper-finecir' class='paper-box floating-card' data-tags="Preprint, First Author, Multimodal Understanding"><div class='paper-box-image'><div><div class="badge">Arxiv 2025</div><img src='/images/FineCIR.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**FineCIR: Explicit Parsing of Fine-Grained Modification Semantics for Composed Image Retrieval** [[Paper]](https://arxiv.org/abs/2503.21309) [[Project]](https://sdu-l.github.io/FineCIR.github.io/)  [[Code]](https://github.com/SDU-L/FineCIR) 

[***Zixu Li***](https://lee-zixu.github.io),  [Zhiheng Fu](https://zhihfu.github.io),  [Yupeng Hu](https://faculty.sdu.edu.cn/huyupeng1/zh_CN/index.htm)✉,  [Zhiwei Chen](https://zivchen-ty.github.io/),  [Haokun Wen](https://haokunwen.github.io/),  [Liqiang Nie](https://liqiangnie.github.io/index.html)
 
</div>
</div>



<h1 style="font-size: 1.25em; font-weight: bold; margin-top: 45px; margin-bottom: 15px; border-bottom: 1px solid #eaecef; padding-bottom: 5px;">📝 More Publications</h1>


<div id='paper-stable' class='paper-box floating-card' data-tags="TKDE 2026, Core Contributor, CCF A, Efficiency"><div class='paper-box-image'><div><div class="badge">TKDE 2026</div><img src='/images/STABLE-TKDE26.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">
**STABLE: Efficient Hybrid Nearest Neighbor Search via Magnitude-Uniformity and Cardinality-Robustness** [[Paper]](https://www.computer.org/csdl/journal/tk/5555/01/11450508/2f5S8Le2iZ2)

Qianyun Yang, [Zhiwei Chen](https://zivchen-ty.github.io/), [Yupeng Hu](https://faculty.sdu.edu.cn/huyupeng1/zh_CN/index.htm), [***Zixu Li***](https://lee-zixu.github.io),  [Zhiheng Fu](https://zhihfu.github.io), [Liqiang Nie](https://liqiangnie.github.io/index.html)


 
</div>
</div>


<div id='paper-refine' class='paper-box floating-card' data-tags="ACM ToMM 2026, Core Contributor, CCF B"><div class='paper-box-image'><div><div class="badge">ACM ToMM 2026</div><img src='/images/REFINE-ToMM26.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">
**REFINE: Composed Video Retrieval via Shared and Differential Semantics Enhancement** [[Paper]](https://dl.acm.org/doi/10.1145/3796712) [[Project]](https://sdu-l.github.io/REFINE.github.io/) [[Code]](https://github.com/iLearn-Lab/TOMM26-REFINE) [[Official Version]](https://dl.acm.org/doi/10.1145/3796712) 

[Yupeng Hu](https://faculty.sdu.edu.cn/huyupeng1/zh_CN/index.htm), [***Zixu Li***](https://lee-zixu.github.io), [Zhiwei Chen](https://zivchen-ty.github.io/), [Qinlei Huang](https://windlikeo.github.io/HQL.github.io/), [Zhiheng Fu](https://zhihfu.github.io), [Mingzhu Xu](https://faculty.sdu.edu.cn/xumingzhu/zh_CN/)✉, [Liqiang Nie](https://liqiangnie.github.io/index.html)


 
</div>
</div> 


<div id='paper-intent' class='paper-box floating-card' data-tags="AAAI 2026, Project Leader, Core Contributor, CCF A, Multimodal Understanding, Robustness"><div class='paper-box-image'><div><div class="badge">AAAI 2026</div><img src='images/2026-INTENT-AAAI26.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**INTENT: Invariance and Discrimination-aware Noise Mitigation for Robust Composed Image Retrieval** [[Paper]](https://arxiv.org/abs/2604.18051) [[Project]](https://zivchen-ty.github.io/INTENT.github.io/) [[Code]](https://github.com/ZivChen-Ty/INTENT) [[Official Version]](https://ojs.aaai.org/index.php/AAAI/article/view/39181) 

[Zhiwei Chen](https://zivchen-ty.github.io/), [Yupeng Hu](https://faculty.sdu.edu.cn/huyupeng1/zh_CN/index.htm)✉, [Zhiheng Fu](https://zhihfu.github.io), [***Zixu Li***](https://lee-zixu.github.io)†, [Jiale Huang](https://arcadiadream.github.io/HJL.github.io/), [Qinlei Huang](https://windlikeo.github.io/HQL.github.io/), [Yinwei Wei](https://weiyinwei.github.io)

 
</div>
</div>


<div id='paper-offset' class='paper-box floating-card' data-tags="ACM MM 2025, Project Leader, Core Contributor, CCF A, Multimodal Understanding"><div class='paper-box-image'><div><div class="badge">ACM MM 2025</div><img src='/images/OFFSET-MM25.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**OFFSET: Segmentation-based Focus Shift Revision for Composed Image Retrieval** [[Paper]](https://arxiv.org/abs/2507.05631) [[Project]](https://zivchen-ty.github.io/OFFSET.github.io/) [[Code]](https://github.com/ZivChen-Ty/OFFSET) [[Official Version]](https://dl.acm.org/doi/10.1145/3746027.3755366) 

[Zhiwei Chen](https://zivchen-ty.github.io/), [Yupeng Hu](https://faculty.sdu.edu.cn/huyupeng1/zh_CN/index.htm)✉, [***Zixu Li***](https://lee-zixu.github.io)†,  [Zhiheng Fu](https://zhihfu.github.io),  [Xuemeng Song](https://xuemengsong.github.io/), [Liqiang Nie](https://liqiangnie.github.io/index.html)


 
</div>
</div>


<div id='paper-hud' class='paper-box floating-card' data-tags="ACM MM 2025, Project Leader, Core Contributor, CCF A, Multimodal Understanding"><div class='paper-box-image'><div><div class="badge">ACM MM 2025</div><img src='/images/HUD-MM25.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">
  
**HUD: Hierarchical Uncertainty-Aware Disambiguation Network for Composed Video Retrieval** [[Paper]](https://arxiv.org/abs/2512.02792) [[Project]](https://zivchen-ty.github.io/HUD.github.io/) [[Code]](https://github.com/ZivChen-Ty/HUD) [[Official Version]](https://dl.acm.org/doi/10.1145/3746027.3755445) 
 

[Zhiwei Chen](https://zivchen-ty.github.io/), [Yupeng Hu](https://faculty.sdu.edu.cn/huyupeng1/zh_CN/index.htm)✉, [***Zixu Li***](https://lee-zixu.github.io)†, [Zhiheng Fu](https://zhihfu.github.io),  [Haokun Wen](https://haokunwen.github.io/), [Weili Guan](https://faculty.hitsz.edu.cn/guanweili)


</div>
</div>


<h1 style="font-size: 1.25em; font-weight: bold; margin-top: 45px; margin-bottom: 15px; border-bottom: 1px solid #eaecef; padding-bottom: 5px;">📝 Challenge Technical Report</h1>


<div id='paper-r3' class='paper-box floating-card' data-tags="CVPRW 2026, First Author, Challenge 1st🏅, Challenge, Multimodal Understanding"><div class='paper-box-image'><div><div class="badge">CVPR 2026 Challenge 1st🏅</div><img src='images/R3-CVPRW26.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1"> 

**R<sup>3</sup>: Composed Video Retrieval via Reasoning-Guided Recalling and Re-ranking** [[Technical Report]](https://arxiv.org/abs/2606.01113)

[***Zixu Li***](https://lee-zixu.github.io), [Yupeng Hu](https://faculty.sdu.edu.cn/huyupeng1/zh_CN/index.htm)✉, [Zhiheng Fu](https://zhihfu.github.io),  [Zhiwei Chen](https://zivchen-ty.github.io/), [Weili Guan](https://faculty.hitsz.edu.cn/guanweili), [Liqiang Nie](https://liqiangnie.github.io/index.html)

</div>
</div>


<div id='paper-temp-ret' class='paper-box floating-card' data-tags="CVPRW 2026, First Author, Challenge 1st🏅, Challenge, Egocentric Vision Reasoning"><div class='paper-box-image'><div><div class="badge">CVPR 2026 Challenge 1st🏅</div><img src='images/TempRet-CVPRW26.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1"> 

**TempRet: Temporal Enhancement and Two-Stage Reranking for CVPR 2026 EPIC-KITCHENS-100 Multi-Instance Retrieval Challenge** [[Technical Report]](https://arxiv.org/abs/2605.24470)

[***Zixu Li***](https://lee-zixu.github.io), [Yupeng Hu](https://faculty.sdu.edu.cn/huyupeng1/zh_CN/index.htm)✉, [Zhiwei Chen](https://zivchen-ty.github.io/), [Zhiheng Fu](https://zhihfu.github.io),  Xiaowei Zhu, [Weili Guan](https://faculty.hitsz.edu.cn/guanweili), [Liqiang Nie](https://liqiangnie.github.io/index.html)

</div>
</div>


<div id='paper-egoadapt' class='paper-box floating-card' data-tags="CVPRW 2026, Project Leader, Core Contributor, Challenge 1st🏅, Challenge, Egocentric Vision Reasoning"><div class='paper-box-image'><div><div class="badge">CVPR 2026 Challenge 1st🏅</div><img src='images/EgoAdapt-CVPRW26.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1"> 

**EgoAdapt: A Multi-Scene Egocentric Adaptation Method for CVPR 2026 HD-EPIC VQA Challenge** [[Technical Report]](https://arxiv.org/abs/2605.24500)

[Zhiwei Chen](https://zivchen-ty.github.io/), [Yupeng Hu](https://faculty.sdu.edu.cn/huyupeng1/zh_CN/index.htm)✉, [***Zixu Li***](https://lee-zixu.github.io)†, [Zhiheng Fu](https://zhihfu.github.io),  Guozhi Qiu, [Weili Guan](https://faculty.hitsz.edu.cn/guanweili), [Liqiang Nie](https://liqiangnie.github.io/index.html)

</div>
</div>


<div id='paper-omniego' class='paper-box floating-card' data-tags="CVPRW 2026, First Author, Challenge 2nd🥈, Challenge, Egocentric Vision Reasoning"><div class='paper-box-image'><div><div class="badge">CVPR 2026 Challenge 2nd🥈</div><img src='images/OmniEgo-R2-CVPRW26.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1"> 

**OmniEgo-R<sup>2</sup>: A Routed Reasoning Framework for the 1st Cross-Domain EgoCross Challenge at CVPR 2026** [[Technical Report]](https://arxiv.org/abs/2605.24481)

[***Zixu Li***](https://lee-zixu.github.io), [Zhiwei Chen](https://zivchen-ty.github.io/), [Zhiheng Fu](https://zhihfu.github.io),  Wenbo Wang, [Yupeng Hu](https://faculty.sdu.edu.cn/huyupeng1/zh_CN/index.htm)✉, [Weili Guan](https://faculty.hitsz.edu.cn/guanweili), [Liqiang Nie](https://liqiangnie.github.io/index.html)

</div>  
</div>


<div id='paper-egoaction' class='paper-box floating-card' data-tags="CVPRW 2026, Project Leader, Core Contributor, Challenge 3rd🥉, Challenge, Egocentric Vision Reasoning"><div class='paper-box-image'><div><div class="badge">CVPR 2026 Challenge 3rd🥉</div><img src='images/EgoAction-CVPRW26.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1"> 

**EgoAction: Egocentric Action Composition with Reliability-Aware Temporal Fusion for the EPIC-KITCHENS Action Detection Challenge at CVPR 2026** [[Technical Report]](https://arxiv.org/abs/2605.24496)

[Zhiheng Fu](https://zhihfu.github.io),  [***Zixu Li***](https://lee-zixu.github.io)†, [Zhiwei Chen](https://zivchen-ty.github.io/), Fangxu Liu, [Yupeng Hu](https://faculty.sdu.edu.cn/huyupeng1/zh_CN/index.htm)✉, [Weili Guan](https://faculty.hitsz.edu.cn/guanweili), [Liqiang Nie](https://liqiangnie.github.io/index.html)

</div>
</div>



<h1 style="font-size: 1.25em; font-weight: bold; margin-top: 45px; margin-bottom: 15px; border-bottom: 1px solid #eaecef; padding-bottom: 5px;"><span class="i18n-en-inline">🏭 Industry Project</span><span class="i18n-zh-inline">🏭 产业项目</span></h1>


<div class='paper-box floating-card industry-card' data-tags="Huawei, Industry Project, ANN, Vector Database, Efficiency"><div class='paper-box-image'><div><div class="badge">Huawei Cloud VectorDB</div><img src='images/huawei.png' alt="Huawei CSS VectorDB performance" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

<div class="industry-project-title i18n-en"><strong>Huawei Approximate Nearest Neighbor Search Collaboration Project</strong> <a class="paper-link-btn" href="https://www.huaweicloud.com/product/css/vectordb.html" target="_blank">Product Page</a></div>
<div class="industry-project-title i18n-zh"><strong>华为通用向量检索合作项目</strong> <a class="paper-link-btn" href="https://www.huaweicloud.com/product/css/vectordb.html" target="_blank">产品页面</a></div>

<div class="award-ribbon">
  <span class="i18n-en-flex">🏆 Huawei Outstanding Technical Collaboration Award · Top 10 globally / year</span>
  <span class="i18n-en-flex">🌟 Huawei Outstanding Student Award · Top 30 globally / year</span>
  <span class="i18n-zh-flex">🏆 华为优秀技术合作成果奖 · 全球每年 Top 10</span>
  <span class="i18n-zh-flex">🌟 华为优秀学生奖 · 全球每年 Top 30</span>
</div>

<p class="i18n-en"><em>Student Lead, 2022–2026.</em> I led the algorithmic design and iterative optimization of <span class="highlight-red">QSGNGT</span>, a graph-indexing method for large-scale approximate nearest neighbor (ANN) search. The project targeted <span class="highlight-blue">high-throughput, high-recall vector retrieval</span> under industrial-scale deployment constraints, and was jointly developed with Huawei for cloud-native vector database scenarios.</p>
<p class="i18n-zh"><em>学生负责人，2022–2026。</em> 我主导了 <span class="highlight-red">QSGNGT</span> 算法的设计与迭代优化，该方法面向大规模近似最近邻（ANN）检索构建高效图索引。在工业级部署约束下，项目聚焦于 <span class="highlight-blue">高吞吐、高召回的向量检索</span>，并与华为联合推进云原生向量数据库场景落地。</p>

<!-- <div class="huawei-highlights">
  <span><b>SOTA performance:</b> ranked <span class="highlight-red">1st in QPS</span> under fixed Recall on six million-scale ANN-Benchmarks datasets.</span>
  <span><b>Continuous optimization:</b> improved peak performance by over <span class="highlight-red">164%</span> on Euclidean-distance datasets and <span class="highlight-red">116%</span> on angular-distance datasets.</span>
  <span><b>Industrial deployment:</b> integrated into <span class="highlight-blue">Huawei Cloud GaussDB / CSS VectorDB</span> for cloud-native, hundred-billion-scale vector retrieval.</span>
  <span><b>System impact:</b> supported <span class="highlight-red">10×</span> retrieval-scale growth, <span class="highlight-red">sub-10ms</span> latency, and <span class="highlight-red">2×</span> faster response.</span>
</div> -->

<div class="benchmark-orgs">
  <div class="benchmark-orgs-title"><span class="i18n-en-inline">Representative ANN-Benchmarks participants / baselines</span><span class="i18n-zh-inline">ANN-Benchmarks 代表参与企业 / 基线算法</span></div>
  <div class="org-logo-strip">
    <span class="org-logo-card"><img src="images/company-logos/google.svg" alt="Google">Google</span>
    <span class="org-logo-card"><img src="images/company-logos/microsoft.svg" alt="Microsoft">Microsoft</span>
    <span class="org-logo-card"><img src="images/company-logos/meta.svg" alt="Meta">Meta</span>
    <span class="org-logo-card"><img src="images/company-logos/yahoo.svg" alt="Yahoo">Yahoo</span>
    <span class="org-logo-card"><img src="images/company-logos/jd.svg" alt="JD.com">JD.com</span>
    <span class="org-logo-card"><img src="images/company-logos/alibaba.svg" alt="Alibaba">Alibaba</span>
    <span class="org-logo-card"><img src="images/company-logos/01ai.ico" alt="01.AI">01.AI</span>
  </div>
</div>

</div>
</div>


<script>
document.addEventListener('DOMContentLoaded', function() {
  const roadmap = document.getElementById('research-map');
  const backToRoadmapBtn = document.getElementById('roadmap-back-btn');

  if (roadmap && backToRoadmapBtn) {
    const roadmapLinks = document.querySelectorAll('.node-paper-link[href^="#paper-"]');

    roadmapLinks.forEach(link => {
      link.addEventListener('click', () => {
        backToRoadmapBtn.classList.add('show');
      });
    });

    backToRoadmapBtn.addEventListener('click', () => {
      backToRoadmapBtn.classList.remove('show');
    });
  }

  const languageSwitcher = document.getElementById('research-language-switcher');
  if (languageSwitcher) {
    const tabs = languageSwitcher.querySelectorAll('.lang-tab');
    const panels = languageSwitcher.querySelectorAll('.lang-panel');
    const setLanguage = (lang) => {
      document.body.classList.toggle('lang-en', lang === 'en');
      document.body.classList.toggle('lang-zh', lang === 'zh');
      document.documentElement.setAttribute('lang', lang === 'zh' ? 'zh-CN' : 'en');
      tabs.forEach(tab => {
        const active = tab.dataset.lang === lang;
        tab.classList.toggle('active', active);
        tab.setAttribute('aria-selected', active ? 'true' : 'false');
      });
      panels.forEach(panel => {
        panel.classList.toggle('active', panel.dataset.langPanel === lang);
      });
    };
    setLanguage(languageSwitcher.querySelector('.lang-tab.active')?.dataset.lang || 'en');
    tabs.forEach(tab => {
      tab.addEventListener('mouseenter', () => setLanguage(tab.dataset.lang));
      tab.addEventListener('click', () => setLanguage(tab.dataset.lang));
      tab.addEventListener('focus', () => setLanguage(tab.dataset.lang));
    });
  }

  const wrapper = document.getElementById('publications-wrapper');
  if (!wrapper) return;

  const filterContainer = document.getElementById('filter-container');

  const allElements = Array.from(wrapper.children).filter(el => el.id !== 'filter-container');
  const paperBoxes = allElements.filter(el => el.classList.contains('paper-box'));

  allElements.forEach((el, index) => {
    el.dataset.originalOrder = String(index);
  });

  const linkLikeTags = new Set(['Paper', 'PDF', 'Project', 'Project Page', 'Code', 'Blog', 'Website', 'Technical Report']);
  const venueFilterExcludeTags = new Set(['ACL 2026', 'CVPR 2026', 'AAAI 2026', 'ACM MM 2025', 'AAAI 2025', 'Arxiv 2025', 'ICASSP 2025', 'ICASSP 2026', 'TKDE 2026', 'TIP 2026', 'ACM ToMM 2026', 'CVPRW 2026', 'CCF B', 'Challenge 1st🏅', 'Challenge 2nd🥈', 'Challenge 3rd🥉', 'Huawei', 'ANN', 'Vector Database']);
  const venueFullNames = {
   'ACL 2026': 'The 64th Annual Meeting of the Association for Computational Linguistics (ACL 2026)',
    'CVPR 2026': 'IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR 2026)',
    'AAAI 2026': 'The 40th Annual AAAI Conference on Artificial Intelligence (AAAI 2026)',
    'ACM MM 2025': 'ACM International Conference on Multimedia (ACM MM 2025)',
    'AAAI 2025': 'The 39th Annual AAAI Conference on Artificial Intelligence (AAAI 2025)',
    'Arxiv 2025': 'arXiv preprint (2025)',
    'TKDE 2026': 'IEEE Transactions on Knowledge and Data Engineering (TKDE 2026)',
    'TIP 2026': 'IEEE Transactions on Image Processing (TIP 2026)',
    'ACM ToMM 2026': 'ACM Transactions on Multimedia Computing, Communications, and Applications (ACM ToMM 2026)',
    'CVPRW 2026': 'IEEE/CVF Conference on Computer Vision and Pattern Recognition Workshop (CVPRW 2026)'
  };
  let tagCounts = {};
  let activeTags = new Set();

  paperBoxes.forEach(box => {
    const tagsAttribute = box.getAttribute('data-tags');
    if (!tagsAttribute) return;
    const tagsList = tagsAttribute.split(',').map(t => t.trim()).filter(t => t);

    const textContainer = box.querySelector('.paper-box-text');
    const linksContainer = box.querySelector('.links');
    if (textContainer && !textContainer.querySelector('.badge-container')) {
      const badgeContainer = document.createElement('div');
      badgeContainer.className = 'badge-container';
      tagsList.filter(tag => !linkLikeTags.has(tag)).forEach(tag => {
        const badge = document.createElement('span');
        badge.className = 'inner-tag-badge';
        badge.textContent = tag;
        badgeContainer.appendChild(badge);
      });

      const paragraphs = textContainer.querySelectorAll('p');
      if (paragraphs.length >= 2) {
        paragraphs[1].insertAdjacentElement('afterend', badgeContainer);
      } else if (linksContainer) {
        textContainer.insertBefore(badgeContainer, linksContainer);
      } else {
        textContainer.appendChild(badgeContainer);
      }
    }

    tagsList.filter(tag => !linkLikeTags.has(tag) && !venueFilterExcludeTags.has(tag)).forEach(tag => tagCounts[tag] = (tagCounts[tag] || 0) + 1);
  });

  textContainerLinkButtons();
  enrichPaperCards();

  const tagOrder = [
      'First Author',
      'Project Leader',
      'Core Contributor',
      'CCF A',
      'Preprint',
      'Challenge',
      'Egocentric Vision Reasoning',
      'Multimodal Understanding',
      'Robustness',
      'Efficiency'
    ];
    
    const sortedTags = Object.keys(tagCounts).sort((a, b) => {
      const ia = tagOrder.indexOf(a);
      const ib = tagOrder.indexOf(b);
    
      if (ia !== -1 && ib !== -1) return ia - ib;
      if (ia !== -1) return -1;
      if (ib !== -1) return 1;
      return a.localeCompare(b);
    });
  
  if (filterContainer) {
    filterContainer.innerHTML = '';
    sortedTags.forEach(tag => {
      const btn = document.createElement('button');
      btn.className = 'filter-btn';
      btn.textContent = `${tag} (${tagCounts[tag]})`;
      btn.onclick = () => {
        if (activeTags.has(tag)) {
          activeTags.delete(tag);
          btn.classList.remove('active');
        } else {
          activeTags.add(tag);
          btn.classList.add('active');
        }
        filterPapers();
      };
      filterContainer.appendChild(btn);
    });
  }

  function textContainerLinkButtons() {
    paperBoxes.forEach(box => {
      const textContainer = box.querySelector('.paper-box-text');
      if (!textContainer || textContainer.querySelector('.paper-link-container')) return;
      const firstParagraph = textContainer.querySelector('p');
      if (!firstParagraph) return;

      const linkContainer = document.createElement('div');
      linkContainer.className = 'paper-link-container';
      firstParagraph.querySelectorAll('a').forEach(link => {
        link.classList.add('paper-link-btn');
        linkContainer.appendChild(link);
      });

      if (linkContainer.children.length > 0) {
        const badgeContainer = textContainer.querySelector('.badge-container');
        if (badgeContainer) {
          badgeContainer.insertAdjacentElement('afterend', linkContainer);
        } else {
          firstParagraph.insertAdjacentElement('afterend', linkContainer);
        }
      }
    });
  }

  function enrichPaperCards() {
    paperBoxes.forEach(box => {
      const textContainer = box.querySelector('.paper-box-text');
      if (!textContainer) return;
      const paragraphs = textContainer.querySelectorAll('p');
      const titleParagraph = paragraphs[0];
      const authorParagraph = paragraphs[1];
      if (!titleParagraph || !authorParagraph) return;

      const badgeText = (box.querySelector('.badge')?.textContent || '').trim();
      const venueKey = Object.keys(venueFullNames).find(key => badgeText.includes(key));
      if (venueKey && !textContainer.querySelector('.venue-full-name')) {
        const venue = document.createElement('div');
        venue.className = 'venue-full-name';
        venue.textContent = venueFullNames[venueKey];
        titleParagraph.insertAdjacentElement('afterend', venue);
      }

      authorParagraph.classList.add('paper-authors');
      authorParagraph.innerHTML = authorParagraph.innerHTML
        .replace(/\[\*\*\*Zixu Li\*\*\*\]\(([^)]+)\)/g, '<a href="$1" class="primary-gradient-text author-self">Zixu Li</a>')
        .replace(/\[\*\*\*Zixu Li\*\*\*\]\(([^)]+)\)/g, '<a href="$1" class="primary-gradient-text author-self">Zixu Li</a>')
        .replace(/\[\*\*\*Zixu Li\*\*\*\]\(([^)]+)\)/g, '<a href="$1" class="primary-gradient-text author-self">Zixu Li</a>')
        .replace(/\[\*\*\*Zixu Li\*\*\*\]/g, '<span class="primary-gradient-text author-self">Zixu Li</span>')
        .replace(/\*\*\*Zixu Li\*\*\*/g, '<span class="primary-gradient-text author-self">Zixu Li</span>')
        .replace(/Zixu Li/g, '<span class="primary-gradient-text author-self">Zixu Li</span>')
        .replace(/\*/g, '<span class="author-star" title="First author">⭐</span>')
        .replace(/†/g, '<span class="author-anchor" title="Project leader">⚓️</span>')
        .replace(/✉/g, '<span class="author-mail" title="Corresponding author">📧</span>');
    });
  }

  function filterPapers() {
    paperBoxes.forEach(box => {
      const boxTagsString = box.getAttribute('data-tags');
      const boxTags = boxTagsString ? boxTagsString.split(',').map(t => t.trim()) : [];
      const isMatched = activeTags.size === 0 || Array.from(activeTags).every(activeTag => boxTags.includes(activeTag));

      box.style.opacity = activeTags.size > 0 && !isMatched ? '0.25' : '1';

      box.querySelectorAll('.inner-tag-badge').forEach(badge => {
        badge.classList.toggle('active', activeTags.has(badge.textContent));
      });
    });

    if (activeTags.size > 0) {
      const sortedElements = [...allElements].sort((a, b) => {
        const aIsBox = a.classList.contains('paper-box');
        const bIsBox = b.classList.contains('paper-box');
        
        let aScore = 1;
        if (aIsBox) {
          const aTags = (a.getAttribute('data-tags') || '').split(',').map(t => t.trim());
          const aMatched = Array.from(activeTags).every(tag => aTags.includes(tag));
          aScore = aMatched ? 0 : 2;
        }

        let bScore = 1;
        if (bIsBox) {
          const bTags = (b.getAttribute('data-tags') || '').split(',').map(t => t.trim());
          const bMatched = Array.from(activeTags).every(tag => bTags.includes(tag));
          bScore = bMatched ? 0 : 2;
        }

        if (aScore !== bScore) {
          return aScore - bScore;
        }
        
        return Number(a.dataset.originalOrder) - Number(b.dataset.originalOrder);
      });
      
      sortedElements.forEach(el => wrapper.appendChild(el));
    } else {
      allElements
        .sort((a, b) => Number(a.dataset.originalOrder) - Number(b.dataset.originalOrder))
        .forEach(el => wrapper.appendChild(el));
    }
  }
});
</script>

</div>



<h1><span class="i18n-en-inline">🔖 Patent</span><span class="i18n-zh-inline">🔖 专利</span></h1>
<!-- - [国家发明专利授权, 第二发明人] 基于实体挖掘和修改关系绑定的组合图像检索方法及系统 - 授权专利号: *ZL202411903224.3*-->

<ul class="i18n-en">
  <li>[Under substantive examination, second inventor] Data processing method, electronic device, readable storage medium and program product - Application No.: <em>CN202410533951.9</em></li>
</ul>
<ul class="i18n-zh">
  <li>[国家发明专利实审，第二发明人] 数据处理方法、电子设备、可读存储介质和程序产品 - 申请号：<em>CN202410533951.9</em></li>
</ul>
  
<!-- - [国家发明专利实审, 第二发明人] 基于属性的邻域关系引导的组合图像检索方法及系统 - 申请号: *CN202511944904.4*

- [国家发明专利实审, 第二发明人] 基于共享和差异语义增强的组合视频检索方法及系统 - 申请号: *CN202511944910.X*

- [国家发明专利实审, 第二发明人] 基于互补性引导解耦的组合图像检索方法及系统 - 申请号: *CN202510142418.4*

- [国家发明专利实审, 第二发明人] 基于自适应中间粒度聚合网络的组合图像检索方法及系统 - 申请号: *CN202510274983.6*

- [国家发明专利实审, 第三发明人] 基于特征相似性和属性一致性协同约束的近似近邻混合检索的用户推荐方法及系统 - 申请号: *CN202311201790.5*

- [国家发明专利实审, 第三发明人] 一种基于分割焦点偏移修正的组合图像检索方法及系统 - 申请号: *CN202510143920.7*

- [国家发明专利实审, 第三发明人] 一种基于层次化不确定性感知消歧的组合视频检索方法及系统 - 申请号: *CN202511567477.2*

- [国家发明专利实审, 第四发明人] 面向开放域视觉语言多任务的自适应指代关系对齐的检索方法及系统 - 申请号: *CN202511944907.8*-->

<!-- - [发明授权, 第四发明人] 基于跨模态语义解析的图文检索方法及系统 - 授权专利号: *ZL202410326442.9*-->

<!-- - [发明授权, 第五发明人] 一种基于受挫随机游走和特征加权聚类的高校经济困难生识别方法及系统 - 授权专利号: *ZL202211425243.0*-->

<h1><span class="i18n-en-inline">🎖 Honors and Awards</span><span class="i18n-zh-inline">🎖 荣誉奖励</span></h1>
<ul class="i18n-en">
  <li><em>2026.06</em> Shandong University Graduate Academic Star Award (Practical Application Category, 18 people in the whole university).</li>
  <li><em>2025.10</em> <strong>Grand Prize (特等奖)</strong> in the CICAS Smart Power Scenario Competition.</li>
  <li><em>2024.09</em> Huawei Outstanding Technical Collaboration Award <strong>(Top 10 globally per year)</strong>.</li>
  <li><em>2024.09</em> Huawei Outstanding Student Award <strong>(Top 30 globally per year)</strong>.</li>
  <li><em>2023.06</em> Outstanding Undergraduate Thesis <strong>(Ranked 1st out of 409 candidates)</strong>.</li>
  <li><em>2023.06</em> Outstanding Graduates of Shandong Province.</li>
  <li><em>2023.06</em> Outstanding Graduates of Shandong University.</li>
</ul>
<ul class="i18n-zh">
  <li><em>2026.06</em> 山东大学研究生学术之星（实践应用类，全校18人）。</li>
  <li><em>2025.10</em> CICAS 智能电力场景竞赛<strong>特等奖</strong>。</li>
  <li><em>2024.09</em> 华为优秀技术合作成果奖<strong>（全球每年 Top 10）</strong>。</li>
  <li><em>2024.09</em> 华为优秀学生奖<strong>（全球每年 Top 30）</strong>。</li>
  <li><em>2023.06</em> 山东大学优秀本科毕业论文<strong>（409名候选人中排名第1）</strong>。</li>
  <li><em>2023.06</em> 山东省优秀毕业生。</li>
  <li><em>2023.06</em> 山东大学优秀毕业生。</li>
</ul>

<!--# 💻 Project QSGNGT-->

<h1><span class="i18n-en-inline">🏆 Competition</span><span class="i18n-zh-inline">🏆 竞赛获奖</span></h1>
<ul class="i18n-en">
  <li>1st place 🏅, CVPR VidLLMs Workshop, Reasoned-Aware Composed Video Retrieval Challenge, 2026.</li>
  <li>1st place 🏅, CVPR EgoVis Workshop, HD-EPIC Challenge, 2026. <a href="https://www.codabench.org/competitions/13645/#/results-tab">Link</a></li>
  <li>1st place 🏅, CVPR EgoVis Workshop, EPIC-KITCHENS Challenge-Multi-Instance Retrieval Track, 2026. <a href="https://www.codabench.org/competitions/12008/#/results-tab">Link</a></li>
  <li>2nd place 🥈, CVPR EgoVis Workshop, EgoCross Challenge-Source-Limited Track, 2026. <a href="https://www.codabench.org/competitions/11279/#/results-tab">Link</a></li>
  <li>2nd place 🥈, CVPR EgoVis Workshop, EgoCross Challenge-Open-Source Track, 2026. <a href="https://www.codabench.org/competitions/13868/#/results-tab">Link</a></li>
  <li>3rd place 🥉, CVPR EgoVis Workshop, EPIC-KITCHENS Challenge-Action Detection Track, 2026. <a href="https://www.codabench.org/competitions/13830/#/results-tab">Link</a></li>
</ul>
<ul class="i18n-zh">
  <li>冠军 🏅，CVPR VidLLMs Workshop，Reasoned-Aware Composed Video Retrieval Challenge，2026。</li>
  <li>冠军 🏅，CVPR EgoVis Workshop，HD-EPIC Challenge，2026。<a href="https://www.codabench.org/competitions/13645/#/results-tab">链接</a></li>
  <li>冠军 🏅，CVPR EgoVis Workshop，EPIC-KITCHENS Challenge-Multi-Instance Retrieval Track，2026。<a href="https://www.codabench.org/competitions/12008/#/results-tab">链接</a></li>
  <li>亚军 🥈，CVPR EgoVis Workshop，EgoCross Challenge-Source-Limited Track，2026。<a href="https://www.codabench.org/competitions/11279/#/results-tab">链接</a></li>
  <li>亚军 🥈，CVPR EgoVis Workshop，EgoCross Challenge-Open-Source Track，2026。<a href="https://www.codabench.org/competitions/13868/#/results-tab">链接</a></li>
  <li>季军 🥉，CVPR EgoVis Workshop，EPIC-KITCHENS Challenge-Action Detection Track，2026。<a href="https://www.codabench.org/competitions/13830/#/results-tab">链接</a></li>
</ul>

<h1><span class="i18n-en-inline">📖 Education</span><span class="i18n-zh-inline">📖 教育经历</span></h1>
<ul class="i18n-en">
  <li><em>2023.09 - now</em>, Shandong University, Artificial Intelligence, Ph.D.</li>
  <li><em>2019.09 - 2023.06</em>, Shandong University, Data Science and Big Data Technology, Bachelor's Degree.</li>
</ul>
<ul class="i18n-zh">
  <li><em>2023.09 - 至今</em>，山东大学，人工智能，博士研究生。</li>
  <li><em>2019.09 - 2023.06</em>，山东大学，数据科学与大数据技术，学士。</li>
</ul>

<h1><span class="i18n-en-inline">📃 Services</span><span class="i18n-zh-inline">📃 学术服务</span></h1>
<ul class="i18n-en">
  <li>Conference PC Member: CVPR, ECCV, ICLR, NeurIPS, AAAI, ACM MM, SIGIR, IJCAI, ICME, ICMR, ICASSP</li>
  <li>Journal Reviewer: IEEE TIP, IEEE TIFS, ACM ToMM</li>
</ul>
<ul class="i18n-zh">
  <li>会议 PC Member：CVPR, ECCV, ICLR, NeurIPS, AAAI, ACM MM, SIGIR, IJCAI, ICME, ICMR, ICASSP</li>
  <li>期刊审稿人：IEEE TIP, IEEE TIFS, ACM ToMM</li>
</ul>


<br>
<br>
<br>
<br>

<br>
<br>
<br>
<br>
















