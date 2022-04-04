# MongoDB install setup https://www.youtube.com/watch?v=4crXgQZG4W8

## through homebrew
- `brew tap mongodb/brew`
- `brew install mongodb-community`

## create database folder for mongo (-p means private)
- `sudo mkdir -p /System/Volumes/Data/data/db`

## permissions to use above folder
- `sudo chown -R `id -un` /System/Volumes/Data/data/db`

## launch from folder path
- `sudo mongod --dbpath /System/Volumes/Data/data/db`
- keep open in this terminal
- `crtl c` to close


## Install Compass desktop app
- `brew install --cask mongodb-compass`


## start mongo... not sure these?
- `brew services start mongodb/brew/mongodb-community`
- `mongod --config`