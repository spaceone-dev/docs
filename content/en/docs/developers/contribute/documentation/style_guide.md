---
title: "Style Guide (shortcodes)"
linkTitle: "style guide"
weight: 2
date: 2021-10-01
description: >
    This page explains the custom Hugo shortcodes that can be used in SpaceONE Markdown documentation.
---

## Heading tag
It is recommended to use them sequentially from `##`, `<h2>`. It's for style, not just semantic markup.
{{< alert title="Note" >}}
When you add `##` in the documentation, it makes a list of Table of Contents automatically.
{{< /alert >}}

## Link button
Code :
```go-html-template
{{</* link-button background-color="navy400" url="/" text="Home" */>}}
{{</* link-button background-color="white" url="https://www.spaceone.org/" text="spaceone.org" */>}}
```

Output : <br>
{{< link-button background-color="navy400" url="/" text="Home" />}}
{{< link-button background-color="white" url="https://www.spaceone.org/" text="spaceone.org" />}}

## Video
Code :
```go-html-template
{{</* video src="https://www.youtube.com/embed/zSoEg2v_JrE" title="SpaceONE Setup" */>}}
```

Output: <br><br>
{{< video src="https://www.youtube.com/embed/zSoEg2v_JrE" title="SpaceONE Setup">}}

## Alert
Code :
```go-html-template
{{</* alert title="Note Title" >}}
	Note Contents
{{< /alert */>}}
```

Output: <br>
{{% alert title="Note Title" %}}
Note Contents
{{% /alert %}}

## Reference
* Learn about [Hugo](https://gohugo.io/)
* Learn about [How to use Markdown for writing technical documentation](https://experienceleague.adobe.com/docs/contributor/contributor-guide/writing-essentials/markdown.html?lang=en)