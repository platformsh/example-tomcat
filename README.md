# Tomcat 8.5 template for Platform.sh

The Apache Tomcat® software is an open source implementation of the Java Servlet, JavaServer Pages, Java Expression Language and Java WebSocket technologies. The Java Servlet, JavaServer Pages, Java Expression Language and Java WebSocket specifications are developed under the Java Community Process.

This template has the Tomcat, so you need to deploy your application. There are two ways to do it:

## Tomcat Manager

The Tomcat Host Manager application enables you to create, delete, and otherwise manage virtual hosts within Tomcat. 

 The Tomcat Host Manager application is a part of Tomcat installation, by default available using the following context: /host-manager. You can use the host manager in the following ways:

* Utilizing the graphical user interface, accessible at: {server}/host-manager/html.
* Utilizing a set of minimal HTTP requests suitable for scripting. You can access this mode at: {server}/host-manager/text.

The user is `admin` and to get the password, you can access the machine through [SSH](https://docs.platform.sh/development/access-site.html#accessing-the-application-with-ssh) and execute:
`echo $PLATFORM_PROJECT_ENTROPY`

## Deploy via SSH

You can deploy an App without the Tomcat Manager with an upload of the artifact at the `webapps` folder via [SSH](https://docs.platform.sh/development/access-site.html#accessing-the-application-with-ssh).


## Services

* Java 8

## Customizations

The following files and additions make the framework work.  If using this project as a reference for your own existing project, replicate the changes below to your project.

* [`.platform/routes.yaml`](.platform/routes.yaml): Platform.sh allows you to define the [routes](https://docs.platform.sh/configuration/routes.html).
* [`.platform/services.yaml`](.platform/services.yaml):  Platform.sh allows you to completely define and configure the topology and [services you want to use on your project](https://docs.platform.sh/configuration/services.html).
* [`.platform.app.yaml`](.platform.app.yaml): You control your application and the way it will be built and deployed on Platform.sh [via a single configuration file](https://docs.platform.sh/configuration/app-containers.html).
* An additional library dependency, [`platformsh/config-reader-java`](https://github.com/platformsh/config-reader-java), has been added.  It provides convenience wrappers for accessing the Platform.sh environment variables.

## References

* [Platform.sh post](https://platform.sh/blog/2019/java-hello-world-at-platform.sh/)
* [Apache Tomcat](http://tomcat.apache.org/)
* [Eclipse MicroProfile](https://microprofile.io/)
* [Java at Platform.sh](https://docs.platform.sh/languages/java.html)
* [PLATFORM_PROJECT_ENTROPY](https://docs.platform.sh/development/variables.html#platformsh-provided-variables)