# my-image

## build 
docker build -t convertor .

## run 
docker run -it --name myContainer --rm -e PDF_NAME=PDF_Sara -v $PWD/images:/app/images -v $PWD/output:/app/output convertor images output