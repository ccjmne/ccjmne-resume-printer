# ccjmne-resume-printer

Printing (possibly old) versions of [ccjmne-resume](https://github.com/ccjmne/ccjmne-resume) to PDF or thumbnails.

```shell
DATE=2017-03-10 OUTPUT=2017-03-10.png THUMBNAIL=yes tsx printer.ts
```

Example pipeline:

```shell
git checkout 1.0.0
yarn install
npx webpack --mode production
DATE=$(git log -1 --format=%aI | cut -d'T' -f1) OUTPUT=$DATE     tsx path/to/printer.ts
DATE=$(git log -1 --format=%aI | cut -d'T' -f1) OUTPUT=$DATE.png tsx path/to/printer.ts
```
