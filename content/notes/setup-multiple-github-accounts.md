---
author: "Balaji Vijayn"
title: "How to Setup Multiple Github Accounts"
date: "2023-05-13"
tags: ["git"]
ShowToc: false
---

### Generate Private and Public Keys

Generate the public and private key with email id as unique identifier and provide the name for the key file using '-f'

```
ssh-keygen -t rsa -C "emailId" -f "github-balajivijayan"
```

- Add the generated public key to the GITHUB account
- Checkout the Repo to local machine

```
git checkout git@github.com:balajivijayan/balajivijayan.github.io.git
```

Apply the Email used to generate the public key as local config in the same folder as the checked out git repo
```
$ git config user.email "<emailId>"
$ git config user.name "<emailId>"
```

Override the Github Origin 

```
git remote add origin git@github.com:balajivijayan/balajivijayan.github.io.git
git remote set-url origin git@github.com:balajivijayan/balajivijayan.github.io.git balajivijayan.github.io
```