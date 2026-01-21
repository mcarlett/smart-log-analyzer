# smart-log-analyzer

Run local infra with docker-compose `cd containers && docker-compose up`

Run the analyzer with `jbang -Dcamel.jbang.version=4.17.0 camel@apache/camel run error-analyzer.camel.yaml`

Run the correlator with `jbang -Dcamel.jbang.version=4.17.0 camel@apache/camel run traces-mapper.camel.yaml logs-mapper.camel.yaml infinispan.camel.yaml kaoto-datamapper-4a94acc3.xsl kaoto-datamapper-8f5bb2dd.xsl`

Run the log-generator with `jbang --javaagent=./opentelemetry-javaagent.jar -Dotel.javaagent.configuration-file=./agent.properties --deps org.apache.camel:camel-opentelemetry2 -Dcamel.jbang.version=4.17.0 camel@apache/camel run log-generator.camel.yaml`
