# Imagebuilder  

Imagebuilder for GL.iNet devices. The Image Builder (previously called the Image Generator) is a pre-compiled environment suitable for creating custom images without the need for compiling them from source.  

## System Requirement  

- x86_64 platform  
- ubuntu or other linux  
- You need to install necessary software  

```bash  
$ sudo apt-get update
$ sudo apt-get install subversion build-essential git-core libncurses5-dev zlib1g-dev gawk flex quilt libssl-dev xsltproc libxml-parser-perl mercurial bzr ecj cvs unzip git wget
```  

## How to use it  

It's easy to generate an image by issueing *gl_image* script. It will generate all GL.iNet's devices, and you can specify the target image to build with **-d** option. Issueing *gl_image --help* to see more details.  

## Configuration  

Here is a brief description for images.json configuration file.  

- version: The **version** variable will generate a verison file into **/etc/glversion** and override **/etc/opk/distfeeds.conf** with the version number.  
- profiles: A list of devices that you prefer to build, you can issue *make info* to see all available device.  
- packages: The **default** option is a list of packages to embed into the image which is specified in **profiles** variable. It also supports an option name after **profile** that will overlay in **default** packages.  

