# LearnAndroidDevelopment

> Learn Android Development via a Project in 2019

## Archived

我们已经在2019年10月基本完成了对相关知识的学习，并在一定程度上实现了作为目标的 `Musharing` 项目，故此仓库就此封存，不再更新。

在实现的过程中，我们只在这个仓库中放入了一部分 Java以及一小部分杂项的 学习笔记。这个系列的笔记对 Java 基础知识作了比较精炼的总结，可供学习参考与日常查阅。这一系列文章也可在我的博客 [clownote](https://clownote.github.io) 中找到。

关于 **Android开发** 部分，我们学习了 郭霖（[@guolindev](http://guolin.tech)）的《《第一行代码 第2版》，这本书由浅入深，逻辑清晰，各种操作都讲解的比较详细，我们很难在其基础上再做提炼，推荐阅读原书。

## 说明

这个项目旨在帮助我们学习相关的知识以完成项目 `Musharing-Android`。用于共享学习资料与分享学习心得，同时也提出每周的计划督促大家学习。

该 GitHub项目 提供的功能：

* 查看每周的学习计划
* 存放我们在学习过程中的资料、笔记以及其他相关内容
* 为大家提供一个交流的场所
* 练习使用 GitHub 平台，参与一个开源项目，尝试以开发者的方式解决问题

在项目中出现的问题希望大家可以在 GitHub 上协作解决，共同完成，在内容上相互补充，互相帮助、学习，以在最短的时间内完成学习的任务。

## 关于使用

1. **每周计划**：我们会把每周的学习计划会使用 [`Projects`](https://github.com/musharing-team/LearnAndroidDevelopment/projects) 分条提出，并逐个开 `Issues`，方便大家讨论，在所有人完成后 `close`。同时也会把所有一个完整的计划文件放到 [`Weekly`](https://github.com/musharing-team/LearnAndroidDevelopment/tree/master/Weekly) 目录中，供大家参考。
2. **学习笔记**：我们可以把自己学习的笔记提交到 [`Daily`](https://github.com/musharing-team/LearnAndroidDevelopment/tree/master/Daily) 目录中。每个人一个独立的目录，公共性质的可以以 [`worker`](https://github.com/orgs/musharing-team/people/musharingWorker) 的身份提交（或直接提交到 [`worker` 子目录](https://github.com/musharing-team/LearnAndroidDevelopment/tree/master/Daily/worker)中），用以分享。

【注】关于提交，见下面的详细说明。

3. **学习资料**：我们可以把自己发现的好的学习资料放到 [`Materials`](https://github.com/musharing-team/LearnAndroidDevelopment/tree/master/Materials) 目录。
4. **项目准备**：我们在项目准备过程中的一些文件(非隐私性)可以放到 [`Project`](https://github.com/musharing-team/LearnAndroidDevelopment/tree/master/Project) 目录中。
4. **提出问题**：有任何问题都可以开 [`Issues`](https://github.com/musharing-team/LearnAndroidDevelopment/issues)，大家可以一起讨论。

## 提交说明

* 在学习的过程中，每个人都应该把这个仓库 `Fork` 一份。

每次使用，都应该先尝试从 `musharing-team/LearnAndroidDevelopment` pull 一份master，以保持更新；
然后在自己 Fork 得到的 仓库中创作、修改；
在确认无误后在**在次日00:00前**提交一个 `pull request`，在收到请求后，[管理员](https://github.com/cdfmlr)将及时统一处理。

【注】即使你用这个权限，也请不要自己将自己的请求验证通过、 `merge` 进 `musharing-team/LearnAndroidDevelopment`！

* 如果在有特殊需求的情况下，如果有需要大量合作的部分，也有可能会在 `musharing-team/LearnAndroidDevelopment` 中直接开 `branch`，但这不会是该项目中的主流操作。

* 所有的提交操作 **必须提供简要说明！**

例如，在 `example.txt` 中将错误拼写 “栗子” 修改为正确的 “例子” 后，应该在 commit 时说明：`修改拼写错误: 栗子 -> 例子`。 

---

## 最终目标：完成项目 —— 曉音（Musharing）

我们通过一段时间的学习，将在最终完成一个名为 “*曉音*” 的 Android App 开发，下面是这个 App 的简介：

#### 世界上第一台随身听

1979年7月1日，索尼发布了第一款标志性的盒式磁带随身听TPS-L2。令人印象深刻的是，它配备有两个迷你耳机插孔，允许两个人同时收听。同时，TPS-L2有一个“热线”按钮，用来激活一个小的内置麦克风，部分覆盖磁带中的声音，允许一个用户通过音乐与另一个用户交谈。
在这个随身听已经几乎成为历史的时代里，偶有那么一刻，我们会怀念它曾经带给我们的仪式感与感动。这是“曉音”诞生的初衷。
在参考了索尼最早的一代便携式音乐播放器后，我们打算将它的功能付诸软件，开发一个手机App版的TPS-L2。

#### 现在 有一首歌只想和你听

网易云把小众音乐的爱好者聚集在了一起，全民k歌为每个人预留了发挥的空间。二者的火爆，是因为许多音乐是应该拿出来与大家一起分享的——而有的音乐，只愿意与一个人分享。
“曉音”只为你把音乐分享给那个人。
“曉音”秉持极简主义风格，播放音乐的同时，可以用在应用内进行聊天交互，虽然是用键盘输入的文字，但它更像我们在说话，不能撤回，也只能用自己的记忆保存。
不论携手相依，或是相隔异地。愿此刻二人世界，只有音乐为伴。

#### 说不出的话 曉音帮你唱出来

文字不能传达的，就亲口对ta说。
对话键旁有一个“热键”，按下后音乐的声音将被调低，同时设备的麦克风将采集你的声音并传达给那个人。
把不敢说的话，用唱的方式告诉ta。


#### 与其它软件的比较
首先需要明白的一点是，具有近似功能的软件不在少数，YouTube、哔哩哔哩、优酷、腾讯、爱奇艺都是播放软件，它们共同存在的原因是，各自有不同的侧重点（自制、番剧、大片、综艺、网络剧）。

“曉音”的侧重点，在于它是一个交互感、私密感、体验感都很强的熟人社交音乐软件。与其它软件不同的在于，注重交流，追求同步与即时，旨在传达感情。

#### 功能实现

* 让App的用户(A)，可以和另一用户(B)同步收听一首歌曲。用户(A)可以通过私信的方式邀请用户（B）共享音乐。在音乐播放期间，两方都可以随时暂停音乐，音乐也一直同步播放。
* 在收听时，不但可以通过已有的聊天界面和其他用户聊天，还能在歌曲播放时，按下发声按钮，说一段话，让这段话随乐声传进另一人耳中。

