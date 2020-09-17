# ph-jaxws-pom

A POM only project that contains all dependencies for easily using JAXWS from Maven.

Currently it is very tedious to include all artefacts relevant for JAXWS into each and every POM manually.
Therefore I created this project to provide an easy to use POM for using JAXWS from within Maven.

This project is can be used for JAX-WS 2.2.x and 2.3.x (since 1.1.0).

# News and noteworthy

* v1.2.0 - 2020-09-17
    * Updated to Jakarta JAX-WS 2.3.3 - no more JDK dependencies
* v1.1.3 - 2019-05-07
    * Using unbounded version instead of limiting to Java 12.x
* v1.1.2 - 2019-05-02
    * Updated to ph-jaxb-pom 1.0.2
* v1.1.1 - 2019-05-02
    * Updated to stax-ex 1.8.1
    * Added support for JDK 12
* v1.1.0 - 2018-11-21
    * Explicitly using stax-ex 1.8
    * Added support for Java versions up to 11
    * Renamed from `ph-jaxws` to `ph-jaxws-pom`
    * Including `ph-jaxb-pom`
* v1.0.4 - 2017-09-18
    * Needed explicit excludes for `com.sun.xml.bind` artefacts
* v1.0.3 - 2017-09-12
    * Explicitly using stax-ex 1.7.8
    * Switching from `com.sun.xml.bind` artefacts to `org.glassfish.jaxb` artefacts
* v1.0.2 - 2017-07-21
    * Bound to JAXWS 2.2.10
* v1.0.1 - 2016-10-28
    * Explicitly using stax-ex 1.7.7
* v1.0.0 - 2016-02-26
    * Initial release
    * Bound to JAXWS 2.2.9-b14002

# Maven usage

Include it in your regular Maven dependencies but explicitly state the type **pom**:

```xml
<dependency>
  <groupId>com.helger</groupId>
  <artifactId>ph-jaxws-pom</artifactId>
  <version>1.2.0</version>
  <type>pom</type>
</dependency>
```

# Gradle usage (for issues up to 1.1.3)

As Gradle does not support Maven profile activation by JDK version, this section outlines the includes per JDK version (as of ph-jaxws-pom 1.1.0).

With JDK 8, include the following dependencies:
* org.glassfish.jaxb:jaxb-core:2.2.11
* org.glassfish.jaxb:jaxb-runtime:2.2.11
* com.sun.istack:istack-commons-runtime:2.21
* org.glassfish.jaxb:txw2:2.2.11
* com.sun.xml.ws:jaxws-rt:2.2.10 excluding both com.sun.xml.bind:jaxb-core and com.sun.xml.bind:jaxb-impl
* com.sun.xml.ws:policy:2.4
* org.glassfish.gmbal:gmbal-api-only:3.1.0-b001
* com.sun.xml.stream.buffer:streambuffer:1.5.3
* org.glassfish.ha:ha-api:3.1.9
* org.jvnet.staxex:stax-ex:1.8.1

With JDK 9 or later, include the following dependencies:
* org.glassfish.jaxb:jaxb-runtime:2.3.2
* com.sun.xml.ws:jaxws-rt:2.3.1

The exclusion of this POM might be necessary via `exclude group: 'com.helger', module: 'ph-jaxws-pom'`

---

My personal [Coding Styleguide](https://github.com/phax/meta/blob/master/CodingStyleguide.md) |
On Twitter: <a href="https://twitter.com/philiphelger">@philiphelger</a> |
Kindly supported by [YourKit Java Profiler](https://www.yourkit.com)