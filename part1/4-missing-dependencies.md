First, I started a container called `curler` based on the `ubuntu:latest` image:

```bash
docker run -d -it --name curler ubuntu
```

Because `curl` is required as a dependency, I had to get inside the container with
`docker exec -it curler bash` and install it there:

```bash
apt update
apt install -y curl
```

Then, I was set up to execute the provided shell script in the container with 
`docker exec`. The `-it` flag is necessary to make the prompt of the script
interactive:

```bash
docker exec -it curler sh -c 'echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;'
```

For example, when `helsinki.fi` is given to the script as input, the output is following:

```
Input website:
helsinki.fi
Searching..
<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>301 Moved Permanently</title>
</head><body>
<h1>Moved Permanently</h1>
<p>The document has moved <a href="https://www.helsinki.fi/">here</a>.</p>
</body></html>
```


