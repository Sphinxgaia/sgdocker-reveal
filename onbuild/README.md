# L'essentiel pour reveal JS
## by Jérôme Masson


--------


# Onbuild image
- Based on node 6 alpine
- configuration ENV variables:
  - Release version : VERSION 3.6
  - VCS Link : ENV VCS https://github.com
  - VCS User :  GITUSER Sphinxgaia
  - VCS Repository : REPO my_reveal
  - tar.gz release sha1num : sha1 d03f677b3e7e584dc38f598f6847c0c8f52f679a

## Default reveal.js configuration :
  - slideNumber
  - history
  - markdown support
  - zoom support
  - note support
  - highlight support
  - title_footer plugin added

## Usage :

- You must have a copy of your `Slides` folder and `index.html` in `my_folder before` build `my_image_name`

~~~bash
mkdir my_folder && cd my_folder
touch Dockerfile
echo "FROM Sphinxgaia:3.6-onbuild" > Dockerfile
docker build -t my_image_name .
~~~
