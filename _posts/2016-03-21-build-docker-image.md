---
layout: post
section-type: post
title: How to build a docker image
category: tech
tags: [ 'tutorial', 'docker' ]
---

First of all you must to create a <a href="https://docs.docker.com/engine/reference/builder/" target="\_blank">Dockerfile</a> 
for your image, in a nutshell a Dockerfile is a guideline 
that sais to docker hub what it have todo, which are the steps and hoy it have to execute it.

To upload an image to official docker hub repository you must to have an account, is free and you can link
with your github whether you want.

Once you have the Dockerfile and your docker account you must to follow this steps:

## 1. Login in your docker hub account

<code data-trim class="bash">
docker login --username="your_username" --email="your_email"
</code>

Once logged the promt ask you for your account password.

## 2. Build your image in your local machine

You have to create the image, for that you have to execute the next command

<code data-trim class="bash">
docker build --tag="your_image_name" .
</code>

Depends of the size of your image, the creation could be during some time.

## 3. Upload the image to docker hub repository

Once the image has been built it has been uploaded to docker hub repository, first you have to get 
the image name

<code data-trim class="bash">
docker images
<code>

You should look something like this


ubuntu                                  14.04               97434d46f197        2 days ago          188 MB

When you know the name of the image you have to upload it

<code data-trim class="bash">
docker push "your_image_name"
<code>






