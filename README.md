This tutorial introduces the basics of writing a RESTful web service API with Go and the Gin Web Framework (Gin).

You’ll get the most out of this tutorial if you have a basic familiarity with Go and its tooling. If this is your first exposure to Go, please see Tutorial: Get started with Go for a quick introduction.
# Getting Started
```
git clone https://github.com/deepakmardii/go-API
```
Next:
```
cd go-API
```
Install Gin:
```
go get github.com/gin-gonic/gin
```
From the command line in the directory containing main.go, run the code:
```
go run .
```
From a new command line window, use curl to make a GET request to your running web service.
### GET Method
``` 
curl http://localhost:8080/albums
```
or
```
curl http://localhost:8080/albums \
    --header "Content-Type: application/json" \
    --request "GET"
```
### POST Method
```
curl http://localhost:8080/albums \
    --include \
    --header "Content-Type: application/json" \
    --request "POST" \
    --data '{"id": "4","title": "The Modern Sound of Betty Carter","artist": "Betty Carter","price": 49.99}'
```
### GET /albums/[id] Method
```
curl http://localhost:8080/albums/2
```
