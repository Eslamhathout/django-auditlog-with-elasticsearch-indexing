django-auditlog-with-elasticsearch-indexing
===========================================

From Auditlog docs: Auditlog tries to use as much as Python and Django's built in functionality to keep the list of dependencies as short as possible. Also, Auditlog aims to be fast and simple to use.

django auditlog with elasticsearch indexing: A package that extends the auditlog functionalityies by indexing the logs to Elasticsearch insetead of inserting it to a relational database.

Prerequisites
-------------

In order to setup a communication channel with Elasticsearch, Override the `conf.py` file to add the Elasticsearch host, password and cloud_id.

conf.py: 
`
# Register all models when set to True
settings.AUDITLOG_INCLUDE_ALL_MODELS = getattr(
    settings, "AUDITLOG_INCLUDE_ALL_MODELS", False
)

# Exclude models in registration process
# It will be considered when `AUDITLOG_INCLUDE_ALL_MODELS` is True
settings.AUDITLOG_EXCLUDE_TRACKING_MODELS = getattr(
    settings, "AUDITLOG_EXCLUDE_TRACKING_MODELS", ()
)

# Register models and define their logging behaviour
settings.AUDITLOG_INCLUDE_TRACKING_MODELS = getattr(
    settings, "AUDITLOG_INCLUDE_TRACKING_MODELS", ()
)

# Disable on raw save to avoid logging imports and similar
settings.AUDITLOG_DISABLE_ON_RAW_SAVE = getattr(
    settings, "AUDITLOG_DISABLE_ON_RAW_SAVE", False
)

# TODO: Elasticsearch configurations
ELASTIC_USER=''
ELASTIC_PASSWORD=''
CLOUD_ID=''
`
 
