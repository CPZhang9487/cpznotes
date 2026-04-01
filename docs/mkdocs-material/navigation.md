# **導航相關**

參考 <https://squidfunk.github.io/mkdocs-material/setup/setting-up-navigation/>

修改 `mkdocs.yml`

適當的修改 nav

```yaml
  features:
    - navigation.expand
    - navigation.indexes
    - navigation.instant
    - navigation.instant.prefetch
    - navigation.instant.preview
    - navigation.instant.progress
    - navigation.path
    - navigation.prune
    - navigation.sections
    - navigation.tabs
    - navigation.tabs.sticky
    - navigation.top
    - navigation.tracking
    - toc.integrate
    - toc.follow

nav:
  - 首頁:
    - index.md
  - Material for MkDocs:
    - mkdocs-material/index.md
    - mkdocs-material/navigation.md
```
