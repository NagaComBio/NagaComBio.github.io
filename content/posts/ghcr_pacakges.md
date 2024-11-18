---
title: "Ghcr_pacakges"
date: 2024-11-18T21:21:23+01:00
draft: false
type: "post"
tags: ["ghcr", "docker", "singularity"]
---

# How to Upload a Singularity Image to GitHub Container Registry (ghcr.io)

Publishing a Singularity image to GitHub Container Registry (ghcr.io) can be quick and easy! Follow these **three simple steps** to get your locally created image uploaded and ready to share.

---

## **Step 1: Create Your Singularity Image**

First, you need to build your Singularity image using an Apptainer installation. Whether you're working on an HPC or your personal computer, you can create an image from a definition file with this command:

```bash
singularity build example.sif example.def
```
Make sure your .def file is properly configured for your application needs!


## **Step 2: Log In to GitHub Container Registry**

Next, authenticate with GitHub Container Registry using Apptainer's remote login. 
You'll need:
- Your GitHub username
- A classic GitHub personal access token with read and write permissions for package management

Run the following command to log in:
```
apptainer remote login --username github_username oras://ghcr.io

```
| Pro Tip: Keep your token secure and ensure it has the necessary permissions to avoid login issues.

## **Step 3: Push Your Image to ghcr.io**

Now it's time to push your image! While doing so, you can add a tag for better version control. 

Use this command:
```
singularity push example.sif oras://ghcr.io/github_username:latest
```

## **Make Your Image Public**

By default, images uploaded to ghcr.io are private. To share your image with others, adjust the package visibility in your GitHub settings to make it public.