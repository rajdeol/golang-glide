# Golang glide container

This is golang 1.8 container with glide 0.12.3 built from source and compiled into a binary.
# Build:
```sh
 docker build . -t rajdeol/golang-glide
```

# Use as command line :
```sh
docker run --rm \
    --name=glide-$$ \
    -v $(pwd):/path-of-your-project \
# required if private repositiories are added in the glide.yml file
    -v ~/.ssh/id_rsa:/root/.ssh/id_rsa \
    -v ~/.ssh/id_rsa.pub:/root/.ssh/id_rsa.pub \
    -v ~/.ssh/known_hosts:/root/.ssh/known_hosts \
    -w "/path-of-your-project" \
    rajdeol/golang-glide ${*}
```
