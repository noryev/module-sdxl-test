# SDXL v0.9 in Docker 🐋

```
export HUGGINGFACE_TOKEN=<my huggingface token>
```
```
docker build -t sdxl:v0.9 --build-arg HUGGINGFACE_TOKEN=$HUGGINGFACE_TOKEN .
```
```
mkdir -p outputs
```
```
docker run -ti --gpus all \
    -v $PWD/outputs:/outputs \
    -e OUTPUT_DIR=/outputs/ \
    -e PROMPT="a lilypad on a galaxy of water" \
     stable-diffusion-xl:latest
```
Will overwrite `outputs/image0.png` each time.

## Running on Lilypad

Anatomy of a lilypad run command



Local `./stack run --network dev github.com/noryev/module-sdxl:42e8521e2b77325f8fc56fc2246e97d840f12dba`

Testnet `lilypad run github.com/noryev/module-sdxl:42e8521e2b77325f8fc56fc2246e97d840f12dba`