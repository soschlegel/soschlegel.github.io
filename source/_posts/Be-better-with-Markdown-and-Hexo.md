---
title: Be better with Markdown and Hexo
date: 2020-05-17 20:17:53
tags: 
    - Hexo
    - Markdown
    - VSCode
subtitle: You want to start writing blogs with Hexo? Here you'll find some help to do improve your work and make your life easier
---

* After you have started writing a blog, you will quickly notice your first mistakes: Bad grammar if you are not a native speaker and very often typos. This will also be a collection of snippets and small How-Tos with Hexo. Then it's time to start thinking about how you can get better with the right plugins and be more productive with the right tools - so here we go!

## Updates

* 17.05.2020: Initial create
* 21.05.2020: added section [Include Images](#include-images)
* 24.05.2020: added section [Read more](#read-more)

<!-- more -->

## Code Spell Checker

Typos can happen to everybody and every time, so it's probably a good idea to use a Spell Checker. At first look, this [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) seems to be the most popular - so install it to VSCode and test it for a while :-)

## DeepL plugin

For me and many others [DeepL.com](https://www.deepl.com/translator) is definitely the best translation solution. Let's say something like "next-generation-Google-Translate". And at least for Windows and macOS [a nice plugin is available](https://www.deepl.com/app), which offers you a quick and easy solution for doing translations. Using it on Windows, you simple mark a text to translate and git `CTRL+C+C`. This can be used in any program like Chrome, Windows or VSCode and opens a small Window where you can select your target language to translate to.

![Screenshot of DeepL-Plugin](Be-better-with-Markdown-and-Hexo/20200517a.png)

## Enhanced Markdown preview

Some people don't even know that by default a Markdown-Preview is embedded in VSCode (activate it by clicking the button in the upper right corner). Relying a high number of installations and downloads the Plugin [Markdown Preview Enhanced](https://shd101wyy.github.io/markdown-preview-enhanced/#/) might be even better then the default one. I've been using it from the beginning and maybe someone knows the standard preview and knows where the differences are.

![Find Markdown Preview Button](Be-better-with-Markdown-and-Hexo/20200517b.png)

Install it using this [link](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced) to VSCode or search for `markdown-preview-enhanced` in `Extensions`.

## PlantUML

Sometimes pictures say more then thousand words, so just use this easy solution described [in this article](https://www.freecodecamp.org/news/inserting-uml-in-markdown-using-vscode/) to use the PlantUML-Syntax to improve your posts with nice UML-Graphics.

``` plantuml
@startuml
    actor Guest
    note right of YourBlog: Built with PlantUML
    YourBlog <- Guest : visits it
    YourBlog -> Guest : understands quickly
    YourBlog -> Guest : loves it
@enduml
```

by simple using this little bit of "code"

``` bash
actor Guest
note right of YourBlog: Built with PlantUML
YourBlog <- Guest : visits it
YourBlog -> Guest : understands quickly
YourBlog -> Guest : loves it
```

For a more information about the setup and capabilities of PlantUML just visit the [official page](https://plantuml.com/de/sequence-diagram).

## Include Images

Including images with Hexo also works with normal Markdown-Syntax - also very simple, but comes with problems if you do it wrong, like a had to learn:

![Images missing on detail page](Be-better-with-Markdown-and-Hexo/20200521a.png)

This is caused by wrong relative paths, when you switch between "list-view" and "detail-view". They official solution by provided by Hexo is not so elegant, so they I decided to use this [simple approach](https://chrismroberts.com/2020/01/06/using-markdown-in-hexo-to-add-images/).

In short words:

* activate `post-asset-folder` in `_config.yml`
  
```yaml
post_asset_folder: true
```

* Install `hexo-asset-link`
  
```bash
npm i -s hexo-asset-link
```

* Then store your images in the generated `Post-Asset-Folder` which is named like your post, i.e.

![Structure of Source-Folder](Be-better-with-Markdown-and-Hexo/20200521.png)

``` markdown
![Structure of Source-Folder](Be-better-with-Markdown-and-Hexo/20200521.png)
```

## Read more

If you want to include a ![READ More Button](Be-better-with-Markdown-and-Hexo/20200524.png) on your overview-page, you simply need to include the `<!--more -->`-Tag at your wanted position in your post.

{% card %}
This feature has to be supported by your theme!
{% endcard %}


## others

... time to time I'll extend this list with new stuff. Next one will probably be some solution for PlantUML and Hexo/Markdown ...
