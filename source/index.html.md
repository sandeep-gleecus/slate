---
title: Renyoo API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell: cURL

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='#'>Get the latest Postman collection</a> # must be linked to a GDrive with managed access
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to Renyoo API !! If you are here, you know what Renyoo is all about and chances are you've contributed, in whichever capacity, to make it what it is today. Yeah i know the negative connations .. that is intentional :).

So without much ado, lets do what you intend to do here. The UI is pretty self-explanatory and in this age of Digital Navigation, am pretty sure you will not be lost here.

Browse through the menu or search to find your endpoint of interest. Click on one to read about the endpoint in detail and go through the code examples and sample request/response to understand it better. Reach out to us [here](mailto:developer@renyoo.co) in case you need any further assistance. 

Do visit here often and more importantly, contribute to this documentation regularly and make the world a better place for your fellow devlopers.

# Authentication

> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: meowmeowmeow"
```

> Make sure to replace `meowmeowmeow` with your API key.

I am not sure if Renyoo uses API keys to allow access to the API. If it is, this section must guide on how to do that. 

In case of using API keys, Renyoo expects the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: meowmeowmeow`

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside>

# Posts

## Get All Posts


```shell
curl "http://example.com/api/Posts"
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves all Posts.

### HTTP Request

`GET http://example.com/api/Posts`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include Posts that have already been adopted.

<aside class="success">
Remember — a happy Post is an authenticated Post!
</aside>

## Get a Specific Post

```shell
curl "http://example.com/api/Posts/2"
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific Post.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://example.com/Posts/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Post to retrieve

## Delete a Specific Post

```shell
curl "http://example.com/api/Posts/2"
  -X DELETE
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint deletes a specific Post.

### HTTP Request

`DELETE http://example.com/Posts/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Post to delete

