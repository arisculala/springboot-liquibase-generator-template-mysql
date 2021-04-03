# springboot-liquibase-generator-template-mysql

## Prerequisite:
* Make sure to install maven (https://maven.apache.org/install.html)
* Make sure to install mysql (https://dev.mysql.com/doc/mysql-osx-excerpt/5.7/en/osx-installation-pkg.html)


- Make sure that you have installed mysql in your local
```
NOTE: By default your local mysql have the accout `root` as superuser
```

- Create test database `test_liquibase`
```
$ mysql -uroot
mysql> CREATE DATABASE test_liquibase;
mysql> exit
```
- Checkout the project in your chosen local directory
```
$ mkdir dev
$ cd dev
$ git clone https://github.com/arisculala/springboot-liquibase-generator-template-mysql.git
```

- Browse inside the project directory and run liquibase
```
$ cd springboot-liquibase-generator-template-mysql
$ mvn liquibase:update
```

- You should be able to see success build message
```
[INFO] Scanning for projects...
[INFO]
[INFO] --< com.liquibase.generator.template:springboot-liquibase-generator-template >--
[INFO] Building Springboot Liquibase Generator Template 0.0.1-SNAPSHOT
[INFO] --------------------------------[ war ]---------------------------------
[INFO]
[INFO] --- liquibase-maven-plugin:4.2.2:update (default-cli) @ springboot-liquibase-generator-template ---
[INFO] ------------------------------------------------------------------------
[project, pluginDescriptor]
[INFO]
[INFO]
[INFO] Liquibase Community 4.2.2 by Datical
[INFO] ####################################################
##   _     _             _ _                      ##
##  | |   (_)           (_) |                     ##
##  | |    _  __ _ _   _ _| |__   __ _ ___  ___   ##
##  | |   | |/ _` | | | | | '_ \ / _` / __|/ _ \  ##
##  | |___| | (_| | |_| | | |_) | (_| \__ \  __/  ##
##  \_____/_|\__, |\__,_|_|_.__/ \__,_|___/\___|  ##
##              | |                               ##
##              |_|                               ##
##                                                ##
##  Get documentation at docs.liquibase.com       ##
##  Get certified courses at learn.liquibase.com  ##
##  Free schema change activity reports at        ##
##      https://hub.liquibase.com                 ##
##                                                ##
####################################################
Starting Liquibase at 01:31:09 (version 4.2.2 #36 built at 2020-12-09 20:07+0000)
[INFO] Executing on Database: jdbc:mysql://localhost:3306/test_liquibase
[INFO] Successfully acquired change log lock
[INFO] Creating database history table with name: DATABASECHANGELOG
[INFO] Reading from DATABASECHANGELOG
[INFO] Table user created
[INFO] ChangeSet src/main/resources/config/liquibase/changelog/initial_schema.xml::1b474469-bfac-4872-82eb-2db5340a0674::arisculala ran successfully in 29ms
[INFO] Successfully released change log lock
[INFO] ------------------------------------------------------------------------
[INFO]
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  2.376 s
[INFO] Finished at: 2021-04-04T01:31:10+08:00
[INFO] ------------------------------------------------------------------------
```
