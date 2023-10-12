---
title: "Download from Google Cloud Storage using gsutil from singularity container"
date: 2023-10-12T10:06:41+02:00
draft: false
type: "post"
tags: ["googlecloud", "docker", "singularity", "gsutil"]
---
## Introduction
Downloading files from Google Cloud Storage (GCS) using `gsutil` from a singularity container can be tricky. In this blog post, I will show you how to do it.

## Prerequisites
- Singularity installed on your computer
- A Google Cloud Storage bucket with the files you want to download

## Step 1: Create a singularity container
First, we need to create a singularity container with `gsutil` installed. There are docker images available for `gsutil` on [Docker Hub](https://hub.docker.com/r/google/cloud-sdk/). We can use one of them to create our singularity container.

```bash
singularity pull docker://google/cloud-sdk
```

## Step 2: Download files from Google Cloud Storage
Now that we have our singularity container, we can use it to download files from Google Cloud Storage. To do so, we need to run the following command:

```bash
singularity exec cloud-sdk_latest.sif gsutil -m cp -r gs://my_bucket/my_folder .
```
or

```bash
singularity shell -B /path/to/my/folder cloud-sdk_latest.sif
gsutil -m cp -r gs://my_bucket/my_folder .
```

## Conclusion
I hope this blog post was helpful. If you have any questions, please feel free to connect with me on [LinkedIn](https://www.linkedin.com/in/nagarna/).
