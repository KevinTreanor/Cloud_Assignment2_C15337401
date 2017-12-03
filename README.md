# Cloud_Assignment2_C15337401
Python file and text document for the assignment

The system is comprised of two worker nodes and a manager. To run the system use the curl commands below:

curl -s -X GET -H 'Accept: application/json' http://localhost:8080/containers | python -mjson.tool

curl -s -X GET -H 'Accept: application/json' http://localhost:8080/containers?state=running | python -mjson.tool

curl -s -X GET -H 'Accept: application/json' http://localhost:8080/images | python -mjson.tool

curl -X POST -H 'Content-Type: application/json' http://localhost:8080/containers -d '{"image": "my-app"}'
    curl -X POST -H 'Content-Type: application/json' http://localhost:8080/containers -d '{"image": "b14752a6590e"}'
    curl -X POST -H 'Content-Type: application/json' http://localhost:8080/containers -d '{"image": "b14752a6590e","publish":"8081:22"}'
    
     Create image (from uploaded Dockerfile)
    curl -H 'Accept: application/json' -F file=@Dockerfile http://localhost:8080/images
    
     
    curl -X PATCH -H 'Content-Type: application/json' http://localhost:8080/containers/b6cd8ea512c8 -d '{"state": "running"}'
    curl -X PATCH -H 'Content-Type: application/json' http://localhost:8080/containers/b6cd8ea512c8 -d '{"state": "stopped"}'

    curl -s -X PATCH -H 'Content-Type: application/json' http://localhost:8080/images/7f2619ed1768 -d '{"tag": "test:1.0"}'
