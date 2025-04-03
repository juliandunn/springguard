# Example Java Project for Chainguard Libraries

Use an `$HOME/.m2/settings.xml` like this:

```
<settings>
  <mirrors>
    <mirror>
      <!--Send all requests to the Artifactory virtual repository -->
      <id>chainguard-libraries</id>
      <mirrorOf>*</mirrorOf>
      <url>https://maven.cloudsmith.io/your-tenant/your-repo/</url>
    </mirror>
  </mirrors>

  <activeProfiles>
    <activeProfile>chainguard-libraries</activeProfile>
  </activeProfiles>

  <profiles>
    <profile>
      <id>chainguard-libraries</id>
      <repositories>
        <repository>
          <id>central</id>
          <url>http://central</url>
          <releases>
            <enabled>true</enabled>
          </releases>
          <snapshots>
            <enabled>true</enabled>
          </snapshots>
        </repository>
      </repositories>
      <pluginRepositories>
        <pluginRepository>
          <id>central</id>
          <url>http://central</url>
          <releases>
            <enabled>true</enabled>
          </releases>
          <snapshots>
            <enabled>true</enabled>
          </snapshots>
        </pluginRepository>
      </pluginRepositories>
    </profile>
  </profiles>

  <servers>
    <server>
      <id>chainguard-libraries</id>
      <username>julian-dunn</username>
      <password>[elided]</password>
    </server>
  </servers>
</settings>
```
