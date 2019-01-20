#### Which version of Java should I use?

Majority of the course has been developed on Java 8. The course is being updated to Java 11.

If you wish to use Java 9 or higher, please modify the following:

**Note:** If you are on Java 9, or Java 10 you should consider updating to Java 11.

Update your Maven POM properties to reflect the Java version. 
```xml
    <properties>
        <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
        <project.reporting.outputEncoding>UTF-8</project.reporting.outputEncoding>
        <java.version>11</java.version>
        <jaxb.version>2.3.0</jaxb.version>
        <maven.compiler.source>${java.version}</maven.compiler.source>
        <maven.compiler.target>${java.version}</maven.compiler.target>
    </properties>

```

The JAXB API is no longer included with Java in Java 9 and higher. You will need to add this dependency as follows:

```xml
        <dependency>
            <groupId>javax.xml.bind</groupId>
            <artifactId>jaxb-api</artifactId>
            <version>${jaxb.version}</version>
        </dependency>
        <dependency>
            <groupId>com.sun.xml.bind</groupId>
            <artifactId>jaxb-core</artifactId>
            <version>${jaxb.version}</version>
        </dependency>
        <dependency>
            <groupId>com.sun.xml.bind</groupId>
            <artifactId>jaxb-impl</artifactId>
            <version>${jaxb.version}</version>
        </dependency>
```

#### Do I need to use the Oracle JDK?
No. Open JDK should work just as well. 

#### Do I need to pay Oracle for a license to use Java?
No, the Oracle JDK is free to use for development.