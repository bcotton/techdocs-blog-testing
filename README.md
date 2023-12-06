# techdocs-blog-testing

To reproduce this error you have to build a custom image of the techdocs container, as a version of the conatiner with v1.3 of the techdocs-plugin has not been released:
[When do new releases of the docker images get cut? · Issue #65 · backstage/techdocs-container](https://github.com/backstage/techdocs-container/issues/65)

```
git clone git@github.com:backstage/techdocs-container.git 
git clone git@github.com:backstage/mkdocs-techdocs-core.git
cd mkdocs-techdocs-core 
./build-e2e-image.sh 
```

Then in this repo:
```
cd docs
techdocs-cli serve -v -c mkdocs.yml --docker-image mkdocs:local-dev

```
