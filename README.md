# ph-jaxws
A POM only project that contains all dependencies for easily using JAXWS from Maven.

Currently it is very tedious to include all artefacts relevant for JAXWS into each and every POM manually.
Therefore I created this project to provide an easy to use POM for using JAXWS from within Maven.

#Maven usage

Include it in your regular Maven dependencies but explicitly state the type **pom**:

```xml
    <dependency>
      <groupId>com.helger</groupId>
      <artifactId>ph-jaxws</artifactId>
      <version>1.0.0-SNAPSHOT</version>
      <type>pom</type>
    </dependency>
```

---

My personal [Coding Styleguide](https://github.com/phax/meta/blob/master/CodeingStyleguide.md) |
On Twitter: <a href="https://twitter.com/philiphelger">@philiphelger</a>
