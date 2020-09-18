---
weight: 1
title: "first_post"
date: 2020-09-16T20:39:49+08:00
draft: false
author: "YC"
description: "这篇文章展示了一些基本的用法"
resources:
- name: "featured-image"
  src: "featured-image.png"

tags: ["Markdown"]
categories: ["Markdown"]

lightgallery: true
toc:
  auto: false
---

{{< bilibili BV1T4411M7YN >}}

现在又配置了一下github actions更香了。
推送到远端服务器的网上太多了，正好刚配置完搜索的，就贴一下吧，帮助后来的小伙伴们。
```
- name: Use Node.js
        uses: actions/setup-node@v1
        with:
          node-version: '12.x'

      - name: Install automic-algolia
        run: | 
          npm install atomic-algolia
          npm run algolia
        env:
          ALGOLIA_APP_ID: ${{ secrets.ALGOLIA_APP_ID }}
          ALGOLIA_ADMIN_KEY: ${{ secrets.ALGOLIA_ADMIN_KEY }}
          ALGOLIA_INDEX_NAME: ${{ secrets.ALGOLIA_INDEX_NAME }}
          ALGOLIA_INDEX_FILE: "./public/index.json"
```

## 4 多语言和 i18n

**LoveIt** 主题完全兼容 Hugo 的多语言模式, 并且支持在网页上切换语言.

![语言切换](language-switch.gif "语言切换")

### 4.1 兼容性 {#language-compatibility}

{{< version 0.2.10 changed >}}

| 语言 | Hugo 代码 | HTML `lang` 属性 | 主题文档 | Lunr.js 支持 |
|:---- |:----:|:----:|:----:|:----:|
| 英语 | `en` | `en` | :(far fa-check-square fa-fw): | :(far fa-check-square fa-fw): |
| 简体中文 | `zh-cn` | `zh-CN` | :(far fa-check-square fa-fw): | :(far fa-check-square fa-fw): |
| 法语 | `fr` | `fr` | :(far fa-square fa-fw): | :(far fa-check-square fa-fw): |
| 波兰语 | `pl` | `pl` | :(far fa-square fa-fw): | :(far fa-square fa-fw): |
| 巴西葡萄牙语 | `pt-br` | `pt-BR` | :(far fa-square fa-fw): | :(far fa-check-square fa-fw): |
| 意大利语 | `it` | `it` | :(far fa-square fa-fw): | :(far fa-check-square fa-fw): |
| 西班牙语 | `es` | `es` | :(far fa-square fa-fw): | :(far fa-check-square fa-fw): |
| 德语 | `de` | `de` | :(far fa-square fa-fw): | :(far fa-check-square fa-fw): |
| 塞尔维亚语 | `pl` | `pl` | :(far fa-square fa-fw): | :(far fa-square fa-fw): |
| 俄语 | `ru` | `ru` | :(far fa-square fa-fw): | :(far fa-check-square fa-fw): |
| 罗马尼亚语 | `ro` | `ro` | :(far fa-square fa-fw): | :(far fa-check-square fa-fw): |
| 越南语 | `vi` | `vi` | :(far fa-square fa-fw): | :(far fa-check-square fa-fw): |

### 4.2 基本配置

学习了 [Hugo如何处理多语言网站](https://gohugo.io/content-management/multilingual) 之后, 请在 [站点配置](#site-configuration) 中定义你的网站语言.

例如, 一个支持英语, 中文和法语的网站配置:

```toml
# [en, zh-cn, fr, pl, ...] 设置默认的语言
defaultContentLanguage = "zh-cn"

[languages]
  [languages.en]
    weight = 1
    title = "My New Hugo Site"
    languageCode = "en"
    languageName = "English"
    [[languages.en.menu.main]]
      identifier = "posts"
      pre = ""
      post = ""
      name = "Posts"
      url = "/posts/"
      title = ""
      weight = 1
    [[languages.en.menu.main]]
      identifier = "tags"
      pre = ""
      post = ""
      name = "Tags"
      url = "/tags/"
      title = ""
      weight = 2
    [[languages.en.menu.main]]
      identifier = "categories"
      pre = ""
      post = ""
      name = "Categories"
      url = "/categories/"
      title = ""
      weight = 3

  [languages.zh-cn]
    weight = 2
    title = "我的全新 Hugo 网站"
    # 网站语言, 仅在这里 CN 大写
    languageCode = "zh-CN"
    languageName = "简体中文"
    # 是否包括中日韩文字
    hasCJKLanguage = true
    [[languages.zh-cn.menu.main]]
      identifier = "posts"
      pre = ""
      post = ""
      name = "文章"
      url = "/posts/"
      title = ""
      weight = 1
    [[languages.zh-cn.menu.main]]
      identifier = "tags"
      pre = ""
      post = ""
      name = "标签"
      url = "/tags/"
      title = ""
      weight = 2
    [[languages.zh-cn.menu.main]]
      identifier = "categories"
      pre = ""
      post = ""
      name = "分类"
      url = "/categories/"
      title = ""
      weight = 3

  [languages.fr]
    weight = 3
    title = "Mon nouveau site Hugo"
    languageCode = "fr"
    languageName = "Français"
    [[languages.fr.menu.main]]
      identifier = "posts"
      pre = ""
      post = ""
      name = "Postes"
      url = "/posts/"
      title = ""
      weight = 1
    [[languages.fr.menu.main]]
      identifier = "tags"
      pre = ""
      post = ""
      name = "Balises"
      url = "/tags/"
      title = ""
      weight = 2
    [[languages.fr.menu.main]]
      identifier = "categories"
      pre = ""
      post = ""
      name = "Catégories"
      url = "/categories/"
      title = ""
      weight = 3
```

然后, 对于每个新页面, 将语言代码附加到文件名中.

单个文件 `my-page.md` 需要分为三个文件:

* 英语: `my-page.en.md`
* 中文: `my-page.zh-cn.md`
* 法语: `my-page.fr.md`

{{< admonition >}}
请注意, 菜单中仅显示翻译的页面. 它不会替换为默认语言内容.
{{< /admonition >}}

{{< admonition tip >}}
也可以使用 [文章前置参数](https://gohugo.io/content-management/multilingual#translate-your-content) 来翻译网址.
{{< /admonition >}}

### 4.3 修改默认的翻译字符串

翻译字符串用于在主题中使用的常见默认值.
目前提供[一些语言](#language-compatibility)的翻译, 但你可能自定义其他语言或覆盖默认值.

要覆盖默认值, 请在你项目的 i18n 目录 `i18n/<languageCode>.toml` 中创建一个新文件，并从 `themes/LoveIt/i18n/en.toml` 中获得提示.

另外, 由于你的翻译可能会帮助到其他人, 请花点时间通过 [:(fas fa-code-branch fa-fw): 创建一个 PR](https://github.com/dillonzq/LoveIt/pulls) 来贡献主题翻译, 谢谢!

## 5 搜索

{{< version 0.2.0 >}}

基于 [Lunr.js](https://lunrjs.com/) 或 [algolia](https://www.algolia.com/), **LoveIt** 主题支持搜索功能.

### 5.1 输出配置

为了生成搜索功能所需要的 `index.json`, 请在你的 [网站配置](#site-configuration) 中添加 `JSON` 输出文件类型到 `outputs` 部分的 `home` 字段中.

```toml
[outputs]
  home = ["HTML", "RSS", "JSON"]
```

### 5.2 搜索配置

基于 Hugo 生成的 `index.json` 文件, 你可以激活搜索功能.

这是你的 [网站配置](#site-configuration) 中的搜索部分:

```toml
[params.search]
  enable = true
  # 搜索引擎的类型 ("lunr", "algolia")
  type = "lunr"
  # 文章内容最长索引长度
  contentLength = 4000
  # 搜索框的占位提示语
  placeholder = ""
  # {{< version 0.2.1 >}} 最大结果数目
  maxResultLength = 10
  # {{< version 0.2.3 >}} 结果内容片段长度
  snippetLength = 50
  # {{< version 0.2.1 >}} 搜索结果中高亮部分的 HTML 标签
  highlightTag = "em"
  # {{< version 0.2.4 >}} 是否在搜索索引中使用基于 baseURL 的绝对路径
  absoluteURL = false
  [params.search.algolia]
    index = ""
    appID = ""
    searchKey = ""
```

{{< admonition note "怎样选择搜索引擎?" >}}
以下是两种搜索引擎的对比:

* `lunr`: 简单, 无需同步 `index.json`, 没有 `contentLength` 的限制, 但占用带宽大且性能低 (特别是中文需要一个较大的分词依赖库)
* `algolia`: 高性能并且占用带宽低, 但需要同步 `index.json` 且有 `contentLength` 的限制

{{< version 0.2.3 >}} 文章内容被 `h2` 和 `h3` HTML 标签切分来提高查询效果并且基本实现全文搜索.
`contentLength` 用来限制 `h2` 和 `h3` HTML 标签开头的内容部分的最大长度.
{{< /admonition >}}

{{< admonition tip "关于 algolia 的使用技巧" >}}
你需要上传 `index.json` 到 algolia 来激活搜索功能. 你可以使用浏览器来上传 `index.json` 文件但是一个自动化的脚本可能效果更好.
[Algolia Atomic](https://github.com/chrisdmacrae/atomic-algolia) 是一个不错的选择.
为了兼容 Hugo 的多语言模式, 你需要上传不同语言的 `index.json` 文件到对应的 algolia index, 例如 `zh-cn/index.json` 或 `fr/index.json`...
{{< /admonition >}}
