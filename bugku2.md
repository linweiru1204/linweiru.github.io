# Bugku CTF2 linux Writeup
## 题目信息：
MISC（杂项）；为Linux基础问题；有`key{ }`做提示
## 解题步骤：
1. 下载文件后得到一个名为linux的压缩包（zip），将其解压
2. 进入后有一名为linux的子文件夹，选择”Open Git Bash here”进入
3. 输入`cd linu`x进入子文件夹
4. 再输入`ls -la`后发现有一文件1.tar.gz
5. 执行`tar -zxvf 1.tar.gz`将其解压， 输入`ls -la`生成新文件夹test
6. 输入`grep -r key.`提示`Binary file test/flag matches`，说明其是一个包含key关键词的二进制文件
7. 执行`strings test/flag | grep key`后无反应，输入`cat test/flag`后出现乱码文件
8. 找到`key{feb81d3834e2423c9903f4755464060b}`
