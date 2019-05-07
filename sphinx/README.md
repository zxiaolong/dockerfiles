## build sphinx image
docker build . -t bionic-sphinx:latest

## build document
### prepare sphinx source
mkdir -p /tmp/sphinx/source
cp *.rst /tmp/sphinx/source

### build
docker-compose up bionic-sphinx

### document output
/tmp/sphinx/build/latex/*.pdf
/tmp/sphinx/build/html/*.*
