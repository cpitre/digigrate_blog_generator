## Commands used to create, version control and publish a Hexo based blogging site:

### Initialize the blog site (digigrate_blog) using the hexo CLI:
```
$ hexo init digigrate_blog
INFO  Cloning hexo-starter https://github.com/hexojs/hexo-starter.git
Submodule 'themes/landscape' (https://github.com/hexojs/hexo-theme-landscape.git) registered for path 'themes/landscape'
Cloning into '/Users/cpitre/git/hexo/digigrate_blog/themes/landscape'...
remote: Enumerating objects: 733, done.
remote: Counting objects: 100% (733/733), done.
remote: Compressing objects: 100% (288/288), done.
remote: Total 663 (delta 415), reused 607 (delta 360), pack-reused 0
Receiving objects: 100% (663/663), 684.33 KiB | 285.00 KiB/s, done.
Resolving deltas: 100% (415/415), completed with 49 local objects.
From https://github.com/hexojs/hexo-theme-landscape
 * branch            73a23c51f8487cfcd7c6deec96ccc7543960d350 -> FETCH_HEAD
Submodule path 'themes/landscape': checked out '73a23c51f8487cfcd7c6deec96ccc7543960d350'
INFO  Install dependencies
added 185 packages from 430 contributors and audited 191 packages in 21.194s

14 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities

INFO  Start blogging with Hexo!
```

### Change into the newly created blog site's directory (digigrate_blog):
```
$ cd digigrate_blog
```

### List the newly created blog site's directory content:
```
$ ls -lsa
total 136
  0 drwxr-xr-x   10 cpitre  staff    320 Nov  1 14:55 .
  0 drwxr-xr-x    6 cpitre  staff    192 Nov  1 14:54 ..
  8 -rw-r--r--    1 cpitre  staff     65 Nov  1 14:54 .gitignore
  8 -rw-r--r--    1 cpitre  staff   2439 Nov  1 14:54 _config.yml
  0 drwxr-xr-x  164 cpitre  staff   5248 Nov  1 14:55 node_modules
112 -rw-r--r--    1 cpitre  staff  55618 Nov  1 14:55 package-lock.json
  8 -rw-r--r--    1 cpitre  staff    577 Nov  1 14:54 package.json
  0 drwxr-xr-x    5 cpitre  staff    160 Nov  1 14:54 scaffolds
  0 drwxr-xr-x    3 cpitre  staff     96 Nov  1 14:54 source
  0 drwxr-xr-x    3 cpitre  staff     96 Nov  1 14:54 themes
```

### Using the git command, initialize the blog site's directory content for source control:
```
$ git init
Initialized empty Git repository in /Users/cpitre/git/hexo/digigrate_blog/.git/
```

### List the blog site's directory content (notice the .git folder):
```
$ ls -lsa
total 136
  0 drwxr-xr-x   11 cpitre  staff    352 Nov  1 14:56 .
  0 drwxr-xr-x    6 cpitre  staff    192 Nov  1 14:54 ..
  0 drwxr-xr-x    9 cpitre  staff    288 Nov  1 14:56 .git
  8 -rw-r--r--    1 cpitre  staff     65 Nov  1 14:54 .gitignore
  8 -rw-r--r--    1 cpitre  staff   2439 Nov  1 14:54 _config.yml
  0 drwxr-xr-x  164 cpitre  staff   5248 Nov  1 14:55 node_modules
112 -rw-r--r--    1 cpitre  staff  55618 Nov  1 14:55 package-lock.json
  8 -rw-r--r--    1 cpitre  staff    577 Nov  1 14:54 package.json
  0 drwxr-xr-x    5 cpitre  staff    160 Nov  1 14:54 scaffolds
  0 drwxr-xr-x    3 cpitre  staff     96 Nov  1 14:54 source
  0 drwxr-xr-x    3 cpitre  staff     96 Nov  1 14:54 themes
```

### Check the status of the directory content against git:
```
$ git status
On branch master

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        .gitignore
        _config.yml
        package-lock.json
        package.json
        scaffolds/
        source/
        themes/

nothing added to commit but untracked files present (use "git add" to track)
```

### Add the blog site's directory content into the git's stage:
```
$ git add .gitignore _config.yml package-lock.json package.json scaffolds/ source/ themes/
```

### After the git add command, check the git workspace status:
```
$ git status
On branch master

Initial commit

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

        new file:   .gitignore
        new file:   _config.yml
        new file:   package-lock.json
        new file:   package.json
        new file:   scaffolds/draft.md
        new file:   scaffolds/page.md
        new file:   scaffolds/post.md
        new file:   source/_posts/hello-world.md
        new file:   themes/landscape/.gitignore
        new file:   themes/landscape/Gruntfile.js
        new file:   themes/landscape/LICENSE
        new file:   themes/landscape/README.md
        new file:   themes/landscape/_config.yml
        new file:   themes/landscape/languages/de.yml
        new file:   themes/landscape/languages/default.yml
        new file:   themes/landscape/languages/es.yml
        new file:   themes/landscape/languages/fr.yml
        new file:   themes/landscape/languages/ja.yml
        new file:   themes/landscape/languages/ko.yml
        new file:   themes/landscape/languages/nl.yml
        new file:   themes/landscape/languages/no.yml
        new file:   themes/landscape/languages/pt.yml
        new file:   themes/landscape/languages/ru.yml
        new file:   themes/landscape/languages/zh-CN.yml
        new file:   themes/landscape/languages/zh-TW.yml
        new file:   themes/landscape/layout/_partial/after-footer.ejs
        new file:   themes/landscape/layout/_partial/archive-post.ejs
        new file:   themes/landscape/layout/_partial/archive.ejs
        new file:   themes/landscape/layout/_partial/article.ejs
        new file:   themes/landscape/layout/_partial/footer.ejs
        new file:   themes/landscape/layout/_partial/gauges-analytics.ejs
        new file:   themes/landscape/layout/_partial/google-analytics.ejs
        new file:   themes/landscape/layout/_partial/head.ejs
        new file:   themes/landscape/layout/_partial/header.ejs
        new file:   themes/landscape/layout/_partial/mobile-nav.ejs
        new file:   themes/landscape/layout/_partial/post/category.ejs
        new file:   themes/landscape/layout/_partial/post/date.ejs
        new file:   themes/landscape/layout/_partial/post/gallery.ejs
        new file:   themes/landscape/layout/_partial/post/nav.ejs
        new file:   themes/landscape/layout/_partial/post/tag.ejs
        new file:   themes/landscape/layout/_partial/post/title.ejs
        new file:   themes/landscape/layout/_partial/sidebar.ejs
        new file:   themes/landscape/layout/_widget/archive.ejs
        new file:   themes/landscape/layout/_widget/category.ejs
        new file:   themes/landscape/layout/_widget/recent_posts.ejs
        new file:   themes/landscape/layout/_widget/tag.ejs
        new file:   themes/landscape/layout/_widget/tagcloud.ejs
        new file:   themes/landscape/layout/archive.ejs
        new file:   themes/landscape/layout/category.ejs
        new file:   themes/landscape/layout/index.ejs
        new file:   themes/landscape/layout/layout.ejs
        new file:   themes/landscape/layout/page.ejs
        new file:   themes/landscape/layout/post.ejs
        new file:   themes/landscape/layout/tag.ejs
        new file:   themes/landscape/package.json
        new file:   themes/landscape/scripts/fancybox.js
        new file:   themes/landscape/source/css/_extend.styl
        new file:   themes/landscape/source/css/_partial/archive.styl
        new file:   themes/landscape/source/css/_partial/article.styl
        new file:   themes/landscape/source/css/_partial/comment.styl
        new file:   themes/landscape/source/css/_partial/footer.styl
        new file:   themes/landscape/source/css/_partial/header.styl
        new file:   themes/landscape/source/css/_partial/highlight.styl
        new file:   themes/landscape/source/css/_partial/mobile.styl
        new file:   themes/landscape/source/css/_partial/sidebar-aside.styl
        new file:   themes/landscape/source/css/_partial/sidebar-bottom.styl
        new file:   themes/landscape/source/css/_partial/sidebar.styl
        new file:   themes/landscape/source/css/_util/grid.styl
        new file:   themes/landscape/source/css/_util/mixin.styl
        new file:   themes/landscape/source/css/_variables.styl
        new file:   themes/landscape/source/css/fonts/FontAwesome.otf
        new file:   themes/landscape/source/css/fonts/fontawesome-webfont.eot
        new file:   themes/landscape/source/css/fonts/fontawesome-webfont.svg
        new file:   themes/landscape/source/css/fonts/fontawesome-webfont.ttf
        new file:   themes/landscape/source/css/fonts/fontawesome-webfont.woff
        new file:   themes/landscape/source/css/images/banner.jpg
        new file:   themes/landscape/source/css/style.styl
        new file:   themes/landscape/source/fancybox/blank.gif
        new file:   themes/landscape/source/fancybox/fancybox_loading.gif
        new file:   themes/landscape/source/fancybox/fancybox_loading@2x.gif
        new file:   themes/landscape/source/fancybox/fancybox_overlay.png
        new file:   themes/landscape/source/fancybox/fancybox_sprite.png
        new file:   themes/landscape/source/fancybox/fancybox_sprite@2x.png
        new file:   themes/landscape/source/fancybox/helpers/fancybox_buttons.png
        new file:   themes/landscape/source/fancybox/helpers/jquery.fancybox-buttons.css
        new file:   themes/landscape/source/fancybox/helpers/jquery.fancybox-buttons.js
        new file:   themes/landscape/source/fancybox/helpers/jquery.fancybox-media.js
        new file:   themes/landscape/source/fancybox/helpers/jquery.fancybox-thumbs.css
        new file:   themes/landscape/source/fancybox/helpers/jquery.fancybox-thumbs.js
        new file:   themes/landscape/source/fancybox/jquery.fancybox.css
        new file:   themes/landscape/source/fancybox/jquery.fancybox.js
        new file:   themes/landscape/source/fancybox/jquery.fancybox.pack.js
        new file:   themes/landscape/source/js/script.js
```

### Commit the git staged workspace contents into the git local repository
```
git commit -m "initial digigrate blog (Hexo)  generator contents"
[master (root-commit) 1e715ef] initial digigrate blog (Hexo)  generator contents
 93 files changed, 7143 insertions(+)
 create mode 100644 .gitignore
 create mode 100644 _config.yml
 create mode 100644 package-lock.json
 create mode 100644 package.json
 create mode 100644 scaffolds/draft.md
 create mode 100644 scaffolds/page.md
 create mode 100644 scaffolds/post.md
 create mode 100644 source/_posts/hello-world.md
 create mode 100644 themes/landscape/.gitignore
 create mode 100644 themes/landscape/Gruntfile.js
 create mode 100644 themes/landscape/LICENSE
 create mode 100644 themes/landscape/README.md
 create mode 100644 themes/landscape/_config.yml
 create mode 100644 themes/landscape/languages/de.yml
 create mode 100644 themes/landscape/languages/default.yml
 create mode 100644 themes/landscape/languages/es.yml
 create mode 100644 themes/landscape/languages/fr.yml
 create mode 100644 themes/landscape/languages/ja.yml
 create mode 100644 themes/landscape/languages/ko.yml
 create mode 100644 themes/landscape/languages/nl.yml
 create mode 100644 themes/landscape/languages/no.yml
 create mode 100644 themes/landscape/languages/pt.yml
 create mode 100644 themes/landscape/languages/ru.yml
 create mode 100644 themes/landscape/languages/zh-CN.yml
 create mode 100644 themes/landscape/languages/zh-TW.yml
 create mode 100644 themes/landscape/layout/_partial/after-footer.ejs
 create mode 100644 themes/landscape/layout/_partial/archive-post.ejs
 create mode 100644 themes/landscape/layout/_partial/archive.ejs
 create mode 100644 themes/landscape/layout/_partial/article.ejs
 create mode 100644 themes/landscape/layout/_partial/footer.ejs
 create mode 100644 themes/landscape/layout/_partial/gauges-analytics.ejs
 create mode 100644 themes/landscape/layout/_partial/google-analytics.ejs
 create mode 100644 themes/landscape/layout/_partial/head.ejs
 create mode 100644 themes/landscape/layout/_partial/header.ejs
 create mode 100644 themes/landscape/layout/_partial/mobile-nav.ejs
 create mode 100644 themes/landscape/layout/_partial/post/category.ejs
 create mode 100644 themes/landscape/layout/_partial/post/date.ejs
 create mode 100644 themes/landscape/layout/_partial/post/gallery.ejs
 create mode 100644 themes/landscape/layout/_partial/post/nav.ejs
 create mode 100644 themes/landscape/layout/_partial/post/tag.ejs
 create mode 100644 themes/landscape/layout/_partial/post/title.ejs
 create mode 100644 themes/landscape/layout/_partial/sidebar.ejs
 create mode 100644 themes/landscape/layout/_widget/archive.ejs
 create mode 100644 themes/landscape/layout/_widget/category.ejs
 create mode 100644 themes/landscape/layout/_widget/recent_posts.ejs
 create mode 100644 themes/landscape/layout/_widget/tag.ejs
 create mode 100644 themes/landscape/layout/_widget/tagcloud.ejs
 create mode 100644 themes/landscape/layout/archive.ejs
 create mode 100644 themes/landscape/layout/category.ejs
 create mode 100644 themes/landscape/layout/index.ejs
 create mode 100644 themes/landscape/layout/layout.ejs
 create mode 100644 themes/landscape/layout/page.ejs
 create mode 100644 themes/landscape/layout/post.ejs
 create mode 100644 themes/landscape/layout/tag.ejs
 create mode 100644 themes/landscape/package.json
 create mode 100644 themes/landscape/scripts/fancybox.js
 create mode 100644 themes/landscape/source/css/_extend.styl
 create mode 100644 themes/landscape/source/css/_partial/archive.styl
 create mode 100644 themes/landscape/source/css/_partial/article.styl
 create mode 100644 themes/landscape/source/css/_partial/comment.styl
 create mode 100644 themes/landscape/source/css/_partial/footer.styl
 create mode 100644 themes/landscape/source/css/_partial/header.styl
 create mode 100644 themes/landscape/source/css/_partial/highlight.styl
 create mode 100644 themes/landscape/source/css/_partial/mobile.styl
 create mode 100644 themes/landscape/source/css/_partial/sidebar-aside.styl
 create mode 100644 themes/landscape/source/css/_partial/sidebar-bottom.styl
 create mode 100644 themes/landscape/source/css/_partial/sidebar.styl
 create mode 100644 themes/landscape/source/css/_util/grid.styl
 create mode 100644 themes/landscape/source/css/_util/mixin.styl
 create mode 100644 themes/landscape/source/css/_variables.styl
 create mode 100644 themes/landscape/source/css/fonts/FontAwesome.otf
 create mode 100644 themes/landscape/source/css/fonts/fontawesome-webfont.eot
 create mode 100644 themes/landscape/source/css/fonts/fontawesome-webfont.svg
 create mode 100644 themes/landscape/source/css/fonts/fontawesome-webfont.ttf
 create mode 100644 themes/landscape/source/css/fonts/fontawesome-webfont.woff
 create mode 100644 themes/landscape/source/css/images/banner.jpg
 create mode 100644 themes/landscape/source/css/style.styl
 create mode 100644 themes/landscape/source/fancybox/blank.gif
 create mode 100644 themes/landscape/source/fancybox/fancybox_loading.gif
 create mode 100644 themes/landscape/source/fancybox/fancybox_loading@2x.gif
 create mode 100644 themes/landscape/source/fancybox/fancybox_overlay.png
 create mode 100644 themes/landscape/source/fancybox/fancybox_sprite.png
 create mode 100644 themes/landscape/source/fancybox/fancybox_sprite@2x.png
 create mode 100644 themes/landscape/source/fancybox/helpers/fancybox_buttons.png
 create mode 100644 themes/landscape/source/fancybox/helpers/jquery.fancybox-buttons.css
 create mode 100644 themes/landscape/source/fancybox/helpers/jquery.fancybox-buttons.js
 create mode 100644 themes/landscape/source/fancybox/helpers/jquery.fancybox-media.js
 create mode 100644 themes/landscape/source/fancybox/helpers/jquery.fancybox-thumbs.css
 create mode 100644 themes/landscape/source/fancybox/helpers/jquery.fancybox-thumbs.js
 create mode 100644 themes/landscape/source/fancybox/jquery.fancybox.css
 create mode 100644 themes/landscape/source/fancybox/jquery.fancybox.js
 create mode 100644 themes/landscape/source/fancybox/jquery.fancybox.pack.js
 create mode 100644 themes/landscape/source/js/script.js
```

### Add and commit this file (./README.md) into the git workpsace/local repository:
```
$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)

        README.md

nothing added to commit but untracked files present (use "git add" to track)

$ git add README.md

$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   README.md

$ git commit -m "added local Hexo blog generator content and Git source control steps"
[master ad48f24] added local Hexo blog generator content and Git source control steps
 1 file changed, 302 insertions(+)
 create mode 100644 README.md
```

### Run Hexo's local web server to check out the created default blog site:
```
$ hexo server
INFO  Validating config
INFO  Start processing
INFO  Hexo is running at http://localhost:4000 . Press Ctrl+C to stop.
(node:7162) Warning: Accessing non-existent property 'lineno' of module exports inside circular dependency
(Use `node --trace-warnings ...` to show where the warning was created)
(node:7162) Warning: Accessing non-existent property 'column' of module exports inside circular dependency
(node:7162) Warning: Accessing non-existent property 'filename' of module exports inside circular dependency
(node:7162) Warning: Accessing non-existent property 'lineno' of module exports inside circular dependency
(node:7162) Warning: Accessing non-existent property 'column' of module exports inside circular dependency
(node:7162) Warning: Accessing non-existent property 'filename' of module exports inside circular dependency
```

### Check for any changes (created by the running of the local Hexo web server) in the local git workspace:
```
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   package.json

no changes added to commit (use "git add" and/or "git commit -a")

$ git diff
diff --git a/package.json b/package.json
index 95866f9..9b85040 100644
--- a/package.json
+++ b/package.json
@@ -9,7 +9,7 @@
     "server": "hexo server"
   },
   "hexo": {
-    "version": ""
+    "version": "5.2.0"
   },
   "dependencies": {
     "hexo": "^5.0.0",
@@ -22,4 +22,4 @@
     "hexo-renderer-stylus": "^2.0.0",
     "hexo-server": "^2.0.0"
   }
-}
+}
\ No newline at end of file

$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   package.json

no changes added to commit (use "git add" and/or "git commit -a")
```

### Add and commit the changed file(s) (./package.json) into the git workpsace/local repository:
```
$ git add package.json

$ git commit -m "package.json file change after the initial 'hexo server' command"
[master 943a657] package.json file change after the initial 'hexo server' command
 1 file changed, 2 insertions(+), 2 deletions(-)
```

### Stop Hexo's local web server (use the CTRL + C keys):
```
INFO  Validating config
INFO  Start processing
INFO  Hexo is running at http://localhost:4000 . Press Ctrl+C to stop.
(node:7162) Warning: Accessing non-existent property 'lineno' of module exports inside circular dependency
(Use `node --trace-warnings ...` to show where the warning was created)
(node:7162) Warning: Accessing non-existent property 'column' of module exports inside circular dependency
(node:7162) Warning: Accessing non-existent property 'filename' of module exports inside circular dependency
(node:7162) Warning: Accessing non-existent property 'lineno' of module exports inside circular dependency
(node:7162) Warning: Accessing non-existent property 'column' of module exports inside circular dependency
(node:7162) Warning: Accessing non-existent property 'filename' of module exports inside circular dependency
^CINFO  Catch you later
```