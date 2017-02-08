# Avas Load Balancer

## Usage

You will only need to install the unit file it will pull everything else it needs automatically and it will automatically pull the latest version of the image every time it restarts.


**NOTE**: This is a private repo so for docker to pull the image correctly you have to be logged into docker.

##### If not logged in you need to:
```
docker login -u callforamerica -p <pass>
```


### Install the avaslb.service systemd unit:
```bash
cp avaslb.service /etc/systemd/system/
```

### Start the avaslb.service:
```bash
systemctl start avaslb
```

### If everything is working set it to auto start:
```bash
systemctl enable avaslb
```

## How to

### Get logs
```bash
# without follow
docker logs avaslb

# with follow
docker logs -f avaslb
```

## Restart container
```bash
systemctl restart avaslb
```

## Stop container
```bash
systemctl stop avaslb
```

## Start container
```bash
systemctl start avaslb
```

## Disable from auto starting
```bash
systemctl disable avaslb
```
