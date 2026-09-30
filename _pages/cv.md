---
layout: cv
permalink: /cv/
title: CV
# nav: false —— 只是不进顶部导航，页面**照样会构建**。之前 /cv/ 一直是能直接访问的，
# 内容还是模板里的 Albert Einstein 假数据。
# published: false（下面已生效，实测过）→ 页面**完全不构建**，/cv/ 返回 404。
# 想重新启用：删掉那行，或改成 published: true，同时把 _data/cv.yml 换成真内容。
published: false
nav: false
nav_order: 5
# 想要顶部导航出现 CV 链接：nav: true，并把 nav_order 排到合适位置
cv_pdf: # you can also use external links here
cv_format: rendercv # options: rendercv, jsonresume
description: This is a description of the page. You can modify it in '_pages/cv.md'. You can also change or remove the top pdf download button.
toc:
  sidebar: left
---
