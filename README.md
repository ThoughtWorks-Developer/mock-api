
## Run Locally

### Combine Technology data

```
jq -n '{ technologies: [ inputs ] | add }' technologies/*.json > technologies.json
```

### Combine Integrations data

```
jq -s . integrations/*.json > integrations.json
```

### Combine Software Templates data

```
jq -s . software_templates/*.json > software_templates.json
```

### Combine all data

```
jq s . technologies.json integrations.json software_templates.json > db.json
```

### Remove

```
rm -rf technologies.json integrations.json software_templates.json
```

### Start Json Server

```
json-server --routes routes.json --watch db.json
```