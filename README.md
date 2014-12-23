Runs a [Chronos](https://github.com/mesosphere/chronos/) instance.

Available on the Docker Index as [samiur/chronos](https://index.docker.io/u/samiur/chronos/):

    docker pull samiur/chronos

### Versions
* Chronos 2.3.0
* Mesos 0.21.0

### Usage
For Chronos to register with the Mesos cluster, you will need to enable host networking with `--net=host` (available in Docker 0.11+, see [announcement](http://blog.docker.io/2014/05/docker-0-11-release-candidate-for-1-0/)).

Starting the container:

    docker run \
        --net=host \
        -p 8081:8081 \
        samiur/chronos:latest \
        [CHRONOS_OPTIONS]

(See Chronos's [documentation](https://github.com/mesosphere/chronos/README.md) for available arguments)

Once the container is up, visit `http://<host>:8081/` and confirm Chronos is running.
