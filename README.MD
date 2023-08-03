# WildFly Common

WildFly Common is a project to provide common utilities for WildFly and related projects.

WildFly Common is released as a single Maven artifact with the coordinates:

```
<dependency>
    <groupId>org.wildfly.common</groupId>
    <artifactId>wildfly-common</artifactId>
</dependency>
```

# Build WildFly Common

Prerequisites:

* JDK 11 or newer - check `java -version`
* Maven 3.6.0 or newer - check `mvn -v`

To build with your own Maven installation:

```
mvn package
```

# Reporting Issues

WildFly Common uses JIRA to manage issues. All issues can be found [here](https://issues.redhat.com/projects/WFCOM/issues).

To create a new issue, comment on an existing issue, or assign an issue to yourself, you'll need to first [create a JIRA account](https://issues.redhat.com/).

# Release Procedure

WildFly Common is released in [JBoss Nexus Repository](https://repository.jboss.org/nexus/)

To release a new version of WildFly Common:

* Use the Maven [`release` plugin](https://maven.apache.org/maven-release/maven-release-plugin/):

```
mvn release:prepare
mvn release:perform
```

* Close and publish the staged artifacts from  [JBoss Nexus Repository](https://repository.jboss.org/nexus/)
* Release the published version in [JIRA](https://issues.redhat.com/projects/WFCOM?selectedItem=com.atlassian.jira.jira-projects-plugin:release-page&status=released-unreleased)
* Update the Release Notes in [GitHub Release page](https://github.com/jbossas/jboss-dmr/releases)


