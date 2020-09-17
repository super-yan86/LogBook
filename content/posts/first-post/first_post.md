---
title: "First_post"
date: 2020-09-16T20:39:49+08:00
lightgallery: true
author: "YC"
resources:
- name: "first-post"
  src: "first-post.png"

tags: ["Markdown"]
categories: ["Markdown"]  
---


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