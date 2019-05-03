# interproscan-environment-docker
Docker image to run Interproscan in Ubuntu 16.04

This is just the environment to run [Interproscan](https://github.com/ebi-pf-team/interproscan/wiki). The interproscan wrapper script and models still need to be downloaded - instructions [here](https://github.com/ebi-pf-team/interproscan/wiki/HowToDownload).
Once this is done and you can run the `interproscan.sh` script like so (remember that the data you want to access from within the container need to be below your mountpoint, which is `$(pwd)` in this case):
```bash
docker run --rm -v $(pwd):/in/ -w /in/ chrishah/interproscan-environment ./interproscan-5.32-71.0/interproscan.sh -h
```

The environment was tested with `Interproscan version 5.32-71.0`.
