# **初始化**

推薦使用 [uv](https://docs.astral.sh/uv/) 管理專案

首先初始化 uv

```bash
uv init
```

接著添加所需依賴

```bash
uv add mkdocs-material
```

再來參考

- <https://squidfunk.github.io/mkdocs-material/creating-your-site/>
- <https://squidfunk.github.io/mkdocs-material/setup/extensions/#recommended-configuration>

初始化 MkDocs

```bash
uv run mkdocs new .
```

並修改 `mkdocs.yml`

適當的設定 site_name 與 site_url

```yaml
site_name: CPZ Notes
site_url: https://cpzhang9487.github.io/cpznotes

theme:
  name: material

markdown_extensions:

  # Python Markdown
  - abbr
  - admonition
  - attr_list
  - def_list
  - footnotes
  - md_in_html
  - toc:
      permalink: true

  # Python Markdown Extensions
  - pymdownx.arithmatex:
      generic: true
  - pymdownx.betterem:
      smart_enable: all
  - pymdownx.caret
  - pymdownx.details
  - pymdownx.emoji:
      emoji_index: !!python/name:material.extensions.emoji.twemoji
      emoji_generator: !!python/name:material.extensions.emoji.to_svg
  - pymdownx.highlight
  - pymdownx.inlinehilite
  - pymdownx.keys
  - pymdownx.mark
  - pymdownx.smartsymbols
  - pymdownx.superfences
  - pymdownx.tabbed:
      alternate_style: true
  - pymdownx.tasklist:
      custom_checkbox: true
  - pymdownx.tilde
```

若使用 [VS Code](https://code.visualstudio.com/)

可再添加 `.vscode/settings.json` 以更好的設置 `mkdocs.yml`

```json
{
  "yaml.schemas": {
    "https://squidfunk.github.io/mkdocs-material/schema.json": "mkdocs.yml"
  },
  "yaml.customTags": [
    "!ENV scalar",
    "!ENV sequence",
    "!relative scalar",
    "tag:yaml.org,2002:python/name:material.extensions.emoji.to_svg",
    "tag:yaml.org,2002:python/name:material.extensions.emoji.twemoji",
    "tag:yaml.org,2002:python/name:pymdownx.superfences.fence_code_format",
    "tag:yaml.org,2002:python/object/apply:pymdownx.slugs.slugify mapping"
  ]
}
```
