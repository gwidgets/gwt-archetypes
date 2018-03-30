[![Build Status](https://travis-ci.org/gwidgets/gwt-ui-archetypes.svg?branch=master)](https://travis-ci.org/gwidgets/gwt-ui-archetypes)

## Description

This project provides a set of archetypes for starting your GWT application. 


## Available archetypes

The available archetypes are:
  - gwt-simple: minimal ready to run gwt project with an empty entry point class. It makes use of the `net.ltgt.gwt.maven` maven plugin. To run dev mode: `mvn gwt:devmode`. More info on goals and configuration can be found on the plugin's [documentation].
  - gwt-simple-mojo-plugin: same as `gwt-simple` except that it uses the `org.codehaus.mojo` plugin. To run dev mode: `mvn package gwt:run`. More info on goals and configuration can be found on the plugin's [documentation].
  - spring-security-gwt: This archetype is based on the example provided in our blog post on how to [secure a GWT application using Spring Security](http://www.g-widgets.com/2016/12/09/securing-a-gwt-app-using-spring-security/). It is a multi module application with a client module, which the GWT application, and a server module which provides authorization and authentication for accessing the application. The project makes use of the Jetty maven plugin as well as the `net.ltgt.gwt.maven` [GWT maven plugin](https://tbroyer.github.io/gwt-maven-plugin/).

  - spring-boot-gwt: This archetype is an integration of GWT into a spring boot application. There are two predefined profiles for running GWT dev mode and for running the application in production. To run the spring boot app with GWT in devmode you need to run the following commands: `mvn spring-boot:run` and in a different window `mvn gwt:devmode -Pgwt-dev`. If you don't need to you use GWT devmode and you need to run or package the application you can use the gwt-prod profile. For example: `mvn package -Pgwt:prod`. Spring Boot version: 1.5.2.RELEASE, GWT version: 2.8.0. This archetypes uses the `net.ltgt.gwt.maven` GWT plugin.

## Usage

On Windows:

    mvn archetype:generate -DarchetypeGroupId=com.gwidgets.maven                ^
      -DarchetypeArtifactId={artifactName}          ^
      -DarchetypeVersion=0.4-SNAPSHOT                ^
      -DgroupId={yourGroupId}                               ^
      -DartifactId={yourArtifactID}                            ^
      -Dmodule={moduleName}                                  ^
      -Dversion={yourVersion}

On Linux/Mac Os: 

        mvn archetype:generate -DarchetypeGroupId=com.gwidgets.maven                \
      -DarchetypeArtifactId={artifactName}          \
      -DarchetypeVersion=0.4-SNAPSHOT                \
      -DgroupId={yourGroupId}                                \
      -DartifactId={yourArtifactID}                             \
      -Dmodule={moduleName}                                   \
      -Dversion={yourVersion}


## Demos:

- spring-security-gwt: [https://gwt-spring-security.herokuapp.com/GwtSpringSecurity.html](https://gwt-spring-security.herokuapp.com/GwtSpringSecurity.html)
  * username: gwidgets, password: gwidgets