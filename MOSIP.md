# <a href="https://github.com/mosip/commons" style="background: url('image-url') repeat;">commons</a>

<!-- ## <a href="https://github.com/mosip/resident-services/blob/master/resident/pom.xml" style="background: url('image-url') repeat;">resident\pom.xml (Parent pom.xml)</a> -->

## Changes that are common to every file.

### 1. Maven version.


#### Older version:

```xml
    <maven.compiler.source>11</maven.compiler.source>
    <maven.compiler.target>11</maven.compiler.target>
```

#### Updated version:

```xml
    <maven.compiler.source>17</maven.compiler.source>
    <maven.compiler.target>17</maven.compiler.target>
```

### 2. Spring boot and its related component version.

#### Older:

```xml
<spring.boot.version>2.0.2.RELEASE</spring.boot.version>
<spring.data.jpa.version>2.0.7.RELEASE</spring.data.jpa.version>
<spring.security.test.version>5.0.5.RELEASE</spring.security.test.version>
<spring-cloud-config.version>2.0.0.RELEASE</spring-cloud-config.version>
```

#### Updated:

```xml
<spring.boot.version>2.7.18</spring.boot.version>
<spring.data.jpa.version>2.7.18</spring.data.jpa.version>
<spring.security.test.version>5.7.11</spring.security.test.version>
<spring-cloud-config.version>3.1.3</spring-cloud-config.version>
```


### 3. Lombok Version:

#### Older:

```xml
<lombok.version>1.18.8</lombok.version>
```

#### Updated:

```xml
<lombok.version>1.18.30</lombok.version>
```

### 4. Jacoco Version:

#### Older:

```xml
<jacoco.maven.plugin.version>0.8.5</jacoco.maven.plugin.version>
```

#### Updated:

```xml
<jacoco.maven.plugin.version>0.8.7</jacoco.maven.plugin.version>
```

### 5. Junit Version:

#### Older:

```xml
<junit.version>4.12</junit.version>
```

#### Updated:

```xml
<junit.version>4.13.1</junit.version>
```

### 6. Added Junit Dependency:


```xml
<dependency>
    <groupId>junit</groupId>
    <artifactId>junit</artifactId>
    <version>${junit.version}</version>
</dependency>
```




<!-- ## <a href="https://github.com/mosip/commons/blob/master/kernel/kernel-core/pom.xml" style="background: url('image-url') repeat;">1. kernel-core (/kernel/kernel-core/pom.xml)</a>


### No other changes needed. -->

<!-- #### Older:

```xml
<lombok.version>1.18.8</lombok.version>
```

#### Updated:

```xml
<lombok.version>1.18.30</lombok.version>
```

### 2. Jacoco Version:

#### Older:

```xml
<jacoco.maven.plugin.version>0.8.5</jacoco.maven.plugin.version>
```

#### Updated:

```xml
<jacoco.maven.plugin.version>0.8.7</jacoco.maven.plugin.version>
``` -->


<!-- 

## <a href="https://github.com/mosip/commons/blob/master/kernel/kernel-authcodeflowproxy-api/pom.xml" style="background: url('image-url') repeat;">2. kernel/kernel-authcodeflowproxy-api (/kernel/kernel-authcodeflowproxy-api/pom.xml)</a>


### 1. Lombok Version:

#### Older:

```xml
<lombok.version>1.18.8</lombok.version>
```

#### Updated:

```xml
<lombok.version>1.18.30</lombok.version>
```

### 2. Jacoco Version:

#### Older:

```xml
<jacoco.maven.plugin.version>0.8.5</jacoco.maven.plugin.version>
```

#### Updated:

```xml
<jacoco.maven.plugin.version>0.8.7</jacoco.maven.plugin.version>
```

        
## <a href="https://github.com/mosip/commons/blob/master/kernel/kernel-biometrics-api/pom.xml" style="background: url('image-url') repeat;">3. kernel/kernel-biometrics-api (/kernel/kernel-biometrics-api/pom.xml)</a>


### 1. Lombok Version:

#### Older:

```xml
<lombok.version>1.18.8</lombok.version>
```

#### Updated:

```xml
<lombok.version>1.18.30</lombok.version>
```

### 2. Jacoco Version:

#### Older:

```xml
<jacoco.maven.plugin.version>0.8.5</jacoco.maven.plugin.version>
```

#### Updated:

```xml
<jacoco.maven.plugin.version>0.8.7</jacoco.maven.plugin.version>
```

 -->


<!-- ## 3. h2:

### Older:

```xml
<h2.version>1.4.197</h2.version>
```

### Updated:

```xml
<h2.version>2.2.224</h2.version>
```

## 4. Postgresql

### Older:

```xml
<postgresql.version>42.2.2</postgresql.version>
```

### Updated:

```xml
<postgresql.version>42.7.2</postgresql.version>
```

## 5. hibernate

### Older:

```xml
<hibernate.version>5.2.17.Final</hibernate.version>
```

### Updated:

```xml
<hibernate.version>6.4.4.Final</hibernate.version>
```

## 6. junit

### Older:

```xml
<junit.version>4.12</junit.version>
```

### Updated:

```xml
<junit.version>4.13.2</junit.version>
```

## 7. lombok

### Older:

```xml
<lombok.version>1.18.8</lombok.version>
```

### Updated:

```xml
<lombok.version>1.18.30</lombok.version>
```

## <a href="https://github.com/mosip/resident-services/blob/master/resident/resident-service/pom.xml" style="background: url('image-url') repeat;">resident\resident-service\pom.xml</a>

### Added plugin to support lombok (needed for java 17):

```xml
<plugin>
    <groupId>org.apache.maven.plugins</groupId>
    <artifactId>maven-compiler-plugin</artifactId>
    <version>${maven.compiler.version}</version>
    <configuration>
        <source>${maven.compiler.source}</source>
        <target>${maven.compiler.target}</target>
        <fork>true</fork>
        <compilerArgs>
            <arg>-J--add-opens=jdk.compiler/com.sun.tools.javac.code=ALL-UNNAMED</arg>
            <arg>-J--add-opens=jdk.compiler/com.sun.tools.javac.comp=ALL-UNNAMED</arg>
            <arg>-J--add-opens=jdk.compiler/com.sun.tools.javac.file=ALL-UNNAMED</arg>
            <arg>-J--add-opens=jdk.compiler/com.sun.tools.javac.main=ALL-UNNAMED</arg>
            <arg>-J--add-opens=jdk.compiler/com.sun.tools.javac.model=ALL-UNNAMED</arg>
            <arg>-J--add-opens=jdk.compiler/com.sun.tools.javac.parser=ALL-UNNAMED</arg>
            <arg>-J--add-opens=jdk.compiler/com.sun.tools.javac.processing=ALL-UNNAMED</arg>
            <arg>-J--add-opens=jdk.compiler/com.sun.tools.javac.tree=ALL-UNNAMED</arg>
            <arg>-J--add-opens=jdk.compiler/com.sun.tools.javac.util=ALL-UNNAMED</arg>
            <arg>-J--add-opens=jdk.compiler/com.sun.tools.javac.jvm=ALL-UNNAMED</arg>
        </compilerArgs>
        <annotationProcessorPaths>
            <path>
                <groupId>org.projectlombok</groupId>
                <artifactId>lombok</artifactId>
                <version>${lombok.version}</version>
            </path>
        </annotationProcessorPaths>
    </configuration>
</plugin>
```

## 2. springdoc:

### Older:

```xml
<version>2.5.4</version>
```

### Updated:

```xml
<version>${spring.boot.version}</version>
```
 -->
