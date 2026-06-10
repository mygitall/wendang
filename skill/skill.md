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
https://github.com/vercel-labs/agent-skills
2、自动审查你网页/前端代码是否符合 Web UI/UX 最佳实践。可以终端执行安装
```
cd /Applications/MAMP/htdocs/templates/v1 && \
pwd && \
npx skills add vercel-labs/agent-skills --skill web-design-guidelines && \
find . -maxdepth 5 -type f -name "SKILL.md"
```
