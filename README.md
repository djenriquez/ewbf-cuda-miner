# ewbf-cuda-miner
ewbf-miner for zcash

# Summary
Dockerizes the ewbf-miner binary. Run the docker container as if it were the actual binary, simply pass in flags.

# Run
```
$: docker run --rm -t \
--runtime=nvidia \
djenriquez/ewbf-cuda-miner

+-------------------------------------------------+
|         EWBF's Zcash CUDA miner. 0.3.4b         |
+-------------------------------------------------+
--help, -h          Show this help.
--server            Stratum server only hostname or ip address.
--port              Stratum server port.
--user              Stratum user.
--pass              Stratum password.
--fee               The developer fee in percent allowed decimals for example 0, 1, 2.5, 1.5 etc.
--pec               Power efficiency calculator. Shows power statistics.
--cuda_devices      Space-separated list of cuda devices.
                    Without this option all devices are used.
--solver            Disable benchmark and use specified solver
                    Allowed values from 0 to 3.
--eexit             Exit in case of error. Value 1 exit if miner cannot restart workers.
                    Value 2 if lost connection with the pool. 3 both cases.
--log               Create file miner.log in directory of miner.
                    Allowed values 1 and 2. 1 only errors, 2 will repeat console output.
--logfile           Set custom filename.
--config            Config file.
--tempunits         Temperature units, allowed values: C for celsius, F for fahrenheit and K for kelvin :)).
--templimit         Temperature limit, gpu will be stopped if this limit is reached.
--api               Enable api without an argument will be listen on 127.0.0.1:42000,
                    You can set listen address as an argument for example: --api 0.0.0.0:12345
                    Allowed ports 1000 - 65535

Example1: miner --server server.com --port 7777 --user name --pass secret --cuda_devices 0 1 2 3 --eexit 1
Example2: miner --server server.com --port 7777 --user name --pass secret --eexit 1 --log 2 --solver 1
$: 

```

## Example
```
docker run -d -t \
--name ewbf-miner \
--restart always \
--runtime=nvidia \
djenriquez/ewbf-cuda-miner \
--server equihash.usa.nicehash.com --port 3357 --user 33DyXVuy3R5jfLZRRpEQcXXAJ1Xz5rkGxE --pass x --eexit
```
# Dependencies
- nvidia GPUs
- CUDA drivers for your machine, see https://developer.nvidia.com/cuda-downloads?target_os=Linux
- [nvidia-docker](https://github.com/NVIDIA/nvidia-docker)

## Donations
- BTC - 33DyXVuy3R5jfLZRRpEQcXXAJ1Xz5rkGxE
- LTC - MUaov1JidbnpfeuQiSR3mtJhN3CN8Wj5g9
- ETH - 0xCBBC579Ac1Bc4868823fbBb2D8dDaFF93D619ceD
- DASH - Xy4cgJVAiHsrbeBB53NeQWk2iXKoWjBvJp
- ZEC - t1gYs8Zn2ZCFZWKZsTmZWd5bgXa9eD8M87K
- BCH - LOL