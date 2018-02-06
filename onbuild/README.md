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
  - tar.gz release sha512num : sha512 262eb03cc755d03449f827ff66b382bd21f83a25742b69a3b55455985853338c87a663e4b225ab402fee3ea61968d0fa8759b6536182c79782c9d5a2e98f83a9

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
