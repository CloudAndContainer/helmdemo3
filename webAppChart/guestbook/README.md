## Installing the Chart

To install the chart with your preference of release name, for example, `helmdemo3`:

```bash
$ helm install ./guestbook/ --name helmdemo3 --namespace helm-demo
```

### Uninstalling the Chart

To completely uninstall/delete the `my-release` deployment:

```bash
$ helm delete --purge helmdemo3
```

The command removes all the Kubernetes components associated with the chart and deletes the release.

## Configuration

The following tables lists the configurable parameters of the chart and their default values.

| Parameter                  | Description                                     | Default                                                    |
| -----------------------    | ---------------------------------------------   | ---------------------------------------------------------- |
| `image.repository`         | Image repository                                | `cloudandcontainer/helmguestbook`                                         |
| `image.tag`                | Image tag                                       | `latest`                                                       |
| `image.pullPolicy`         | Image pull policy                               | `Always`                                                   |
| `service.type`             | Service type                                    | `LoadBalancer`                                             |
| `service.port`             | Service port                                    | `3000`                                                     |
| `redis.slaveEnabled`       | Redis slave enabled                             | `true`                                                     |
| `redis.port`               | Redis port                                      | `6379`                                                     |

Specify each parameter using the `--set [key=value]` argument to `helm install`. For example,

```bash
$ helm install my-repo/guestbook --set service.type=NodePort
```
