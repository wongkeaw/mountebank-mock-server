# README #
start mountebank :mb
deploy mock data :mb --configfile imposters.ejs --allowInjection

docker build -t mock-server:1.0 .
docker run -p 2525:2525 -p 9005:9005 -p 9006:9006 -p 9007:9007 -p 9008:9008 -p 9009:9009 -p 9010:9010 mock-server:1.0