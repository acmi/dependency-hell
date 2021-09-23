Dependency Hell
---------------

Необходимо исправить `pom.xml`, добиться успешного выполнения команды `mvn validate`.

Запрещено прописывать в секции `dependencyManagement` зависимость:
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-dependencies</artifactId>
    <version>${spring-boot.version}</version>
    <type>pom</type>
    <scope>import</scope>
</dependency>
```
Всё остальное разрешено😊

Для усложнения задания можно раскомментировать блок
```xml
<!--<dependency>-->
<!--    <groupId>org.springframework.boot</groupId>-->
<!--    <artifactId>spring-boot-starter-data-jpa</artifactId>-->
<!--    <version>${spring-boot.version}</version>-->
<!--</dependency>-->
```