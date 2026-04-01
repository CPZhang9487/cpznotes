# **中文搜索支持**

參考

- <https://squidfunk.github.io/mkdocs-material/setup/setting-up-site-search/>
- <https://squidfunk.github.io/mkdocs-material/plugins/search/>

添加所需依賴

```bash
uv add jieba
```

在 `mkdocs.yml` 添加

```yaml
theme:
  language: zh-TW

  features:
    - search.highlight
    - search.share
    - search.suggest

plugins:
  - search:
      lang:
        - en
        - ja  # 不知道為甚麼，jieba 要加上日語搜索才更好支持中文搜索
        - zh
      pipeline:
        # - stemmer  # 這不要加比較好
        - stopWordFilter
        - trimmer
      separator: '[\s\-,:!=\[\]()"/]+|(?!\b)(?=[A-Z][a-z])|\.(?!\d)|&[lg]t;'
```
