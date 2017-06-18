# Spark + Scala Boilerplate Project

This project provides a skeleton code for a typical Spark project based on Scala. You can use it to quickly bootstrap your own Spark application.

The code doesn't do much, just shows how to create a RDD and show the contents of it.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development purposes. Please note that the instructions are tailored for a typical Ubuntu (or any linux flavored) based OS.

If you are working on Windows, we highly recommend installing Ubuntu on top of Virtual Box.Please download [Virtual Box](https://www.virtualbox.org/) and latest [Ubuntu 17.04 image](https://www.virtualbox.org/wiki/Linux_Downloads).
Please see [these instructions](http://www.wikihow.com/Install-Ubuntu-on-VirtualBox) on how to complete setting up Ubuntu with Virtual Box.


## Prerequisites

Please update the package index by in your terminal by typing:

```sudo apt-get update```

### Java installation
Please check whether java is installed by typing

```java -version```

If you see something like “The program ‘java’ can be found in the following packages…”, we need to install JDK. The easiest option for installing Java is using the version packaged with Ubuntu. Specifically, this will install OpenJDK 8, the latest and recommended version.

Now you can install the JDK with the following command:

```sudo apt-get install -y default-jdk```

### Scala installation
```sudo apt-get install -y scala```

### Git installation
```sudo apt-get install -y git```

### Maven installation
```sudo apt-get install -y maven```

### Spark Installation
Download and install the latest version of Spark on your system with these commands.

```
wget https://d3kbcqa49mib13.cloudfront.net/spark-2.1.1-bin-hadoop2.7.tgz
tar -xvzf spark-2.1.1-bin-hadoop2.7.tgz
sudo mv spark-2.1.1-bin-hadoop2.7 /usr/local/spark
echo 'export PATH=$PATH:/usr/local/spark/bin' >> ~/.bashrc
source ~/.bashrc
```

You can verify the installation by the following command, which should launch spark shell.

```spark-shell```

### Cloning the project
Clone this project using git.
```
git clone https://github.com/CrowdShakti/spark-scala-mvn-boilerplate.git
cd spark-scala-mvn-boilerplate
```

### Building the project
Let's use maven for building the project.
```
mvn package
```

### Running the project
The command for running the jar file created by build phase is:

```spark-submit --class com.examples.MainExample --master local[2] target/spark-scala-maven-project-0.0.1-SNAPSHOT-jar-with-dependencies.jar```


## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags).


## License

This project is licensed under the Apache 2.0 License - see the [LICENSE.md](LICENSE.md) file for details

