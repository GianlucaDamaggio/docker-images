This image can be used in interactive mode.

I suggest using the following command in the working directory

```
docker run -it --mount type=bind,source=$(pwd),target=/host gianlucadamaggio/odgi:latest
```
Your host files are at the following path

```
/host
```
