---
title: "How to build my hugo file"
date: 2023-08-10T22:56:45+09:00
---

# 1) Delete 'public' folder 
![](/images/1.png)

if 'Already exists in the index~' error occured, should delete caches in your directory.   
<br/>  

open git bash!  
```
git rm --cached [my hugo project folder]
``` 


# 2) Open 'git bash'  
#
# 3) Go to my hugo project folder   
use "cd" command   
#
# 4) link with my repository

```
git init
git remote add origin <my github repository(for build) url>
```

# 5) my github.io respository should be submodule.
```
git submodule add -b master <user.github.io repository url> public
```

# 6) Let's build
```
hugo -t <theme name>
```
then, you can see the files in public folder in your project directory

# 7) push files
```
$ cd public
$ git add .
$ git commit -m "<commit message>"
$ git push origin master
$ cd ..
$ git add .
$ git commit -m "<commit message>"
$ git push origin master
```