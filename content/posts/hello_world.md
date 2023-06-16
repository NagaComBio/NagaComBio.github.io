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

### Step 1: Install Hugo on your computer

I have installed Hugo on my Mac using the [homebrew](https://brew.sh/) package manager. You can find the instructions [here](https://gohugo.io/getting-started/installing/).

```bash
brew install hugo
```

### Step 2: Create a new website with Hugo

Create a new website with Hugo is very simple. You just need to run the following command:

```bash
hugo new site my_website
```

### Step 3: Add a theme - Gokarna

You can find a lot of themes on the [Hugo website](https://themes.gohugo.io/). I have chosen the [Gokarna](https://gokarna-hugo.netlify.app/) theme. To add it to your website, you just need to run the following command:

```bash
cd my_website
git init
git submodule add https://github.com/526avijitgupta/gokarna.git themes/gokarna
```

### Step 4: Edit the config file

You can edit the config file (`hugo.toml`) to change the name of your website, the language, the theme, etc. You can find more information [here](https://gokarna-hugo.netlify.app/posts/theme-documentation-basics/#basic-configuration).


### Step 5: Add a new post

To add a new post, you just need to run the following command:

```bash
hugo new _index.md
hugo new posts/hello_world.md
```

And then you can edit the file `content/_index.md` which will be the main landing page or `content/posts/hello_world.md` to write your first blog post. By default, the markdowns are drafts. If you want to publish it, you need to change the `draft` parameter to `false` in the files' header.

Images can be added in the `static` folder. For example, you can add a picture of yourself in the `static` folder and then add the following line in the `content/_index.md` file:

```
![ME](/1172052.png)
```

### Step 6: Deploy your website locally

If you want to see what it looks like, you can run the following command:

```bash
hugo server -D
```
Don't forget to add the `-D` option to see the draft posts.

### Step 7: Export your website as a local static website

If you want to export your website as a local static website, you can run the following command:

```bash
hugo
```
This will create a `public` folder with all the files you need to deploy your website. If you have local server, you can copy the `public` folder to your server. This could be also a good way to test your website before deploying it on GitHub.

### Step 8: Deploy your website on GitHub via GitHub actions

Commit the changes and create a GitHub actions workflow based on the steps described [here](https://gohugo.io/hosting-and-deployment/hosting-on-github/). Once the workflow is complete, the website will be up and running in no time...! 

