# HelloWorld Project

- Let us configure a basic helloworld build
- Create a helloworld project directory and write the below code to `pom.xml` file
- Here pom stands for Project Object Model

```
# mkdir -p /maven/workspace/HelloWorld && cd $_
# vi pom.xml
```

```
<project>

	<groupId>com.example</groupId>
	<artifactId>HellloWorld</artifactId>
	<version>1.0-SNAPSHOT</version>
	<modelVersion>4.0.0</modelVersion>
	<packaging>jar</packaging>

</project>
```

- Let us now create a java file to print HelloWorld. For that we need to create the folder structure in the HelloWorld project workspace

```
# cd /maven/workspace/HelloWorld
# mkdir -p src/main/java
# vi HelloWorld.java
```

```
public class HelloWorld {
	public static void main (String args[]) {
		System.out.println("Hello World");
	}
}
```

- Now we need to run `mvn clean`. This will download required plugins

```
# mvn clean
```

- Now we need to compile

```
# mvn compile
```

- After compiling we can found a `target/classes` directory in which we'll have our `HelloWorld.class` file.
- This is our HelloWorld application
- Now all we need to do is to package our application to a `jar` file
- For that we have to run `mvn package`

```
# mvn package
```

- We can get our jar file in the target directory with the naming convension as `<artifactId>-<version>.<package-extension>`

```
# ls target/*.jar

HelloWorld-1.0-SNAPSHOT.jar
```
