# Pandora 技能仓库

供 Pandora 技能安装器列出和安装技能。当前为私有仓库，访问时需要通过 `GH_TOKEN` 或 `GITHUB_TOKEN` 提供有读取权限的 GitHub 凭据。

## 目录

- `skills/.curated/`：可安装的精选技能。
- `skills/.experimental/`：实验性技能，暂未收录。

每个技能使用独立目录，必须包含带有 `name`、`description` 的 `SKILL.md`，脚本、参考资料和资源文件可按需附带。

## 使用

```bash
python3 "${PANDORA_HOME:-$HOME/.pandora}/skills/.system/skill-installer/scripts/list-skills.py" --repo catPaw-s/pandora-skills
python3 "${PANDORA_HOME:-$HOME/.pandora}/skills/.system/skill-installer/scripts/install-skill-from-github.py" --repo catPaw-s/pandora-skills --path skills/.curated/project-overview
```

`project-overview` 是用于梳理项目结构的中文示例技能。安装本身只复制文件，不会自动执行技能操作。
