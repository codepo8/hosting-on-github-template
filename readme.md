# Hosting HTML/CSS/JS on GitHub

bq. This is a bare-bones example how to host an HTML/CSS/JavaScript example page on GitHub pages. You can fork this repo and get started. 

## Step 1: Create a new repository (or fork this one)

The first step is to get a GitHub account and create a new repository. This one, for example is called `hosting-on-github-template` and is available at `https://github.com/codepo8/hosting-on-github-template` with `codepo8` being my user name. 

## Step 2: Turn on GitHub Pages

1. Go to the settings of the repository and go to pages in the secondary navigation:

    ![The settings of the repository link in the main navigation and the pages link in the secondary navigation](images/settings-pages.png)
1. Select `Deploy from a branch` under `Build and deployment`, choose the `main` branch and the `root` folder and press save.

    ![The Github pages screen with the sections highlighted you should interact with](images/github-pages.png)
    This triggers the build of the page. 
1. Check the `Actions` tab of the main navigation to see the page being built. 

    ![Actions tab showing a running build of GitHub pages](images/actions.png)
    Whilst building this shows a yellow animated dot. When it is done it turns into a green check mark. If there are some issues it will show an error icon and explain what went wrong. Once it is in the green, your changes are live. 
1. When the page is done building you can see in the `Pages` section that it has been deployed. 

    ![Github pages section with successfully deployed page information](images/published-page.png)

    Your page is now available on the web as an HTML/CSS/JS capable environment. For example, this one is at https://codepo8.github.io/hosting-on-github-template/.

    The structure is `https://{{user}}.github.io/{{repository_name}}/` and comes from the repository URL at `https://github.com/{{user}}/{{repository_name}}`. 

## Step 3: Host your HTML/CSS/JS 

And that's all there is to it. You can now put HTML/CSS/JS documents, images and videos into your repository and they will be shown in the browser under the pages URL. For example, the [simple-html-demo.html](https://github.com/codepo8/hosting-on-github-template/blob/main/simple-html-demo.html) file here is available rendered as HTML at https://codepo8.github.io/hosting-on-github-template/simple-html-demo.html. 

Every time you change the code and push to the repository the build process runs in the background and the pages get deployed.

## Advanced: Use templates and includes to publish Markdown content as HTML

Instead of simply hosting HTML, you can also write your content in markdown and have GitHub show it as HTML pages. For example, the [markdown.md](https://github.com/codepo8/hosting-on-github-template/blob/main/markdown.md) file is available as html at https://codepo8.github.io/hosting-on-github-template/markdown or https://codepo8.github.io/hosting-on-github-template/markdown.html. 



The issue there is that you might not be happy with the out-of-the-box rendering of GitHub and especially the listing of the repository name as the main heading. To change it, you can create your own HTML templates. For this to work, you need to create a folder called `_layouts` in your repository and create an HTML document in there. A [bare bones example](https://github.com/codepo8/hosting-on-github-template/blob/main/_layouts/simple.html) called `simple.html` is part of this repository.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>{{ page.title }}</title>
</head>
<body>
    {{ content }}
</body>
</html>
```

The parts surrounded by curly braces are variables. The `{{ page.title }}` will come from a title defined in the markdown's front matter and the `{{ content }}` part means that this is where the content of the markdown file goes. 

In your markdown file you create a front matter section with a title and a template. The title could be whatever you want and will be what displays the `{{ page.title }}` in the template. The template needs to be file name of the HTML template in the `_templates` folder without `.html`.
```markdown
---
title: markdown with template
template: simple
---
# Markdown demo

This markdown file will be shown as HTML

1. Ordered list item 1
1. Ordered list item 2
1. Ordered list item 3

- Unordered list item 1
- Unordered list item 2
- Unordered list item 3

> blockquote 

## Headings

[links](http://example.com)
```

## Advanced: Display colour coded source code

## Demo: showcasing an HTML/CSS/JS example with 

## Tip: Use collections 


