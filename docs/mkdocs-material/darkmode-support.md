# **深色模式支援**

參考

- <https://squidfunk.github.io/mkdocs-material/setup/changing-the-colors/>
- <https://squidfunk.github.io/mkdocs-material/setup/changing-the-colors/#system-preference>

在 `mkdocs.yml` 添加

```yaml
theme:
  palette:

    # Palette toggle for light mode
    - media: "(prefers-color-scheme: light)"
      scheme: default
      toggle:
        icon: material/brightness-7
        name: Switch to dark mode

    # Palette toggle for dark mode
    - media: "(prefers-color-scheme: dark)"
      scheme: slate
      toggle:
        icon: material/brightness-4
        name: Switch to light mode
```
