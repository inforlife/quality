# Documentation Template

Provides a consistent starting point for building InfoRLife [Jekyll](https://jekyllrb.com/)-based documentation websites.

## Usage
Follow the steps below to create a new documentation website.

### Copy this repo
[Create a new repo on GitHub](https://github.com/new) and then 

```
git clone https://github.com/inforlife/documentation-template <NEW SITE NAME>
cd <NEW SITE NAME>
git remote set-url origin https://github.com/inforlife/<NEW SITE NAME>
git remote add upstream https://github.com/inforlife/<NEW SITE NAME>
git push origin master
git push --all

```

### Add content
- Update `./_config.yml` with site related info.
- Create static pages, see `./example_page.md`.
- Replace `./README.md` with one including project related information.
- Commit the changes.

```
git add .
git commit -m "add documentation content" 
```

**The documentation site is available at http://inforlife.github.io/NEW-SITE-NAME/**

## Credits

The template is based on [DOCter](https://github.com/cfpb/docter/) from [CFPB](http://cfpb.github.io/).
