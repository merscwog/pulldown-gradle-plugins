# pulldown-gradle-plugins

Crude code to be able to pull down the direct plugins found on the plugin portal
(this does not attempt to download transitive dependencies)

The below command will download the jar and all direct dependencies of all the plugins from the plugins.gradle.org portal,
including pom files.

<pre>
./gradlew -PearliestDate='01 Nov 2016' readWebSite
</pre>

If a setting for earliestDate is not applied, then it will default to 10 January 1970, which essentially just means everything.
Also note that since this is implemented as part of a gradle build, the commmands can be simply reduced to their camel-case
unambiguous form.  rWS will be interepreted as readWebSite, since no other task matches.

<pre>
./gradlew rWS
</pre>

Again, this is very, very rudimentary, and plenty of other capabilities could be easily added.
