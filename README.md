# delphi-elk

In order to deploy the ELK stack you have to follow below steps

## Step 1: Install ECK operator in your cluster:

  ``kubectl apply -f https://download.elastic.co/downloads/eck/1.2.1/all-in-one.yaml``

## Step 2: Install Elasticsearch:

  ``kubectly apply -f elasticsearch.yml``

## Step 3: Install kibana:

  ``kubectl apply -f kibana.yml``


## To get password of Elasticsearch cluster:

  ``kubectl get secret elasticsearch-es-elastic-user -n elasticsearch -o go-template='{{.data.elastic | base64decode}}'``

