I ran `docker build . -t curler` in this directory to build the image
with tag `curler`.

Then I started image to a new container with `docker run -it web-server`.
The `-it` flag is necessary as the script prompts the user for a website.

When `helsinki.fi` is given as an input, the output is:

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