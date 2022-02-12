commons-lang-api Plugin
===================

[![Jenkins Plugin](https://img.shields.io/jenkins/plugin/v/commons-lang-api-plugin.svg)](https://plugins.jenkins.io/commons-lang-api-plugin)
[![Build Status](https://ci.jenkins.io/buildStatus/icon?job=Plugins/commons-lang-api-plugin/main)](https://ci.jenkins.io/blue/organizations/jenkins/Plugins%2Fcommons-lang-api-plugin/activity/)
[![Jenkins Plugin Installs](https://img.shields.io/jenkins/plugin/i/commons-lang-api-plugin.svg?color=blue)](https://plugins.jenkins.io/commons-lang-api-plugin)

This plugin provides [Commons Lang v2.x](https://commons.apache.org/proper/commons-lang/) to Jenkins Plugins.<br>

Version will be "&lt;commons-lang version&gt;_&lt;plugin version&gt;", so clear what upstream dependency it is offering and plugin can be patch by "plugin version" if required.


## How to introduce to your plugin

### Plugins directly depending on httpclient

Replace the dependency to `org.apache.httpcomponents:httpclient` with the dependency to `apache-httpcomponents-client-4-api`.

* Before:
    ```
    <dependencies>
      ...
      <dependency>
        <groupId>commons-lang</groupId>
        <artifactId>commons-</artifactId>
        <version>2.6</version>
      </dependency>
      ...
    </dependencies>
    ```
* After:
    ```
    <dependencies>
      ...
      <dependency>
        <groupId>org.jenkins-ci.plugins</groupId>
        <artifactId>commons-lang-api-plugin</artifactId>
        <version>2.6_0</version>
      </dependency>
      ...
    </dependencies>
    ```

### Change Log

#### Version 2.6_0 (Feb TBC, 2022)
- First release
- Looks at breaking plugin dependencies upon core jenkins, as discussed [[PR#6267](https://github.com/jenkinsci/jenkins/pull/6267#issuecomment-1036644004)] and Jenkins Core update by [[PR#6270](https://github.com/jenkinsci/jenkins/pull/6270)].
