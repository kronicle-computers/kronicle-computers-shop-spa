# Frontend SPA

This repo contains the Frontend SPA for the fictional Kronicle Computers online computer shop

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
