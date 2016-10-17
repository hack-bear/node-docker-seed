## Dev image:

```
cd api
docker build -t benben/node-web-app .
docker run -p 49160:8080 -d benben/node-web-app
```

## Prod image:

```
cd docker
docker build -t benben/node-dev .
cd ../api
docker run  \
  -d \
  --name "dev-server" \
  -p 49160:8080 \
  -e "APP=index.js" \
  -e "NODE_ENV=development" \
  -v $(pwd):/var/www/example.com/api \
  benben/node-dev;
```
