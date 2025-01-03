
## eicac.github.io (eicac-website)

**This repository is set up with GitHub Actions to immediately update the live website when a push is received on the `main` branch**

### Basic Website Modification Instructions (no local installation needed)

Use these instructions if the only website edits you are making are:

- modifying menus and the home page by editing `hugo.yaml`
- creation of new pages in `content/`
- addition of static assets like images in `assets/images`

All you need to do for simple modifications is add or edit files with the GitHub interface. Commit the changes to the `main` branch, and deployment will immediately trigger via GitHub Actions, updating the live website.

### Advanced Website Modifications

Use these instructions if you need to make more complex website modifications beyond what is listed above.

Before anything else, make sure you have a working version of NodeJS and npm.

Install Hugo (`https://gohugo.io/installation/`). The easiest way on Linux is:

```
sudo snap install hugo
```

Clone this repository, then run the other commands to install dependencies:

```
git clone git@github.com:eicac/eicac.github.io.git eicac-website
cd eicac-website
git submodule update --init --recursive
npm install
```

To pull the latest updates (In case someone else was working on the website):
```
git pull
```

To develop locally:
```
npm run dev
```

To build with Hugo:
```
npm run build
```

To open this repository in Visual Studio Code on Linux:
```
cd eicac-website
code .
```

To commit and push updates to GitHub:
```
git add .
git commit -m "update website"
git push
```

To commit and push all in one, use this utility script instead:
```
./tools/commit-and-push.sh
```

If you need to commit work but do not want it to go live on the website, commit it to a separate branch.
