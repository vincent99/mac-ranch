## Wrapper to deploy Rancher on Docker for Mac / xhyve
=====
Prerequisites:

- Docker for Mac (http://beta.docker.com)
- docker-machine-driver-xhyve (https://github.com/zchee/docker-machine-driver-xhyve)

=========
Usage:
```
mac-ranch Usage:
    mac-ranch [opts]
    -c - Create world
    -d - Destroy world
    -h - Print this message
    -l - List hosts
    -r registration_url - Register another "-n" hosts using the given registration url

    -M - Host memory in MB (default: 512)
    -n - Number of hosts (default: 3)
    -p - privileged (needed for build-master)
    -s - Server Container (default: rancher/server:latest)
            needs full container repo/name[:tag] 
```

### To deploy:

```
./mac-ranch -c -n <number of hosts>
```

#### A specific release
```
./mac-ranch -c -n <number of hosts> -s rancher/server:development
```

#### A build-master
```
./mac-ranch -c -s rancher/build-master -p -n <number of hosts>
```

### List all the hosts
```
./mac-ranch -l
```

### Destroy the cluster
```
./mac-ranch -d
```

### Contact
For bugs, questions, comments, corrections, suggestions, etc., open an issue in [rancher/rancher](//github.com/rancher/rancher/issues) with a title starting with `[mac-ranch] `.

Or just [click here](//github.com/rancher/rancher/issues/new?title=%5Bmac-ranch%5D%20) to create a new issue.

# License
Copyright (c) 2016 [Rancher Labs, Inc.](http://rancher.com)

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

[http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
