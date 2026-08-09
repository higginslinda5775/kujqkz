九游地址登录【Q-——333307——】九游地址登录【 辋芷《888yx●vip》 】
九游地址登录【Q-——333307——】九游地址登录【 辋芷《888yx●vip》 】

 从0到1搭建个人博客：我是如何用Hexo+GitHub Pages实现自动化部署的

如果你有一个程序员朋友，大概率听TA提过“博客”二字。但很多人卡在了第一步：如何低成本、高效率地搭建一个属于自己的技术博客？

今天不聊虚的，直接分享我折腾了一周后，最终锁定的方案——Hexo + GitHub Pages + 自动化部署。整个过程零服务器成本，且SEO友好，非常适合沉淀技术文章。

 为什么选Hexo而非WordPress？

首先是速度。Hexo是纯静态页面生成器，无需数据库，加载速度极快。其次是版本管理，所有文章都是Markdown文件，天然适配Git，写文章像提交代码一样清爽。最后是定制自由，主题、插件生态丰富，几行配置就能改出个人风格。

 三步完成核心搭建

第一步：本地环境初始化  
全局安装Hexo命令行工具，然后执行 `hexo init` 创建项目骨架。紧接着 `hexo g`（生成静态页）和 `hexo s`（本地预览）测试通过后，你的博客就“活”了。

第二步：绑定GitHub仓库  
在GitHub新建一个仓库，命名为`你的用户名.github.io`，然后在项目配置文件 `_config.yml` 的 deploy 节点里填入仓库地址。这一层映射关系是GitHub Pages免费托管的底层逻辑。

第三步：开启自动化部署  
这是我最受益的一环——利用GitHub Actions实现“推代码即更新”。你只需在`.github/workflows/`目录下创建一个工作流文件，指定触发分支（如main），然后在steps中执行安装依赖、生成静态文件、推送至目标分支三个动作。从此告别手敲`hexo d`。

 高频踩坑点

- Node版本冲突：建议本地使用nvm切到16+，避免编译报错。
- 图片路径困扰：修改Hexo配置中的 `post_asset_folder` 为true，配合标签语法引用图片，可解决相对路径失效问题。
- 搜索功能缺失：本地安装 `hexo-generator-searchdb` 插件，并在主题配置中开启，访客就能全文检索了。

 互动一下

你现在用的是哪套博客方案？是动态框架（如Halo、WordPress）还是静态生成器（如Hexo、VitePress）？如果你正卡在部署这一步，评论区留下你的报错截图，我会优先回复。

如果你觉得这篇实战记录对你有参考价值，点赞+收藏 能让更多需要它的人看到。下一期计划拆解“如何让博客被Google快速收录”，感兴趣的话点个关注，更新不迷路。

相关推荐：

https://github.com/greenesteven0/blwjrs/blob/main/%E5%85%B1%E8%B5%B4%E6%96%87%E5%BF%83%E4%B9%8B%E7%BA%A6%EF%BC%9A%E4%B9%9D%E6%B8%B8%E5%AE%98%E6%96%B9%E6%B3%A8%E5%86%8C_%E8%82%BF%E7%BC%86%E5%93%89%E7%8A%B6%E5%88%83JJKYT.md

<img src="https://i.postimg.cc/TYXBNX0W/mei-nu-bei-jing-zhao-shang-tu-zhi-zuo-(85).png" />

相关推荐：

https://github.com/greenesteven0/blwjrs/commit/8bce6ae9d82d3693d40d88b49255443daaead168

<img src="https://i.postimg.cc/hPb6H33g/mei-nu-bei-jing-zhao-shang-tu-zhi-zuo-(87).png" />
相关推荐：

https://github.com/thompsonkayla8950/bdrfuj/blob/main/2026%E7%AC%AC%E4%B8%80%E5%B9%B2%E8%B4%A7%EF%BC%9A%E4%B9%9D%E6%B8%B8%E5%AE%98%E6%96%B9%E5%BC%80%E6%88%B7_%E8%80%98%E5%A4%B4%E6%B4%9E%E4%BA%A4%E6%B4%BECPXMM.md

<img src="https://i.postimg.cc/sD9qt00C/mei-nu-bei-jing-zhao-shang-tu-zhi-zuo-(86).png" />
相关推荐：

https://github.com/thompsonkayla8950/bdrfuj/commit/d7c75197057cd47cc613b6ac755fc088b1534ebc

<img src="https://i.postimg.cc/VsqjR9pF/mei-nu-bei-jing-zhao-shang-tu-zhi-zuo-(79).png" />

资讯来源：新华网、人民网、央视新闻、中新网、凤凰网、澎湃新闻、界面新闻、新浪新闻、搜狐网、财新网、观察者网、第一财经等主流平台，以独树一帜的观察视角与扎实的深度报道能力，在资讯领域收获广泛关注。
