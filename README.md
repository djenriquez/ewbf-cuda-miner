# ewbf-cuda-miner
ewbf-miner for zcash

# Summary
Dockerizes the ewbf-miner binary. Run the docker container as if it were the actual binary, simply pass in flags.

# Run
```
$ docker run --rm -t \
djenriquez/ewbf-cuda-miner
```

## Example
```
docker run -d -t \
--name zecminer \
--restart always \
--runtime=nvidia \
djenriquez/ewbf-cuda-miner \
--server zcl.suprnova.cc --port 4042 --user t1Ri1WHEucpZJyEJER6NvfwsibcMw1NZMWV --pass x --eexit
```
