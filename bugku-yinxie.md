---
layout:default
title:bugku 隐写
---
# bugku4 隐写
# 题目信息：
---
# bugku4 隐写
# 题目信息：
隐写；MISC(杂项）；提交BUGKU{XXX}
 # 初步踩坑
 1.下载后用记事本打开为乱码，用看图软件打开后发现为以Bugku主体的logo图片（PNG）
 2.查看图片属性：无有效信息
 3.使用Aperi'Solve在线分析：报错
 4.使用StegOnline:无法分析
 # 正确步骤
 1.将图片拖入hexed.it(十六进制编辑器）
 2.找到`IHDR`数据块，修改高度，使图片变为正方形，再另存为fix.png
 3.搜索在线PNG修复，上传图片修复后下载打开
 # Flag:
 BUGKU{a1e5aSA}
 # 原理：
 PNG图片头部（IHDR)中的宽度和高度决定图片渲染范围，作者将高度改小（使logo视觉中心上感觉下降），导致图片下半部分被裁剪隐藏，高度修复后即可恢复
