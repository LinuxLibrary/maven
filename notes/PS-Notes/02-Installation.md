# Installation of Maven

- To use Maven we need to have JDK 1.7 or higher

```
# cp -prv ~/Downloads/jdk-8u144-linux-x64.tar.gz /u01/
# cd /u01/jdk
# update-alternatives --install /usr/bin/java java /u01/jdk/bin/java 2
# update-alternatives --config java
# update-alternatives --install /usr/bin/jar jar /u01/jdk/bin/jar 2
# update-alternatives --set jar /u01/jdk/bin/jar
# update-alternatives --install /usr/bin/javac javac /u01/jdk/bin/javac 2
# update-alternatives --set javac /u01/jdk/bin/javac 
# java -version
```

- Now downloaad the tarball from Maven website

```
wget http://redrockdigimark.com/apachemirror/maven/maven-3/3.5.0/binaries/apache-maven-3.5.0-bin.tar.gz
```

- Extract and install Maven

```
# mkdir /u01 && cd $_
# cp -prv ~/Downloads/apache-maven-3.5.0-bin.tar.gz .
# tar -xzf apache-maven-3.5.0-bin.tar.gz
# ln -s apache-maven-3.5.0-bin.tar.gz apache-maven
```

- Configure JAVA_HOME and MAVEN_HOME

```
# echo -e "\nJAVA_HOME='/u01/jdk'" >> /etc/profile
# echo -e "\nMAVEN_HOME='/u01/apache-maven'" >> /etc/profile
# source /etc/profile
```

- Set the PATH

```
# export PATH=$PATH:$JAVA_HOME/bin:$JAVA_HOME/jre/bin:$MAVEN_HOME/bin
```
