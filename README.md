# Intellij patcher docker image

You can find info about patcher itself [here](https://github.com/zr9/intellij_patcher)

## Usage

Clone with `--recurse-submodules`, copy your `platform-impl.jar` to `res` dir, do `chmod 0777 res/platform-impl.jar`, do `docker-compose build` then `docker-compose run patcher`. Enjoy