---
title: "Category API"
url: /apidocs-mxsdk/apidocs/category-api/
type: swagger
description: "The Category API manages the catogories for cataloguing your projects."
weight: 100
restapi: true
---

## Introduction

The Mendix Category API allows Mendix admins to create, edit or delete the category fields and their respective values for catagorizing your projects. 

## Authentication {#authentication}

Authentication for the Projects API uses a personal access token (PAT).

### Generating a PAT {#generate}

For details on how to generate a PAT, see the [Personal Access Tokens](/mendix-profile/user-settings/#pat) section of *User Settings*.

Select at least the following as **Epics** scopes:

* `mx:app:customfields:read` – to perform `GET` operations
* `mx:app:customfields:write` – to perform all operations (`GET`, `POST`, `PATCH`, and `DELETE`)

Store the generated value somewhere safe so you can use it to authorize your API calls.

### Using the PAT

Each request must contain an `Authorization` header with the value `MxToken {GENERATED_PAT}`. For example:

```http
GET /projects HTTP/1.1
Authorization: MxToken 7LJE…vk
```

## API Reference{#api-reference}

{{% alert color="warning" %}}
You cannot call endpoints in the Swagger UI below on this page.
{{% /alert %}}

{{< swaggerui-disable-try-it-out src="/openapi-spec/custom-field-api.yaml"  >}}
