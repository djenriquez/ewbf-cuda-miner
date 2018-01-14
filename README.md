# ewbf-cuda-miner
Run ewbf-miner for zcash

# Summary
Dockerizes the ewbf-miner binary. Run the docker container as if it were the actual binary, simply pass in flags.

# Run
```
docker run -d -t \
--name zecminer \
--restart always \
--runtime=nvidia \
djenriquez/ewbf-cuda-miner \
--server <STRATUM SERVER> --port <PORT> --user <USER/WALLET_ADDRESS> --pass <PASSWORD> --eexit
```

## Example
```
docker run -d -t \
--name zecminer \
--restart always \
--runtime=nvidia \
djenriquez/ewbf-cuda-miner \
--server zcl.suprnova.cc --port 4042 --user t1Ri1WHEucpZJyEJER6NvfwsibcMw1NZMWV --pass x --fee 0 --eexit
```
