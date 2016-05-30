asynchbase
==========

This is a patched version of [SteamShon/asynchbase](https://github.com/SteamShon/asynchbase) which is again forked from [OpenTSDB/asynchbase](https://github.com/OpenTSDB/asynchbase) to support some features that does not exist.

In addition to the patches made in [SteamShon/asynchbase](https://github.com/SteamShon/asynchbase), this project sets up `maven-shade-plugin` to relocate some packages that are prone to collision, specifically,

* `com.google` → `org.apache.s2graph.google` : Google Guava and Protocol Buffers
* `org.jboss` → `org.apache.s2graph.jboss` : Netty 3.9.4.Final


## Building

The following command will make a shaded jar in the directory `target`.

    mvn package -DskipTests
    
The following command will 