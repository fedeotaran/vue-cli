Vue-cli
=======

This image install all necesary thigs to run vue-cli commands.

Usage
-----

`docker run -it --rm -v "$PWD":"$PWD" -w "$PWD"  -u "$(id -u)" fedeotaran/vue-cli vue`

Generate Alias
--------------

`alias vue='docker run -it --rm -v "$PWD":"$PWD" -w "$PWD"  -u "$(id -u)" fedeotaran/vue-cli vue'`

Run server with compose
-----------------------

```
version: '2'
services:
  web:
    image: fedeotaran/vue-cli
    command: npm run dev
    volumes:
      - .:/code
    ports:
      - "8080:8080"
```
