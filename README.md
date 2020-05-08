# aax-to-mp3
Simple dockerized Node.js web service for converting an AAX file into an MP3 file.

## Usage
Install [Docker](https://www.docker.com/), then run:
```
$ docker run -d --rm -p 8082:8081 -p 8087:8087 -v $HOME/tmp:/tmp -e MAX_FILE_SIZE=$(expr 1 \* 1024 \* 1024 \* 1024) bartt/aax-to-mp3 aax-to-mp3
```
Then fire up http://localhost:8082/ in your browser.

![Usage example](https://user-images.githubusercontent.com/837775/64194974-a7ed6700-ce80-11e9-8f7d-63fa09c1fafc.png)

Select your AAX file and click `Convert`. The whole conversion should take 5-10 minutes.

The MP3 file will be downloaded when processing is complete.

## Manual installation
Install [Docker](https://www.docker.com/), then build the image yourself:
```
$ git clone git@github.com:bartt/aax-to-mp3
$ cd aax-to-mp3
$ docker build -t bartt/aax-to-mp3 .
```
