# aspNetCoreAngular2

heroku create --buildpack http://github.com/noliar/dotnet-buildpack.git
git push heroku master
heroku auth:token

heroku create
heroku config:add BUILDPACK_URL=https://github.com/friism/heroku-buildpack-mono/
git push heroku master

dotnet run --environment Production --port 5123
 --server.urls=http://localhost:60000;http://localhost:60001;

heroku config:set ASPNETCORE_SERVER.URLS=http://localhost:12541/
