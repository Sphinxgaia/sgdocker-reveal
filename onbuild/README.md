# Docker images for reveal.js

# reveal.js based on :
- https://github.com/Sphinxgaia/my_reveal

# Alpine for lighter image
- Based on node 6 alpine
- configuration ENV variables:
  - Release version : VERSION 3.6
  - VCS Link : ENV VCS https://github.com
  - VCS User :  GITUSER Sphinxgaia
  - VCS Repository : REPO my_reveal

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

# Onbuild image
- Based on node 6 alpine
- configuration ENV variables:
  - Release version : VERSION 3.6
  - VCS Link : ENV VCS https://github.com
  - VCS User :  GITUSER Sphinxgaia
  - VCS Repository : REPO my_reveal

## Default reveal.js configuration :
  - slideNumber
  - history
  - markdown support
  - zoom support
  - note support
  - highlight support
  - title_footer plugin added

## Usage :

- You have to copy your Slides and index.html folder in my folder before build "my_image_name"

~~~bash
mkdir my_folder && cd my_folder
touch Dockerfile
echo "FROM sphinxgaia/sgdocker-reveal:3.6-onbuild" > Dockerfile
docker build -t my_image_name .
~~~
