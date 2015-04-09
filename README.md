```
git checkout -b gh-pages
git rm -rf .
git commit -am "First commit to gh-pages branch"
git push origin gh-pages
```

Now, we will use a git-subtree technique to push the build or output content to the gh-pages branch:

```
git checkout master
git push origin `git subtree split --prefix _book gh-pages`:gh-pages --force
```

Finally, you will need to run the following line every time you want to update your site/blog!

```
git subtree push --prefix _book origin gh-pages
```
