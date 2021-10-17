I spun up a container with the provided image and started the bash shell in it:

```bash
docker run -d -it --name secretmsg devopsdockeruh/simple-web-service:ubuntu
docker exec -it secretmsg bash
```

Using `tail -f ./text.log`, I found the following text from the `text.log` file:

```
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
```