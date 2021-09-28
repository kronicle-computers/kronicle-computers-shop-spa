# Shop SPA

This repo contains the Shop SPA for the fictional Kronicle Computers online computer shop

## Kronicle

This repo contains a [kronicle.yaml](kronicle.yaml) file that describes the components (e.g. services, databases, 
queues etc.) that belong to this repo.  That YAML file is automatically read by [Kronicle](https://kronicle.tech) from 
this repo's main branch every 15 minutes, with any changes merged to the main branch automatically appearing in 
Kronicle after 15-30 minutes.

### Checking the contents of the `kronicle.yaml` file is valid after making a change

You can run the following command to validate the contents of the `kronicle.yaml` file:

```shell
$ ./gradlew validateKronicleMetadata
```

The following command can also be used:

```shell
$ ./gradlew build
```

### Changes to `kronicle.yaml` file are automatically picked up by Kronicle

There is no need to release changes to the [kronicle.yaml](kronicle.yaml) file in this repo.
When changes to the [kronicle.yaml](kronicle.yaml) file are merged to the main branch,
those changes will automatically become visible in Kronicle within the next 15 to 30 minutes.  
Kronicle reloads all `kronicle.yaml` files every 15 minutes but this takes 10 to 30
minutes to complete.

### Example YAML for areas, teams and components

See the https://github.com/kronicle-tech/kronicle-metadata-codebase-template/blob/main/kronicle.yaml
file for example YAML for components.

### Updating the dependency on the `tech.kronicle:metadata` library

From time to time, Kronicle will make changes to the objects and fields that are supported in
`kronicle.yaml` files. When this happens, you can bring in support for those changes to this repo by
updating the version of the `kronicleVersion` setting in the [gradle.properties](gradle.properties)
file in this repo.

## Build Setup

```bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm run start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, check out the [documentation](https://nuxtjs.org).

## Special Directories

You can create the following extra directories, some of which have special behaviors. Only `pages` is required; you can delete them if you don't want to use their functionality.

### `assets`

The assets directory contains your uncompiled assets such as Stylus or Sass files, images, or fonts.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/assets).

### `components`

The components directory contains your Vue.js components. Components make up the different parts of your page and can be reused and imported into your pages, layouts and even other components.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/components).

### `layouts`

Layouts are a great help when you want to change the look and feel of your Nuxt app, whether you want to include a sidebar or have distinct layouts for mobile and desktop.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/layouts).


### `pages`

This directory contains your application views and routes. Nuxt will read all the `*.vue` files inside this directory and setup Vue Router automatically.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/get-started/routing).

### `plugins`

The plugins directory contains JavaScript plugins that you want to run before instantiating the root Vue.js Application. This is the place to add Vue plugins and to inject functions or constants. Every time you need to use `Vue.use()`, you should create a file in `plugins/` and add its path to plugins in `nuxt.config.js`.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/plugins).

### `static`

This directory contains your static files. Each file inside this directory is mapped to `/`.

Example: `/static/robots.txt` is mapped as `/robots.txt`.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/static).

### `store`

This directory contains your Vuex store files. Creating a file in this directory automatically activates Vuex.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/store).
