# DOC SCAFFOLD

Provides a consistent starting point for building ACS Dobfar Info [Jekyll](https://jekyllrb.com/)-based documentation websites.

## Usage
Follow the steps below to create a new documentation website.

### Copy this repo

- [Create a new repo on GitHub](https://github.com/new).

- Clone this repo into the newly created repo. 

```
git clone git@github.com:acsinfo/doc-scaffold.git new-repo
```

- Edit the git config file replacing the origin URL with your new URL.

```
cd new-repo
$ atom .git/config
[remote "origin"]
    fetch = +refs/heads/*:refs/remotes/origin/*
    url = git@github.com:acsinfo/new-repo.git
```

- Push the repo up to GitHub 

``` 
git push -u origin master
```

### Add content
- Update `./_config.yml` with site related info.

- Create static pages, see `./example_page.md`.

- Replace `./README.md` with one including project related information.

- Build the static site.

```
cd new-repo
$ jekyll build
```

- Commit the changes.

```
git add .
git commit -m "add documentation content" 
```

### Setup Github pages
- Make sure git knows about the subtree (the subfolder with your site). 

```
git add -f _site
git commit -m "initial _site subtree commit"
```

- Push the repo up to GitHub 

```
git subtree push --prefix _site origin gh-pages
```


**The documentation site is now available at http://acsinfo.github.io/new-repo/**

### Configure custom domain

- Add `CNAME` file to `./_site` folder containing the custom domain. 

``` 
new-repo.acsinfo.ch
```

- Create a CNAME record. [help.github.com](https://help.github.com/articles/tips-for-configuring-a-cname-record-with-your-dns-provider/)

```
new-repo.acsinfo.ch CNAME   acsinfo.github.io
```
**The documentation site is now available at http://new-repo.acsinfo.ch/**



**Don't forget to push up to GitHub also the `master` branch.**

## Credits

The scaffold is based on [DOCter](https://github.com/cfpb/docter/) from [CFPB](http://cfpb.github.io/).
