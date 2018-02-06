# L'essentiel pour reveal JS
## by Jérôme Masson


--------


# Alpine for lighter image
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

~~~bash
export pwd=/path/directory

docker run -d -v $pwd/index.html:/reveal.js/index.html \
      -v $pwd/Slides/Cours:/reveal.js/Slides/Cours \
      -v $pwd/Slides/themes:/reveal.js/Slides/themes \
      -v $pwd/Slides/Img:/reveal.js/Slides/Img \
      -p 8080:8000 \
      Sphinxgaia/sgdocker-reveal
~~~
