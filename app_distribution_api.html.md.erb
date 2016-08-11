---
title: APIs for CI Integration
---
<br/>
Prerequisites

- **Version 1.1.1.0** of App Distribution
- **Administrator/Member** access to a project on App Distribution

- **App Distribution url**: Base url of the app distribution instance

- **Phase ID**: this can be retrieved by hovering over the Phase Title in the 'Builds' Section

- **API Token**: this can be retrieved clicking on your user name at the top right of the screen, click on 'View Profile', then copy the API token that appears in the popup window

- **Build ID** - this can be retrieved from the url on the specific build page - i.e. https://<app\_distribution\_url/#/projects/.../build/releases/**[build\_id]**



<br/>

## API
<br/>
Parameters to the app-distribution API are passed as form field data in an HTTP request.

### Creating a Build

A build is a logical grouping of a set of files. Usually, they correspond to a single version of the app, meant to be sent out together to stakeholders.

`/api/v2/builds`


#### Parameters

| Name | Description |
| ---- | ----------- |
| `phase_id` | The integer id of the phase where the build will be added to |
| `api_token` | User's API token |


Note: Phase ID can be retrieved by hovering over the Phase Title in the 'Builds' Section


#### Response

| Description | Status | Example Body |
| ----------- | ------ | ------------ |
| Success | `201` | `{ id: 1 }` |
| Error: `phase_id` is missing | `422` |
| Error: User is unauthenticated | `401` |
| Error: User does not have the authority to create a build | `403` |


#### Example

```sh
curl -s -D- -H 'Authorization:Token token="<api_token>"' -X POST http://example.com/api/v2/builds -F "phase_id=<id>"
```


### Attaching Files to a Build

Files can be attached to the build. When the build is released, stakeholders will see links to all the files within.

`/api/v2/resource_files`


#### Parameters

| Name | Description |
| ---- | ----------- |
| `build_id` | The integer of the build to attach this file to |
| `file` | A reference to the file's path |



#### Response

| Description | Status | Example Body |
| ----------- | ------ | ------------ |
| Success | `201` | `{ id: 1 }` |
| Error: `build_id` is missing | `422` |
| Error: `file` is missing | `422` |
| Error: User is unauthenticated | `401` |
| Error: User does not have the authority to attach files | `403` |



#### Example

```sh
curl -s -D- -H 'Authorization:Token token="<access_token>"' http://example.com/api/v2/resource_files -F "build_id=<id>" -F "file=@/path/to/file.ext"
```
<br/>
<br/>

Upon successful upload, the file will appear in the "QA" section of the build page.

###Sample CI integration script
<br/>

Shown below is an example of how to setup these APIs using a bash script



```
curl -s -D- -H "Authorization:Token token=$API_TOKEN" -X POST $APP_DIST_URL/api/v2/builds -F phase_id=$PHASE_ID > build_response.json

build_id_json= `awk 'BEGIN { FS=":"} /"id"/ { print $2; }' build_response.json `
build_id_length=${#build_id_json}
build
_id=${build_id_json:0:build_id_length-1}

curl -s -D- -H "Authorization: Token token=$API_TOKEN" -X POST $APP_DIST_URL/api/v2/resource_files -F "build_id=$build_id" -F "file=@$OUTPUT_FILE_PATH"
```

<br/>

Parameters:

**API\_TOKEN**: User's API token

**PHASE\_ID** : Project phase ID

**APP\_DIST\_URL** (Base URL of the app-distribution instance )

**OUTPUT\_FILE\_PATH** (complete path with filename specifying location of built artifact)
