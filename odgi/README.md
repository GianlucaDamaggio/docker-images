This image can be used in _interactive_ mode.

I suggest using the following command in the working directory

```
docker run -it --mount type=bind,source=$(pwd),target=/host gianlucadamaggio/odgi:latest
```

The executable is at the following path

```
/home/Admin/github/odgi/bin/./odgi
```

Your _host_ files are at the following path
```
/host
```
