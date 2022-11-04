# Docker Polkadot
My personal unprivileged Polkadot Docker image.  

[![Github tag (latest by date)][github-tag-badge]][github-tag-link]  
[![GitHub Workflow Status (branch)][github-actions-badge]][github-actions-link]

Usage:
```sh
docker run \
  -dit \
  --restart=always \
  --net=host \
  --name=polkadot \
  -v /path/to/polkadot:/data \
  ghcr.io/rblaine95/polkadot \
    --base-path=/data ${EXTRA_POLKADOT_ARGS}
```

### Nonroot
The nonroot user has a U/GID of `65532`.  
If you are having IO permission issues then make sure that the persistent volume has permissions set to allow this user Read/Write access.  
If using [Podman](https://podman.io/) - `podman unshare chown -R 65532:65532 /path/to/polkadot/storage`

### Where can I download the image?
I'm using Github Actions to build and publish this image to:
* [ghcr.io/rblaine95/polkadot](https://ghcr.io/rblaine95/polkadot)

### I want to buy you a coffee
This is just a hobby project for me, if you really want to buy me a coffee, thank you :)  

Monero: `83TeC9hCsZjjUcvNVH6VD64FySQ2uTbgw6ETfzNJa51sJaM6XL4NParSNsKqEQN4znfpbtVj84smigtLBtT1AW6BTVQVQGh`  
![XMR Address](https://api.qrserver.com/v1/create-qr-code/?data=83TeC9hCsZjjUcvNVH6VD64FySQ2uTbgw6ETfzNJa51sJaM6XL4NParSNsKqEQN4znfpbtVj84smigtLBtT1AW6BTVQVQGh&amp;size=150x150 "83TeC9hCsZjjUcvNVH6VD64FySQ2uTbgw6ETfzNJa51sJaM6XL4NParSNsKqEQN4znfpbtVj84smigtLBtT1AW6BTVQVQGh")

### I don't have Polkadot
You should read their [Lightpaper](https://polkadot.network/Polkadot-lightpaper.pdf) and check it out!
* [paritytech/polkadot](https://github.com/paritytech/polkadot)  
* [Polkadot.Network](https://polkadot.network/)  
* [/r/polkadot](https://www.reddit.com/r/polkadot)  
* [/r/dot](https://www.reddit.com/r/dot)


[github-tag-badge]: https://img.shields.io/github/v/tag/rblaine95/docker_polkadot "Github tag (latest by date)"
[github-tag-link]: https://github.com/rblaine95/docker_polkadot/tags
[github-actions-badge]: https://img.shields.io/github/workflow/status/rblaine95/docker_polkadot/Docker/master "Github Workflow Status (master)"
[github-actions-link]: https://github.com/rblaine95/docker_polkadot/actions?query=workflow%3ADocker
