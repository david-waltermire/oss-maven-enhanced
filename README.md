# Maven Build Support for NIST Security Automation Open-Source Software (OSS) Projects

This project provides support for using the Apache [Maven](https://maven.apache.org/) build system.

## Features

This project implements the following features:

* Provides dependency management for the JUnit test framework.
* Provides Maven SCM Git support through the use of the [maven-scm-provider-gitexe](https://maven.apache.org/scm/maven-scm-providers/maven-scm-providers-git/maven-scm-provider-gitexe/).
* Configures java source and compile targets to 1.8
* Manages Maven Plugin versions for a large number of common Plugins to provide a stable build experience.
* Sets up Maven site building using NIST templates
* Configures Javadoc generation, with linking to Java 8 Javadocs
* Uses [PMD](https://pmd.github.io/) through the [maven-pmd-plugin](https://maven.apache.org/plugins/maven-pmd-plugin/) supporting basic static code analysis. 
* Enforces NIST license use on source through the [license-maven-plugin](http://code.mycila.com/license-maven-plugin/).
* and many other features.

## System Requirements

* An Oracle Java 1.8 or higher compatible runtime environment
* An [installation](https://maven.apache.org/install.html) of Apache Maven version 3.0 or higher.

## Usage
 
To use this project, you must configure it as the parent in your Maven pom.xml file.

```Maven POM
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <parent>
        <groupId>gov.nist.secauto</groupId>
        <artifactId>oss-parent</artifactId>
        <version>... version of this project ...7</version>
    </parent>

    ... additional configuration
</project>
```