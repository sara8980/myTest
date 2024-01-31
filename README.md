# my-image

## build 
docker build -t convertor .

## run 
docker run -it --name myContainer -e PDF_Sara -v $PWD/images:/app/images -v $PWD/output:/app/output convertor images output