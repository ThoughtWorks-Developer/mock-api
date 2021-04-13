
## Run Locally

### Combine Technology data

```
jq -n '{ technologies: [ inputs ] | add }' *.json > db.json
```

### Start Json Server

```
json-server --watch db.json
```