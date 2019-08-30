---
layout: post
title:  "使用 Pygame 应用"
date:   2018-07-28 12:00:00 +0530
categories: Python Pygame
---
似乎，上一篇就已经能够编写出一个大体的程序了，接下来将会对程序进行细化，掌握一些基础的用法，使我们的程序丰富起来，实现更多功能。

可以通过 `pygame.mixer.Sound` 来为程序增加音效或bgm，示例：

```python
bgm = pygame.mixer.Sound('sound/bgm.wav') # 加载背景音乐
channel_1 = pygame.mixer.Channel(1) # 设置为第一层
channel_1.play(bgm) # 播放背景音乐
```

> 注意：需要为声音设定层数，并设定播放

可以通过 `pygame.image.load` 来为程序加载图片，示例：
```python
background = pygame.image.load("assets/background.png") # 加载背景图片
```

可以通过 `pygame.display.set_caption` 为程序设定名称，示例：

```python
pygame.display.set_caption("Flappy Bird") # 设置游戏名称
```

可以通过在主程序下使用循环来侦测用户行为，示例：

```python
# 主程序
while True: # 循环执行
	for event in pygame.event.get(): # 侦测事件
		if event.type == pygame.QUIT: # 确定对事件的反馈
			sys.exit() # 直接退出循环，结束所有进程
		if keep_going: # 如果 keep_going 为 true 则循环执行
			if (event.type == pygame.MOUSEBUTTONDOWN): # 鼠标按下的交互
				fly = pygame.mixer.Sound('sound/fly.WAV') # 播放飞行声音
```

至此，你已掌握了 Pygame 的基础操作。

更多内容，可参考我的 [Github] 项目

[Github]: https://github.com/BingYanchi/FlappyBird/