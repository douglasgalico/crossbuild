# CrossBuild - Docker images for cross-compilation

- based on crosstool-NG (git master release)
- go compiler
- cmake
- ninja
- pkg-config

## Examples

```
docker run --rm \
    -v "${SRCDIR}":/work \
    desertbit/crossbuild:linux-armv7 \
    make all
```

```
docker run --rm \
    -v "${SRCDIR}":/work \
    desertbit/crossbuild:linux-armv7 \
    sh -c '$CC test.c -o test'
```

## Alpine Images

The docker alpine images are unstable and broken. Crosstool-NG is not fully compatible...
This is a work in progress task.

## Credits

- [crosstool-NG](https://crosstool-ng.github.io/)
- [dockcross](https://github.com/dockcross/dockcross)