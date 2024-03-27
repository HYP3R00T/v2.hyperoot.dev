---
author: Rajesh
pubDatetime: 2024-03-25 #2024-03-25
title: Export Pip Packages
featured: false
draft: true
tags:
  - python
description: ""
---

Sometimes while I start with a new project, I end up playing around with different external packages which I don't keep track of. To list all the pip packages, we can use `pip list` in the terminal. But

First install `setuptools` using `pip install setuptools`

```python
import pkg_resources

with open('requirements.txt', 'w') as file:
    for package in pkg_resources.working_set:
        file.write(package.project_name + '\\n')
```

Save it with any name and store it in the system environment to easy access
