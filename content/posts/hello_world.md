---
title: "Hello HUGO Gokarna world !"
date: 2023-06-15T18:35:56+02:00
draft: false
type: "post"
tags: ["hugo", "gokarna", "website", "blog", "hello world"]
---

Welcome to my new website where I will be sharing my thoughts on bioinformatics, data science, and other topics that interest me. I hope you will find it enjoyable!

## Creating a website with Hugo and Gokarna theme

To kick things off, I thought I'd share how I built this website using (Hugo)[https://gohugo.io/] and (Gokarna)[https://gokarna-hugo.netlify.app/] theme. It all started when I stumbled upon a GitHub page with the Gokarna theme, and was immediately drawn to its simplicity and beauty. Intrigued, I began researching how to use Hugo and eventually built this website.

### Install Hugo on your computer

I have installed Hugo on my Mac using the [homebrew](https://brew.sh/) package manager. You can find the instructions [here](https://gohugo.io/getting-started/installing/).

```bash
brew install hugo
```

### Create a new website with Hugo

Create a new website with Hugo is very simple. You just need to run the following command:

```bash
hugo new site my_website
```

### Add a theme - Gokarna

You can find a lot of themes on the [Hugo website](https://themes.gohugo.io/). I have chosen the [Gokarna](https://gokarna-hugo.netlify.app/) theme. To add it to your website, you just need to run the following command:

```bash
cd my_website
git init
git submodule add https://github.com/526avijitgupta/gokarna.git themes/gokarna
```

### Edit the config file

You can edit the config file (`hugo.toml`) to change the name of your website, the language, the theme, etc. You can find more information [here](https://gokarna-hugo.netlify.app/posts/theme-documentation-basics/#basic-configuration).


### Add a new post

To add a new post, you just need to run the following command:

```bash
hugo new _index.md
hugo new posts/hello_world.md
```

And then you can edit the file `content/_index.md` or `content/posts/hello_world.md` to write your post. By default, the post is a draft. If you want to publish it, you need to change the `draft` parameter to `false` in the files' header.

Images can be added in the `static` folder. For example, you can add a picture of yourself in the `static` folder and then add the following line in the `content/index.md` file:

```
![ME](/1172052.png)
```

### Deploy your website locally

If you want to see what it looks like, you can run the following command:

```bash
hugo server -D
```
Don't forget to add the `-D` option to see the draft posts.

### Deploy your website on GitHub via GitHub actions

Commit the changes and create a GitHub actions workflow based on the steps described [here](https://gohugo.io/hosting-and-deployment/hosting-on-github/). Once the workflow is complete,the website will be up and running in no time...! 

