# Heureka Fork

## Building (OSX and Windows)

Download the latest cacerts

```sh
wget -O /tmp/cacerts https://storage.googleapis.com/cloud.heurekasoftware.com/java-truststore/latest/cacerts
```

Install the JCE libraries into your

Run the tests with the downloaded cacerts

```sh
mvn clean source:jar install -Djavax.net.ssl.trustStore=/tmp/cacerts
```

Deploy to artifactory

```sh
mvn clean source:jar deploy -Djavax.net.ssl.trustStore=/tmp/cacerts
```
