## 调用skill技巧
 ```
 claude 是“/”斜杠+skill名称
  codex是”$“美元符号+skill名称
 ```
### PTT skill

1、PTT skill
```
https://github.com/op7418/guizang-ppt-skill
```

### web-design-guidelines

2、自动审查你网页/前端代码是否符合 Web UI/UX 最佳实践。可以终端执行安装、

https://github.com/vercel-labs/agent-skills
```
cd /你的项目路径 && \
pwd && \
npx skills add vercel-labs/agent-skills --skill web-design-guidelines && \
find . -maxdepth 5 -type f -name "SKILL.md"
```
```
cd /Applications/MAMP/htdocs/templates/v1

请只做两件事：

1. 在当前目录安装 web-design-guidelines skill：
   npx skills add vercel-labs/agent-skills --skill web-design-guidelines

2. 安装成功后，使用 web-design-guidelines 审查当前模板目录的 HTML/CSS/JS。

禁止：
- 不要修改任何文件
- 不要格式化代码
- 不要重构
- 不要新增依赖
- 不要删除文件

只给我审查报告，必须包含：
- 实际安装路径
- 被审查的文件列表
- High / Medium / Low 问题分类
- 每条问题的 file:line
- 最小修改建议
```
