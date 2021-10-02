# Asset SASS Plugin Not Compiling




```shell
./gradlew assetCompile

```

Results in uncompiled gzip'd scss assets.

```
build/assets/sassy-955cd1ddad81e40ffcdc9fb0c0a7620a.scss.gz
build/assets/sassy-955cd1ddad81e40ffcdc9fb0c0a7620a.scss
build/assets/sassy.scss.gz
build/assets/sassy.scss
```

According to https://github.com/bertramdev/sass-grails-asset-pipeline

it states the imports should be compiled names.
```
<asset:stylesheet src="sassy.css"/>

```

I know thats old, but for completeness, I tried both.
```
<asset:stylesheet src="sassy.scss"/>

```

```
./gradlew bootRun
Grails application running at http://localhost:8080 in environment: development
```
works

```
./gradlew bootWar
java -jar ./build/libs/sassy-0.1.war 
Grails application running at http://localhost:8080 in environment: production
```
but building results in uncompiled files and 404s because built scss .css files do not exist.