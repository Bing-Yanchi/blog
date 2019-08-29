---
layout: post
title:  "使用 Pygame 初步"
date:   2018-03-04 12:00:00 +0530
categories: Python Pygame
---
上一篇文章讲述了 Pygame 的大体内容，这一篇就要步入初始篇章。讲述 Pygame 程序的必要内容，也就是初始内容。通过简单的编写，即可快速上手 Pygame。

首先，导入 Pygame 库：

```python
import pygame
```

建议导入 sys 库，以便于结束进程：
```python
import sys # sys 用于快速结束程序,Python 自带
```


接着，初始化与画布大小：

```python
pygame.init() # 完成初始设置
screen = pygame.display.set_mode([288,512]) # 创建指定大小的画布
```

接下来，编写主程序：
```python
clock = pygame.time.Clock() # 调用帧数
# 主程序
while True: # 循环执行
	for event in pygame.event.get(): # 侦测事件
		if event.type == pygame.QUIT: # 确定对事件的反馈
			sys.exit() # 直接退出循环，结束所有进程
	# 基础类设置
	pygame.display.update() # 调用游戏更新
	clock.tick(60) # 帧数设定
pygame.quit() # 撤销初始化后的设置
```

至此，你已完成基础配置。
