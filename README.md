# [Smashing](https://github.com/dashing-io/smashing/wiki) Container

## Setup
No need for a dockerfile. Simply attach your dashboard directory as a volume and run the container.
```bash
# Run container with your own dashboard configuration
$ docker run -p 3030:3030 -v=/full/path/to/your/dashboard/:/dashboard suhussai/containerized-smashing
```

Or just run the dashboard using the default configurations.
```bash
# Run container with default dashboard configuration
$ docker run -p 3030:3030 suhussai/containerized-smashing
```

Port 3030 is the default port on which the dashboard runs on. It is, however, used as an environment variable so you can set your own using:
```bash
# Run container on port 8080
$ docker run -p 8080:8080 -e PORT=8080 suhussai/containerized-smashing
```
Or
```bash
# Run container on port 8080
$ docker run -p 8080:8080 suhussai/containerized-smashing start -p 8080
```
