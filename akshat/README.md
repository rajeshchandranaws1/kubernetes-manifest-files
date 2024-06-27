# Permanently authenticating with Git repositories
Run the following command to enable credential caching:<br>
ghp_191wN8uucbm81h7n3DbQHeENNzdxYmx2NRIJ2

```
$ git config credential.helper store
$ git push https://github.com/owner/repo.git
```

```
Username for 'https://github.com': <USERNAME>
Password for 'https://USERNAME@github.com': <PASSWORD>
```
You should also specify caching expire,

git config credential.helper 'cache --timeout 7200'
After enabling credential caching, it will be cached for 7200 seconds (2 hour). <br>
43,200 s = 12 h (login once per day) might also be a reasonable choice for some.

You can also use similar commands to configure this not per repository but globally:

```
git config --global credential.helper store
git config --global credential.helper 'cache --timeout 7200'
```
