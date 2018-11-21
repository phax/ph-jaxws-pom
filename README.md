# ph-jaxws-pom

A POM only project that contains all dependencies for easily using JAXWS from Maven.

Currently it is very tedious to include all artefacts relevant for JAXWS into each and every POM manually.
Therefore I created this project to provide an easy to use POM for using JAXWS from within Maven.

This project is can be used for JAX-WS 2.2.x and 2.3.x (since 1.0.5).
JAX-WS 2.3.x is only targeting Java 9 and newer. 

# News and noteworthy

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
  <version>1.1.0</version>
  <type>pom</type>
</dependency>
```

---

My personal [Coding Styleguide](https://github.com/phax/meta/blob/master/CodingStyleguide.md) |
On Twitter: <a href="https://twitter.com/philiphelger">@philiphelger</a>
