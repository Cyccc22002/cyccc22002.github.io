# CyCCC 22-002 Blog Site [![GitHub license](https://img.shields.io/github/license/cotes2020/chirpy-starter.svg?color=blue)][mit]

#### PREFACE
This public repo is used to host the Cyber Captians Career Course Blog site. This does not represent the Army in any way.<br />
The posts and information herein are the thoughts and opinions of the originating contributor. 

## Making Changes and Contributing

### Install Dependencies

```bash
sudo apt update
sudo apt install ruby-full build-essential zlib1g-dev git
```
To avoid installing RubyGems packages as the root user:

```bash
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```
Install Jekyll bundler: 

```bash
gem install jekyll bundler
```

### Pull repo and create branch

this step just gets you onto a branch of code to make all changes and avoid flooding the master branch with commits.<br />
(do as I say not as I do, built in an environment without access to serve site locally)

```bash
git clone https://github.com/Cyccc22002/cyccc22002.github.io.git
git checkout -b <intuitive-branch-name>
bundle
``` 

### Serve site locally to test changes

```bash 
bundle exec jekyll s
```
Give it some time and the site will be available locally.<br />
The site works with live updates, change and save the files in the repo and they will update automatically on your local deployment.<br />
If it does not automatically update, refresh your browser. <br />

Make changes to files and push them to your branch. <br />
You will most likely need to build a [**personal access token**](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) to do this.<br />

```bash
git config --local credential.helper store
git add .
git commit -m "made some changes"
git push
```

### Create/Merge - Merge Request

Once you have completed all the changes you would like to do, create a MR with your branch as source and master (main) and target. <br />
After that you can merge your branch and squash commits into one, creating an overall description commit of changes. 

### Site CI/CD

The site has a GitHub action that will re-bundle and serve based on commits to master (main). <br />
Check the site after the action has completed to ensure expected changes have completed. 

## Posts and Jekyll/Chirpy Guidance

This site is based on the theme Chirpy created by [***cotes2020***](https://github.com/cotes2020).<br /> 
Instructions and help can be found on the [***Chirpy repo page***](https://github.com/cotes2020/jekyll-theme-chirpy)<br />

[***TechnoTim***](https://github.com/techno-tim) also has great information and guidance on developing, deploying, and updating the [***site on his docs page***](https://docs.technotim.live/posts/jekyll-docs-site/).<br />
(also hosted with the Chirpy theme) <br />

Posts have a specific amount of metadata needed to help format the post in relation to the rest of the posts, including tags and such. <br />
Look in the `_posts` folder for examples. 


