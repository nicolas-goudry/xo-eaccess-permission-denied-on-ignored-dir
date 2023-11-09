# EACCESS: permission denied on an ignored directory while running xo

This repository reproduces the issue with `xo` failing with a **EACCESS** error on an ignored directory.

To reproduce the issue:

```
npm i
mkdir -p .data
docker compose up -d
npm run lint
```

```
> xo-eaccess-permission-denied-on-ignored-dir@1.0.0 lint
> xo

Error: EACCES: permission denied, scandir '/fakepath/xo-eaccess-permission-denied-on-ignored-dir/.data/mysql/#innodb_redo'
```
