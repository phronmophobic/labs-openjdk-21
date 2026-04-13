# Welcome to the JDK!

For build instructions please see the
[online documentation](https://openjdk.org/groups/build/doc/building.html),
or either of these files:

- [doc/building.html](doc/building.html) (html version)
- [doc/building.md](doc/building.md) (markdown version)

See <https://openjdk.org/> for more information about the OpenJDK
Community and the JDK and see <https://bugs.openjdk.org> for JDK issue
tracking.

## iOS notes

Per the instructions from https://github.com/utopia-rise/ios-graal-jdk-21, the patch, https://github.com/utopia-rise/ios-graal-jdk-21/blob/ac1923295a72c4c407e2434ea81e762535a5feb5/labs-openjdk/ios-jdk.patch, was applied.

Usage (also per the above instructions).

```sh
./configure
    --with-conf-name=labsjdk
    --with-version-opt=jvmci-23.1.3-b33
    --with-version-pre=
    --with-vendor-name="GraalVM Community"
    --with-vendor-url=https://www.graalvm.org/
    --with-vendor-bug-url=https://github.com/oracle/graal/issues
    --with-vendor-vm-bug-url=https://github.com/oracle/graal/issues

make CONF_NAME=labsjdk graal-builder-image
```

Note: I couldn't find jvmci-23.1.3-b33. The closest I could find was 
GraalVM for Java Development Kit 21.0.3 at  https://www.oracle.com/java/technologies/javase/graalvm-jdk21-archive-downloads.html which is jvmci-23.1-b37.


