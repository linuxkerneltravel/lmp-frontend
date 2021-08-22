# Git分支规范

本项目分支分为：
- main：主分支，进行重大版本发布。
- dev：开发分支，进行日常开发，代码最新版本。
- 临时性分支：针对需求和特定目的进行版本开发的分支。

临时性分支命名规范：前缀_描述，前缀包括：
- feature：新功能；
- bugfix：Bug修复；
- release：预发布；

# Git日志规范

> Git日志即使用`git commit`命令时所提交的`commit message`。

`commit message`格式要求：type（类型）+空格+subject（描述信息：本次提交的目的，具体做了什么操作...）。

type必须是以下类型：
- [Feature]：新功能；
- [Bugfix]：bug修复；
- [Docs]：文档修改；
- [Test]：增加测试；
- [Merge]：代码合并；
- [Optimize]：功能、性能优化；
- [Typo]：拼写错误，多个请用Typos；

示例：`git commit -m '[Feature] 新增功能xxx'`

注意`subject`末尾不需要加标点符号。

# Git提交规范

## 新需求开发

> 进行新需求开发时，需要从`dev`分支创建一个新分支进行个人开发。

```bash
# 切换分支
git checkout dev
# 从当前分支创建新分支
git checkout -b 分支名称
# 将创建的分支推送到远程仓库
git push
```

新需求开发完成后，提交PR将所开发的代码，合并到`dev`分支上。