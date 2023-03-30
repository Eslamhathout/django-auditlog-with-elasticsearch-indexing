django-auditlog-with-elasticsearch-indexing
===========================================

From Auditlog docs: Auditlog tries to use as much as Python and Django's built in functionality to keep the list of dependencies as short as possible. Also, Auditlog aims to be fast and simple to use.

django auditlog with elasticsearch indexing: A package that extends the auditlog functionalityies by indexing the logs to Elasticsearch insetead of inserting it to a relational database.

Prerequisites
-------------

In order to setup a communication channel with Elasticsearch, Override the `conf.py` file to add the Elasticsearch host, password and cloud_id.

conf.py: 

`# TODO: Elasticsearch configurations
ELASTIC_USER=''
ELASTIC_PASSWORD=''
CLOUD_ID=''
`
