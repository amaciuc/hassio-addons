# Redis Stack

### Visit the official [documentation](https://redis.io/about/about-stack/)

## Docker Image

[Here](https://redis.io/docs/latest/operate/oss_and_stack/install/install-stack/docker/) is the documentation how to deploy the `redis-stack` as docker container.

### [Enviroment variables](https://redis.io/docs/latest/operate/oss_and_stack/install/install-stack/docker/#environment-variables)

#### REDIS_ARGS

Explanation why I chose default values for `REDIS_ARGS`.
- `--save 60 1000`: [doc](https://redis.io/docs/latest/operate/oss_and_stack/management/persistence/#snapshotting)
- `--appendonly yes`: [doc](https://redis.io/docs/latest/operate/oss_and_stack/management/persistence/#append-only-file)

#### REDISTIMESERIES_ARGS [parameters](https://redis.io/docs/latest/develop/data-types/timeseries/configuration/#redistimeseries-configuration-parameters)

**OBS!** This env variable could be passed at runtime, but right now, this is disabled. Only `REDIS_ARGS` is enabled and its value can be found [here](https://github.com/amaciuc/hassio-addons/blob/876e365a6ced5038a4e900bc7899287de212ee8c/redis-stack/config.yaml#L35)