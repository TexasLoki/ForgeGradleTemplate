This is a template (or skeleton or boilerplate) repository for Minecraft Forge modding projects.

This branch ("*master*") is for *recommended* 1.7.2 Forge build 1060. Switch to "*edge*" for the latest 1.7.2 Forge build.

## Requirements
* [Gradle installation with gradle binary in PATH](http://www.gradle.org/installation)

	Unlike the source package provided by Forge, this template does not include a gradle wrapper or distribution.

* NetBeans, IntelliJ 13 or any other IDE which can use a gradle build as a project

	Unlike the source package provided by Forge, this template does not include any eclipse files or project skeleton. You may try to generate one via gradle, but YMMV.

## Usage
Simply open or "Import as Gradle Project" `build.gradle` using your IDE of choice. Run `gradle setupDevWorkspace` to setup a testing environment and then `gradle build` to build. To build straight from source without setting up a testing environment, just run `gradle build`.

By default, built JAR files go to the `output` directory.

An example mod is included in `.\src\main\java\com\example\examplemod`. To edit the metadata of your mod, edit `.\src\main\resources\mcmod.info`.

### IDE notes
* **IntelliJ 13** - You will need to additionally run `gradle genIntellijRuns`. This will add the run configurations for Client and Server.
* **NetBeans** - You will need to use the ForgeGradle built-in `debugClient` task to debug Minecraft.

## Warnings
Do not execute `gradle setupDecompWorkspace`. Personal experience has shown that this breaks gradle building/usage and takes too long anyway. This is not a necessary task.

## Updating
To update to a later version of forge, open `build.gradle` in a text editor and update the `version` line under `minecraft` to the latest Forge version string. Alternatively, pull in and merge any changes from this template repository.

Finally, execute `gradle setupDevWorkspace --refresh-dependencies`.