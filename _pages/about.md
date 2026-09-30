---
layout: about
title: Home
permalink: /
subtitle: Postdoctoral Researcher · Peking University

profile:
  align: right
  image: Leader.jpg # 放在 assets/img/ 下。想换成圆形头像就把 image_circular 改 true
  image_circular: false # crops the image to make it circular
  more_info:

# news 和 publications 改由本页正文自己渲染（见文件末尾的 {% include news.liquid %}
# 和 {% bibliography --group_by none %}）。
#
# ↓ 这两个是「给 layout 用的开关」，不是「要不要显示」的开关。about.liquid 里有：
#     {% if page.announcements.enabled %}  → 渲染一份 news
#     {% if page.selected_papers %}        → 渲染一份 selected publications
#   所以要设成 false，否则页面上会出现**两份** —— 而 layout 那份的标题还硬编码指向
#   已经被删掉的 /publications/（会 404）。
#   正文里用 {% include %} / {% bibliography %} 直接调，绕过了这两个开关。
selected_papers: false
announcements:
  enabled: false
  # 下面两项是「活的」—— news.liquid 会读 page.announcements 的这两个值（正文调它时也读）：
  scrollable: true # news 超过 3 条时给区块加 max-height: 60vw（区块内滚动条）
  limit: 10 # 显示多少条；留空 = 全部。目前 _news/ 只有 3 条，所以暂时不起作用

# --- publications 区块的样式 ---
# 本人名字的高亮**主题自带，不需要自定义 CSS**。主题 main.css 里已有：
#   .publications ol.bibliography li .author > em { border-bottom: 1px solid; font-style: normal; }
# bib.liquid 把本人名字输出成 <em>，主题就用 border-bottom 画一条实线下划线。
# ⚠️ 不要再加 `text-decoration: underline` —— 两个属性各画一条，会叠成**两条线**（已踩过）。
# 想彻底不要下划线，就覆盖成 `.publications .author > em { border-bottom: none; }`。
# 另外：别在 papers.bib 里写 \textbf{} / \underline{}，LaTeX 命令不会被转换、会漏成纯文本，
# 而且会让主题认不出你（它靠 scholar.first_name / last_name 精确匹配）。

social: true # includes social icons at the bottom of the page

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

I am a postdoctoral researcher at the Institute of Remote Sensing and Geographic Information System at Peking University. My research asks how multimodal models can help us understand cities. I work across street-level panoramas and satellite imagery, and increasingly with the language people use to describe places, building models that reason across these views instead of treating them separately. I am drawn to multimodal large language models and agentic systems for geospatial intelligence — models that perceive cities more sharply, understand them more deeply, and hold up at scale across thousands of them.

At Peking University I work with [Fan Zhang](https://scholar.google.com/citations?user=dc1TzLoAAAAJ&hl=en) and [Yu Liu](https://scholar.google.com/citations?user=Xh_lRY4AAAAJ&hl=en). Before that, I completed my PhD at the Hong Kong University of Science and Technology, advised by [Fan Zhang](https://scholar.google.com/citations?user=dc1TzLoAAAAJ&hl=en) and [Mengqian Lu](https://scholar.google.com/citations?user=FE461eEAAAAJ&hl=en). I received my MPhil at LIESMARS, Wuhan University, supervised by [Zhenfeng Shao](https://scholar.google.com/citations?user=lsz8fJoAAAAJ&hl=en).

You can reach me at [yong.li@connect.ust.hk](mailto:yong.li@connect.ust.hk).

<h2><a href="{{ '/news/' | relative_url }}" style="color: inherit">news</a></h2>

{% include news.liquid limit=true %}

<h2>selected publications</h2>

<div class="publications">

{% bibliography --group_by none %}

</div>
