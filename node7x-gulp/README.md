This Docker file will use Ubuntu base image and installs node7x, gulp, bower and gulp-sass packages and exposes /opt folder.

How to use this image for building/running angularjs/legacy javascript applications.

Usage: Map the UI source folder as volume mount and install npm / bower packages. Then run the application.

docker run --rm -v ~/hostfolder:/opt yogeshl/node7x-gulp npm install

docker run --rm -v ~/hostfolder:/opt yogeshl/node7x-gulp bower install

docker run --rm -p 3000:3000 -v ~/hostfolder:/opt yogeshl/node7x-gulp npm run build

Note: If using Windows OS, change ~/hostfolder to c:/foldername format