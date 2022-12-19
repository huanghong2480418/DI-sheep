# 老师们，同学们，大家好，我是初三十九班学号为20号的同学，最近我做了些小东西（均为二创），欢迎大家游玩，由于github是外国的网站，进去可能会变的稍加困难🌝

一🌸游戏网站🌸一

夏鸡蛋钢琴块🐔🥚❤：
https://huanghong2480418.github.io/EatKano

猪妈妈钢琴块🐷👩‍🦰❤：
https://huanghong2480418.github.io/PIG

夏鸡蛋飞飞乐🐔🥚❤：
https://huanghong2480418.github.io/EggDino

合成夏头鸡蛋🐔🥚❤：
https://huanghong2480418.github.io/yuanegg

夏蛋坤KUROMi🐔🥚❤（测试阶段）：
https://huanghong2480418.github.io/Kunball

一🌸常见问题🌸一
1.无法访问此网站链接已重置：
①多次刷新（至少1分钟）
②使用梯子
2.出现Github404页面：
①可能是号没了，或者是关闭了
②网址打错了，注意区分大小写
3.没有声音：
①断开与蓝牙耳机的连接，重新访问
②刷新网站有几率恢复
③使用梯子
4.卡在加载页面：
①耐心等待
②多次刷新
③使用梯子

一🌸免费梯子🌸一
https://wwr.lanzoui.com/b03joy6eb
提取码 : wlan
如果你使用了梯子，可以查看以下视频：
https://www.youtube.com/watch?v=mIif-7U2tEU&t=753s
https://www.youtube.com/watch?app=desktop&v=fqYnZagl9vU
注意事项：请不要拿他做不好的事情，仅用于访问以上链接，仅支持安卓端，访问别的网站的话，小心网警。

一🌸意见反馈🌸一
有问题吗？欢迎邮箱反馈！
谷歌taiy07709@gmail.com
（谷歌没梯子收不到）
网易huanghong2480418@163.com
腾讯2810289451@qq.com

一🌸物理视频🌸一
https://wwp.lanzoup.com/iJJYK0ixv0eh
提取码 : wlan

一🌸Github煮噎🌸一
https://www.github.com/huanghong2480418

# DI-sheep：深度强化学习 + 羊了个羊

当 AI 技术的明珠——深度强化学习，遇到号称“通关率只有0.01%”的游戏“羊了个羊”，会碰撞出哪些奇思妙想呢？

P.S. 路过记得点个 star ![stars - di-sheep](https://img.shields.io/github/stars/opendilab/di-sheep?style=social) ，持续更新ing。

P.S.S. 想了解更多深度强化学习相关知识？快来 [DI-engine](https://github.com/opendilab/DI-engine) 训练自己的智能体。

<div align="center">
    <a href="https://github.com/opendilab/DI-sheep"><img width="500px" height="auto" src="https://github.com/opendilab/DI-sheep/blob/master/ui/public/demo.gif"></a>
</div>

# News
- [bilibili] [羊群加不进去？那就来加猫群叭！深度强化学习版的羊了个羊来了](https://www.bilibili.com/video/BV1N24y1o7Lw/?spm_id_from=333.999.0.0)
- [WeChat] [万事开头难？喵小DI玩“羊了个羊”可不难](https://mp.weixin.qq.com/s/4Z3WtkcWRp6x4x60RVELfQ)

# 使用指南

## 算法原理解析
![disheep drawio](https://user-images.githubusercontent.com/33195032/191955286-7c309e9d-6e35-491f-93b3-b14cd1fe033f.png)

## 快速上手

- 如果想**在线试玩** --> [在线网页（改进中）](https://opendilab.net/sheep)
- 如果想**本地部署/测试**
  - 服务端（Python）
    ```shell
    # 预先安装好 Python3
    cd service
    pip install -r requirement.txt
    FLASK_APP=app.py flask run  # 玩家试玩
    # FLASK_APP=agent_app.py flask run  # 玩家 + AI 试玩
    ```
  - 客户端（react）
    ```shell
    # 预先安装好 node.js 和 react
    cd ui
    npm run build
    npm run preview
    ```
    然后在网页中打开对应链接即可
- 如果想进行完整的深度强化学习训练
    ```shell
    # 预先安装好 Python3
    cd service
    pip install -r requirement-train.txt
    python3 -u sheep_ppo_main.py
    ```
- 如果想使用定义好的 gym 羊了个羊环境 --> 点个 star 之后直接暴力 CTRL C+V 拿走 `service/sheep_env.py` 尽情魔改
- 如果想获得训练好的深度强化学习模型 --> 访问 [OpenDILab官网下载链接](https://opendilab.net/download/DI-sheep/) （目前提供了两种试玩模型，但智能体仍有很多进步空间）
- 如果想了解更多深度强化学习相关知识 --> 欢迎参阅 [DI-engine](https://github.com/opendilab/DI-engine) 和[相关文档](https://di-engine-docs.readthedocs.io/zh_CN/latest/)
- 如果想了解未来的更新计划 --> 请参阅[更新计划](#更新计划)
- 如果有其他问题或想法 --> 欢迎 github ISSUE 区讨论，或是贡献 Pull requests

## 项目结构
```text
.
├── LICENSE
├── ui                       --> react 网页前端
└── service                  --> Python 核心模块（算法和服务端）
    ├── app.py                  --> flask 服务 app (仅人类操作)
    ├── agent_app.py                  --> flask 服务 app（人类+AI操作）
    ├── requirement.txt         --> Python 依赖库列表
    ├── sheep_env.py            --> gym 格式环境
    ├── sheep_model.py          --> 基于 PyTorch 的 Actor-Critic 神经网络模型
    ├── sheep_ppo_main.py       --> 基于 DI-engine 的深度强化学习训练主函数
    ├── test_sheep_env.py       --> gym 格式环境的单元测试
    └── test_sheep_model.py     --> 神经网络模型的单元测试
```



# 更新计划

## 算法

- [ ] 强化学习训练参数调整和算法微调
- [ ] 提供可供本地试玩的模型权重
- [ ] 详细的神经网络和强化学习算法设计文档
- [ ] model-based RL 和 planning 算法
- [ ] 神经网络压缩（用于部署） 

## 环境
- [ ] 添加原类型游戏（比如3tiles）中的各种道具
- [ ] 牌的层数问题如何定义
- [ ] 结合 JAX 优化环境运行速度
- [ ] 更多结合 AI 的玩法设计


## 应用
- [x] 更多自定义主题和 BGM
- [x] 在线网页端部署
- [x] 样例神经网络权重下载
- [ ] 更多 AI 训练时的行为分析
- [ ] 移动端应用（欢迎Android/IOS开发者支持）


# 致谢
- react 前端部分主要参考 https://github.com/StreakingMan/solvable-sheep-game ，请大家也多多支持这个 repo 


# License
DI-sheep is released under the Apache 2.0 license.
