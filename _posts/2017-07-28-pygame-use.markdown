---
layout: post
title:  "使用 Pygame 应用"
date:   2018-07-28 12:00:00 +0530
categories: Python Pygame
---
似乎，上一篇就已经能够编写出一个大体的程序了，接下来将会对程序进行细化，掌握一些基础的用法，使我们的程序丰富起来，实现更多功能。

可以通过`pygame.mixer.Sound`来为程序增加音效或bgm，示例：

```python
bgm = pygame.mixer.Sound('sound/bgm.wav') # 加载背景音乐
channel_1 = pygame.mixer.Channel(1) # 设置为第一层
channel_1.play(bgm) # 播放背景音乐
```

> 注意：需要为声音设定层数，并设定播放