
## eicac.github.io (eicac-website)

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

To develop:
```
npm run dev
```

To build:
```
npm run build
```

To deploy:
```
npm run deploy
```

To open this repository in Visual Studio Code on Linux:
```
cd eicac-website
code .
```

To commit and push updates to GitHub (this saves the source code for the website. It does NOT deploy the website, you need to run `npm run deploy` for that):
```
git add .
git commit -m "update website"
git push
```

To commit, push, and deploy all in one, use this utility script instead:
```
./tools/save-and-deploy.sh
```
