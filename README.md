# Cloud_Assignment2_C15337401
Python file and text document for the assignment

The system is comprised of two worker nodes and a manager. To run the system use the curl commands below:
curl -s -X GET -H 'Accept: application/json' http://localhost:8080/containers | python -mjson.tool
curl -s -X GET -H 'Accept: application/json' http://localhost:8080/containers?state=running | python -mjson.tool
