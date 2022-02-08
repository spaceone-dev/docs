---
title: "Content Guide"
linkTitle: "content guide"
weight: 1
date: 2021-10-01
description: >
    This page contains guidelines for SpaceONE documentation.
---

## Create a new page
Go to the parent page of the page creation location. Then, click the 'Create child page' button at the bottom right.<br><br>
or:
<br>
You can also fork from [the repository](https://github.com/spaceone-dev/docs) and work locally.

## Choosing a title and filename
Create a filename that uses the words in your title separated by underscroe (_). For example, the topic with title Using [Project Management](/docs/guides/project/project_management/) has filename project_management.md.

## Adding fields to the front matter
In your document, put fields in the front matter. The front matter is the YAML block that is between the triple-dashed lines at the top of the page. Here's an example:

```yaml
---
title: "Project Management"
linkTitle: "Project Management"
weight: 10
date: 2021-06-10
description: >
  View overall status of each project and Navigate to detailed cloud resources.
---

```

{{% alert title="Attention" %}}
When writing a description, if you start a sentence without a space with a tab. Entire site will fail.   
{{% /alert %}}

### Description of front matter variables
| Variables | Description |
| :--- | :--- |
| title | The title for the content |
| linkTitle | Left-sidebar title |
| weight | Used for ordering your content in left-sidebar. Lower weight gets higher precedence. So content with lower weight will come first. If set, weights should be non-zero, as 0 is interpreted as an unset weight. |
| date | Creation date |
| description | Page description |

If you want to see more details about front matter, click [Front matter](https://gohugo.io/content-management/front-matter/).

## Write a document

### Adding Table of Contents
When you add `##` in the documentation, it makes a list of Table of Contents automatically.

### Adding images
Create a directory for images named **file_name_img** in the same hierarchy as the document. For example, create project_management_img directory for project_management.md. Put images in the directory.

### Style guide
Please refer to the [style guide](/docs/developers/contribute/document/style_guide/) to write the document.

## Opening a pull request
When you are ready to submit a pull request, commit your changes with **new branch**.
