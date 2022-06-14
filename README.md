# Sinfonia

Purpur modifications that adds new features in order to work along with the PixelJam plugins ecosystem.

## License
[![MIT License](https://img.shields.io/github/license/PurpurMC/Purpur?&logo=github)](LICENSE)

All patches are licensed under the MIT license, unless otherwise noted in the patch headers.

See [PaperMC/Paper](https://github.com/PaperMC/Paper), and [PaperMC/Paperweight](https://github.com/PaperMC/paperweight) for the license of material used by this project.

## API

### [Javadoc](https://purpurmc.org/javadoc)

### Dependency Information
Maven
```xml
<repository>
    <id>purpur</id>
    <url>https://repo.purpurmc.org/snapshots</url>
</repository>
```
```xml
<dependency>
    <groupId>org.purpurmc.purpur</groupId>
    <artifactId>purpur-api</artifactId>
    <version>1.19-R0.1-SNAPSHOT</version>
    <scope>provided</scope>
</dependency>
```

Gradle
```kotlin
repositories {
    maven("https://repo.purpurmc.org/snapshots")
}
```
```kotlin
dependencies {
    compileOnly("org.purpurmc.purpur", "purpur-api", "1.19-R0.1-SNAPSHOT")
}
```

Yes, this also includes all API provided by Paper, Spigot, and Bukkit.

## Building and setting up

#### Initial setup
Run the following commands in the root directory:

```
./gradlew applyPatches
```

#### Creating a patch
Patches are effectively just commits in either `Purpur-API` or `Purpur-Server`.
To create one, just add a commit to either repo and run `./gradlew rebuildPatches`, and a
patch will be placed in the patches folder. Modifying commits will also modify its
corresponding patch file.

See [CONTRIBUTING.md](CONTRIBUTING.md) for more detailed information.


#### Compiling

Use the command `./gradlew build` to build the API and server. Compiled JARs
will be placed under `Purpur-API/build/libs` and `Purpur-Server/build/libs`.

To get a purpurclip jar, run `./gradlew createReobfPaperclipJar`.
To install the `purpur-api` and `purpur` dependencies to your local Maven repo, run `./gradlew publishToMavenLocal`