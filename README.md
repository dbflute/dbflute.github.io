# DB management system for Lean startup

## Contribution Guides
DBFlute want to your contribution. If you want to contribute this project, please contact me!  [@jflute](https://twitter.com/jflute)


## To install

### Requirements:

    Java8(for Apache Ant)
    Maven
    pom.xml
    Internet connection

### Add dependency to pom.xml:

DBFlute:
```
<dependency>
    <groupId>org.dbflute</groupId>
    <artifactId>dbflute-runtime</artifactId>
    <!-- optional -->
    <!-- <version>${dbflute.version}</version> -->
</dependency>
```

JDBC Driver(Example - MySQL):
```
<dependency>
    <groupId>mysql</groupId>
    <artifactId>mysql-connector-java</artifactId>
    <version>5.1.33</version>
    <scope>runtime</scope>
</dependency>
```

JDBC Drivers for H2, MySQL, PostgreSQL are included. If you want to use driver for other, you need to put a driver file on *DBFlute-client*/extlib directory.


DBFlute Maven plugin:
```
<plugin>
    <groupId>org.dbflute</groupId>
    <artifactId>dbflute-maven-plugin</artifactId>
    <version>1.1.0-RC3</version>
    <!-- "RC3" as of 2015/02/15 -->
    <configuration>
        <clientProject>xxxdb</clientProject>
        <packageBase>com.xxx.dbflute</packageBase>
    </configuration>
</plugin>
```

If do you want a version's DBFlute, you can use this properties:
```
<dbflute.version>1.1.0-sp2</dbflute.version>
```

### Create client for Maven:
```
mvn -e dbflute:create-client
```

After running this command, *DBFlute-client* directory is created.
```
[PROJECT_ROOT]
 |-src/main/java
 |-...
 |-dbflute_xxxdb // DBFlute-client
    |-dfprop
    |-...
 |-mydbflute
    |-dbflute-1.1.0 // DBFlute-engine
```

### Modify properties
Please modify two files for your environment.

- *DBFlute-client*/dfprop/basicInfoMap.dfprop
- *DBFlute-client*/dfprop/databaseInfoMap.dfprop

##### basicInfoMap.dfprop(Exapmle - MySQL, String):
```
    ...
    # /- - - - - - - - - - - - - - - - - - - - - - - - - - - - - -
    # o database: (Required)
    #  This is the target database, only considered when generating
    #  the SQL for your DBFlute project.
    #  Your possible choices are:
    #
    #    mysql, postgresql, oracle, db2, sqlserver,
    #    h2, derby, (sqlite, firebird, msaccess)
    #
    ; database = mysql
    # - - - - - - - - - -/
    ...

    # /- - - - - - - - - - - - - - - - - - - - - - - - - - - - - -
    # o targetContainer: (Required)
    #  The target DI container.
    #  If your target language is 'csharp', you can specify 'seasar' only.
    #  Your possible choices are:
    #
    #       spring, guice, seasar, cdi
    #
    ; targetContainer = spring
    # - - - - - - - - - -/
    ...
```

##### databaseInfoMap.dfprop(Exapmle - MySQL):

```
...
map:{
    ; driver   = com.mysql.jdbc.Driver
    ; url      = jdbc:mysql://localhost:3306/xxxdb?characterEncoding=UTF-8
    ; schema   =  
    ; user     = xxxdb
    ; password = xxxdb
    ...
}
```

## Resources for Newcomers
- [Setup with Maven(Japanese Only)](http://dbflute.seasar.org/ja/environment/setup/maven.html)
- [DBFlute Official(Japanese Only)](http://dbflute.seasar.org/)
- [Google Groups(Japanese Only)](https://groups.google.com/forum/#!forum/dbflute)
- [Author's Twitter](https://twitter.com/jflute)
