FROM grokzen/redis-cluster:7.0.10

RUN sed -i 's/appendonly yes/appendonly no/g' /redis-conf/redis-cluster.tmpl \
    && echo 'save ""' >> /redis-conf/redis-cluster.tmpl \
    && echo 'protected-mode no' >> /redis-conf/redis-cluster.tmpl \
    && sed -i 's/autorestart=true/autorestart=unexpected/g' /generate-supervisor-conf.sh

