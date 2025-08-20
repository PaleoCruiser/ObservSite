```
docker pull nginx

docker run -d -p 8080:80 --name obs_server nginx

docker stop obs_server

docker rm obs_server
```
To see Nginx HTTP request logs on Docker Desktop for Windows, follow these steps:
Identify the Nginx container: Open your terminal or command prompt and run docker ps. This command lists all running Docker containers. Locate the container running your Nginx instance and note its CONTAINER ID or NAMES.
Code
```
docker ps
```
View the logs: Use the docker logs command followed by the container's ID or name to retrieve its logs. By default, the Nginx Docker image sends access and error logs to stdout and stderr, which are captured by Docker's logging mechanism.
Code
```
docker logs obs_server
```

To continuously stream the logs (similar to tail -f), add the -f flag:
Code
```
docker logs -f obs_server
```


http://127.0.0.1:8080/tiny.png?msg=Uncaught%2520ReferenceError%253A%2520typo%2520is%2520not%2520defined&src=blob%253Ahttps%253A%252F%252F4cdebsaxbfy907vgqhlj7d6uzjkpiotno3phgxbuwxkf0u6jzk-h794075209.scf.usercontent.goog%252F9f8db1e5-f9a1-40a6-83f5-aab73eaf2c8e&ln=556&col=7&err_name=ReferenceError&err_stack=ReferenceError%253A%2520typo%2520is%2520not%2520defined%250A%2520%2520%2520%2520at%2520intentionallyCauseError%2520%28blob%253Ahttps%253A%252F%252F4cdebsaxbfy907vgqhlj7d6uzjkpiotno3phgxbuwxkf0u6jzk-h794075209.scf.usercontent.goog%252F9f8db1e5-f9a1-40a6-83f5-aab73eaf2c8e%253A556%253A7%29