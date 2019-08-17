# Docker Randomx Benchmark

Run `randomx-benchmark` using Docker.

This image clones `https://github.com/tevador/RandomX.git` and builds it according to instructions.

## Usage

Append any `randomx-benchmark` params after the image name. i.e:

```shell
docker run -it --rm lchaia/randomx-benchmark --verify --jit
```

## Docker Compose example

```yaml
version: "3"

services:
  randomx-benchmark:
    image: lchaia/randomx-benchmark
    container_name: randomx-benchmark
    command: --verify --jit
```

## Copyrights

Code from this repository is released under MIT license.
RandomX code is released under BSD-3-Clause

[RandomX Acknowledgements](https://github.com/tevador/RandomX#acknowledgements)

## Donations

Please consider [donating to the RandomX team](https://github.com/tevador/RandomX#donations).
