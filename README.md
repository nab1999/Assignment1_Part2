# Assignment1_Part2

## Part 2: Docker Containers with Commands

### Step1: (Using the docker image from Part 1)

In this Part 2 of the assignment, we will be using the same docker image “app1_img” which was created in previous step1.

![image](https://user-images.githubusercontent.com/126570628/227045084-60263847-a3c1-4c0e-9ff8-28f75a702e47.png)

### Step2: (Run the Docker Container)

In this step, we will create a docker container with the image “app1_img” by using the command: “docker run -p 5000:5000 -d app1_img”. This command runs the container and its embedded application, each on port 5000 using a port-binding approach. The first 5000 is the port that we allocate to the container on our machine. The second 5000 is the port where the application will run on the container. We can verify that the container is running by using the command “docker ps” as shown in below output.

![image](https://user-images.githubusercontent.com/126570628/227045283-cbe56c66-fd04-4e44-9150-8447590d9aab.png)

Output of our flask app can be accessed on the local machine CLI when we send a request to localhost:5000 as show in below figure by using the “curl localhost:5000” command.

![image](https://user-images.githubusercontent.com/126570628/227045463-37da1cfd-c9c5-4bdf-9403-d7690d1af776.png)

### Step3: (Use Different Docker Container Commands)

#### Section 3.1.0 ('docker ps' command to list all running containers):

![image](https://user-images.githubusercontent.com/126570628/227046056-cfa0275d-25b2-4491-85ec-e02f996176be.png)

#### Section 3.1.1 (‘docker stop' command to stop a running container):

#### Section 3.1.2 ('docker rm' command to remove a stopped container):

#### Section 3.1.3 ('docker logs' command to view the logs of a container):

![image](https://user-images.githubusercontent.com/126570628/227046216-bb910a94-69d0-4763-b40c-418d2fdc1ec8.png)

#### Section 3.1.4 ('docker inspect' command to view the details of a container):

#### OUTPUT:

root@ubuntu1:/home/nabeel/assignment1_part1# docker inspect 3cba77cad15b

[
    {
        "Id": "3cba77cad15bae638fff346548a6b68bc48ff8c608a938ad70b93d0ed8a63457",
        "Created": "2023-03-22T17:03:17.051098727Z",
        "Path": "python",
        "Args": [
            "app1.py"
        ],
        "State": {
            "Status": "running",
            "Running": true,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 3000,
            "ExitCode": 0,
            "Error": "",
            "StartedAt": "2023-03-22T17:03:17.385908305Z",
            "FinishedAt": "0001-01-01T00:00:00Z"
        },
        "Image": "sha256:af4b5ca2ba1791e50e857cbb2da012280b0768b149ff799f5acb4e7c3bf7c5b2",
        "ResolvConfPath": "/var/snap/docker/common/var-lib-docker/containers/3cba77cad15bae63                                                                                                8fff346548a6b68bc48ff8c608a938ad70b93d0ed8a63457/resolv.conf",
        "HostnamePath": "/var/snap/docker/common/var-lib-docker/containers/3cba77cad15bae638f                                                                                                ff346548a6b68bc48ff8c608a938ad70b93d0ed8a63457/hostname",
        "HostsPath": "/var/snap/docker/common/var-lib-docker/containers/3cba77cad15bae638fff3                                                                                                46548a6b68bc48ff8c608a938ad70b93d0ed8a63457/hosts",
        "LogPath": "/var/snap/docker/common/var-lib-docker/containers/3cba77cad15bae638fff346                                                                                                548a6b68bc48ff8c608a938ad70b93d0ed8a63457/3cba77cad15bae638fff346548a6b68bc48ff8c608a938ad70b                                                                                                93d0ed8a63457-json.log",
        "Name": "/tender_sanderson",
        "RestartCount": 0,
        "Driver": "overlay2",
        "Platform": "linux",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "docker-default",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": null,
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "default",
            "PortBindings": {
                "5000/tcp": [
                    {
                        "HostIp": "",
                        "HostPort": "5000"
                    }
                ]
            },
            "RestartPolicy": {
                "Name": "no",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "CapAdd": null,
            "CapDrop": null,
            "CgroupnsMode": "host",
            "Dns": [],
            "DnsOptions": [],
            "DnsSearch": [],
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "private",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": 0,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": null,
            "UTSMode": "",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "ConsoleSize": [
                49,
                189
            ],
            "Isolation": "",
            "CpuShares": 0,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "",
            "BlkioWeight": 0,
            "BlkioWeightDevice": [],
            "BlkioDeviceReadBps": [],
            "BlkioDeviceWriteBps": [],
            "BlkioDeviceReadIOps": [],
            "BlkioDeviceWriteIOps": [],
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": [],
            "MaskedPaths": [
                "/proc/asound",
                "/proc/acpi",
                "/proc/kcore",
                "/proc/keys",
                "/proc/latency_stats",
                "/proc/timer_list",
                "/proc/timer_stats",
                "/proc/sched_debug",
                "/proc/scsi",
                "/sys/firmware"
            ],
            "ReadonlyPaths": [
                "/proc/bus",
                "/proc/fs",
                "/proc/irq",
                "/proc/sys",
                "/proc/sysrq-trigger"
            ]
        },
        "GraphDriver": {
            "Data": {
                "LowerDir": "/var/snap/docker/common/var-lib-docker/overlay2/eaa1e35a2c5f5001                                                                                                49b7bee64b83ee66fa2613a3613c18f4ab3e511f9b39a5fb-init/diff:/var/snap/docker/common/var-lib-do                                                                                                cker/overlay2/w1vcqgeomhpsgqzd090yb578n/diff:/var/snap/docker/common/var-lib-docker/overlay2/                                                                                                jssukl6cbzu3ldklrditfwvzm/diff:/var/snap/docker/common/var-lib-docker/overlay2/6jhs5xasd7t5e7                                                                                                tcef9p92dj7/diff:/var/snap/docker/common/var-lib-docker/overlay2/dq4seeum6yudjuy1gp8gcrcax/di                                                                                                ff:/var/snap/docker/common/var-lib-docker/overlay2/48647e48dfce620b18b25c72e76e1f84bd6cfd8a7a                                                                                                fcf9865eede11e950412d1/diff:/var/snap/docker/common/var-lib-docker/overlay2/826dbe61c17abe709                                                                                                38ea098b952a51026be401f0bc9c1c3ea90061c4644e636/diff:/var/snap/docker/common/var-lib-docker/o                                                                                                verlay2/c64b44c84d4a7a069f8c824251528f097e0e2a9b96c6dc475ba22e27597d7706/diff:/var/snap/docke                                                                                                r/common/var-lib-docker/overlay2/452d334c266fc66a1f36cac4643006a13f06d74c57a3384ef8f09d1e8970                                                                                                2bc6/diff:/var/snap/docker/common/var-lib-docker/overlay2/b88509940f87f926ffd0acd99e73b10fa92                                                                                                9c48571c4c76cae70ecf3d12fca19/diff",
                "MergedDir": "/var/snap/docker/common/var-lib-docker/overlay2/eaa1e35a2c5f500                                                                                                149b7bee64b83ee66fa2613a3613c18f4ab3e511f9b39a5fb/merged",
                "UpperDir": "/var/snap/docker/common/var-lib-docker/overlay2/eaa1e35a2c5f5001                                                                                                49b7bee64b83ee66fa2613a3613c18f4ab3e511f9b39a5fb/diff",
                "WorkDir": "/var/snap/docker/common/var-lib-docker/overlay2/eaa1e35a2c5f50014                                                                                                9b7bee64b83ee66fa2613a3613c18f4ab3e511f9b39a5fb/work"
            },
            "Name": "overlay2"
        },
        "Mounts": [],
        "Config": {
            "Hostname": "3cba77cad15b",
            "Domainname": "",
            "User": "",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "ExposedPorts": {
                "5000/tcp": {}
            },
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:                                                                                                /bin",
                "LANG=C.UTF-8",
                "GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568",
                "PYTHON_VERSION=3.8.16",
                "PYTHON_PIP_VERSION=22.0.4",
                "PYTHON_SETUPTOOLS_VERSION=57.5.0",
                "PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d5cb0afaf23b8520f1bbc                                                                                                fed521017b4a95f5c01/public/get-pip.py",
                "PYTHON_GET_PIP_SHA256=394be00f13fa1b9aaa47e911bdb59a09c3b2986472130f30aa0bfa                                                                                                f7f3980637"
            ],
            "Cmd": [
                "app1.py"
            ],
            "Image": "app1_img",
            "Volumes": null,
            "WorkingDir": "/app",
            "Entrypoint": [
                "python"
            ],
            "OnBuild": null,
            "Labels": {}
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "715c9f74652c2cc4e4635003ec975bab386a141c6b0b7fec3378ef69676a91b1",
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "Ports": {
                "5000/tcp": [
                    {
                        "HostIp": "0.0.0.0",
                        "HostPort": "5000"
                    },
                    {
                        "HostIp": "::",
                        "HostPort": "5000"
                    }
                ]
            },
            "SandboxKey": "/run/snap.docker/netns/715c9f74652c",
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "a1992e782b63a81c190e31679eac6cde4b41b54642a7d630929de374e0ab2022",
            "Gateway": "172.17.0.1",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "172.17.0.2",
            "IPPrefixLen": 16,
            "IPv6Gateway": "",
            "MacAddress": "02:42:ac:11:00:02",
            "Networks": {
                "bridge": {
                    "IPAMConfig": null,
                    "Links": null,
                    "Aliases": null,
                    "NetworkID": "dfb426cfdcbafffddbe38282a3c842ab3ef9e4a93fa888ba6ade5f1f255                                                                                                16c5d",
                    "EndpointID": "a1992e782b63a81c190e31679eac6cde4b41b54642a7d630929de374e0                                                                                                ab2022",
                    "Gateway": "172.17.0.1",
                    "IPAddress": "172.17.0.2",
                    "IPPrefixLen": 16,
                    "IPv6Gateway": "",
                    "GlobalIPv6Address": "",
                    "GlobalIPv6PrefixLen": 0,
                    "MacAddress": "02:42:ac:11:00:02",
                    "DriverOpts": null
                }
            }
        }
    }
]


#### Section 3.1.5 ('docker exec' command to execute a command inside a running container):

![image](https://user-images.githubusercontent.com/126570628/227047031-191bd24e-ee05-4645-bef3-819ee5fcdf2d.png)

#### Section 3.1.6 ('docker attach' command to attach to a running container):

![image](https://user-images.githubusercontent.com/126570628/227047207-36f928f6-bb52-419a-b3f6-eebd49216b8a.png)

#### Section 3.1.7 ('docker commit' command to create a new image from a container):

![image](https://user-images.githubusercontent.com/126570628/227047447-f862119c-3871-4332-be57-2a700147ca50.png)

#### Section 3.1.8 ('docker cp' command to copy files/folders between the container and the host):

![image](https://user-images.githubusercontent.com/126570628/227047655-703b24d2-7730-408b-9ed1-7ec34a5358ef.png)

![image](https://user-images.githubusercontent.com/126570628/227047701-253cad11-c8fd-44d2-9e7f-1b85afbf07d6.png)

#### Section 3.1.9 ('docker stats' command to view the resource usage of containers):

![image](https://user-images.githubusercontent.com/126570628/227047796-b5f7c8a3-9f08-4d37-80a1-d8721b22df23.png)

![image](https://user-images.githubusercontent.com/126570628/227047860-2897c832-9275-4797-81f4-67529995ef68.png)

#### Section 3.2.0 (‘docker pause' command to pause a running container):

![image](https://user-images.githubusercontent.com/126570628/227047985-61307f94-d235-49aa-ae81-f59daaa754e6.png)

#### Section 3.2.1 ('docker unpause' command to unpause a paused container):

![image](https://user-images.githubusercontent.com/126570628/227048090-d4384cc0-8836-4cfd-a073-dbe618d675f8.png)

#### Section 3.2.2 ('docker rename' command to rename a container):

![image](https://user-images.githubusercontent.com/126570628/227048171-c0ce536d-8830-4fa4-81e7-5f4ca5a61f5f.png)

#### Section 3.2.3 ('docker wait' command to wait for a container to exit and then display its exit code):

#### Section 3.2.4 ('docker attach' command to attach local standard input, output, and error streams to a running container):

![image](https://user-images.githubusercontent.com/126570628/227048290-da90f41f-b137-49ea-b293-3939272b18bd.png)

#### Section 3.2.5 ('docker port' command to display the public-facing port that a container is listening on):

![image](https://user-images.githubusercontent.com/126570628/227048375-66319792-23bd-41de-b2a4-91ba448da1c8.png)

#### Section 3.2.6 ('docker update' command to update a container's resource limits):

The docker update command dynamically updates container configuration. We can use this command to prevent containers from consuming too many resources from their Docker host. Example is shown below for limiting the container’s cpu-shares to 512.

![image](https://user-images.githubusercontent.com/126570628/227048507-55b2d78f-ea06-4c25-b13e-5ce4b12549f1.png)

#### Section 3.2.7 ('docker restart' command to restart a running container):

