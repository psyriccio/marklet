# Marklet

[![Build Status](https://travis-ci.org/Faylixe/marklet.svg)](https://travis-ci.org/Faylixe/marklet) [![Maven Central](https://maven-badges.herokuapp.com/maven-central/fr.faylixe/marklet/badge.svg)](https://maven-badges.herokuapp.com/maven-central/fr.faylixe/marklet) [![Join the chat at https://gitter.im/Faylixe/marklet](https://badges.gitter.im/Faylixe/marklet.svg)](https://gitter.im/Faylixe/marklet?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

**Marklet** is a custom Java Doclet which aims to generate a Javadoc in a markdown format which is ready to use in GitHub. You can check a **Marklet** generated javadoc on the following project :

* [Marklet itself !](https://github.com/Faylixe/marklet/tree/master/javadoc/fr/faylixe/marklet)
* [Google Code Jam API](https://github.com/Faylixe/googlecodejam-client/tree/master/javadoc/fr/faylixe/googlecodejam/client)

In order to use it with Maven, adds the following configuration for the ``maven-javadoc-plugin``
in your project ``POM`` :

```xml
<plugin>
	<groupId>org.apache.maven.plugins</groupId>
	<artifactId>maven-javadoc-plugin</artifactId>
	<version>2.9</version>
	<configuration>
		<doclet>fr.faylixe.marklet.Marklet</doclet>
		<docletArtifact>
			<groupId>fr.faylixe</groupId>
			<artifactId>marklet</artifactId>
			<version>1.0.5</version>
		</docletArtifact>
		<reportOutputDirectory>./</reportOutputDirectory>
		<destDir>./</destDir>
		<additionalparam>-d javadoc/</additionalparam>
		<useStandardDocletOptions>false</useStandardDocletOptions>
	</configuration>
</plugin>
```

This will generate the javadoc report into the project directory under subfolder ``javadoc/``.

##Current issues

The current version is a pre release with the following feature missing :

* Interfaces, inner classes, enumerations, and annotations has not been tested already and subject to bug.

If you do notice any other error, do not hesitate to submit pull request, or indicates it to the Gitter channel.