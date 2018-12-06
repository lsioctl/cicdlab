# CI/CD LAB

## prepare the Heroku CLI image

```
cd hk
docker login registry.gitlab.com
docker build -t registry.gitlab.com/laurent.steff/cicdlab/hk:*version* .
docker push registry.gitlab.com/laurent.steff/cicdlab/hk:*version*
```

