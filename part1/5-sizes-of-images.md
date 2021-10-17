After the images have been pulled from the Docker Hub, information about them
can be viewed using the `docker images` command.

```bash
➜  docker images   

REPOSITORY                          TAG       IMAGE ID       CREATED        SIZE
(omitted)
devopsdockeruh/simple-web-service   ubuntu    4e3362e907d5   7 months ago   83MB
devopsdockeruh/simple-web-service   alpine    fd312adc88e0   7 months ago   15.7MB
```

From its output, one can observe that the version of the image tagged `alpine`
takes is about six times smaller in size.

The functionalities of the two images do not differ: this can be verified by
opening a shell in the Alpine container with 

```
docker exec -it (name of the alpine container) sh
``` 

and checking that the content of `text.log` is alright.
