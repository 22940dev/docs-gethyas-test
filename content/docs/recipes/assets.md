---
title: "Assets"
description: "Customize Hyas SCSS or Hyas JS. Add a Lambda function."
lead: "Customize Hyas SCSS or Hyas JS. Add a Lambda function."
date: 2020-09-21T14:41:53+02:00
lastmod: 2020-09-21T14:41:53+02:00
draft: false
images: []
menu:
  docs:
    parent: "recipes"
weight: 170
toc: true
---

```bash
..
├── fonts/
├── images/
├── js/
│   ├── vendor/
│   ├── app.js
│   └── index.js
├── lambda/
└── scss/
    ├── common/
    ├── components/
    ├── layouts/
    ├── vendor/
    └── app.scss
```

See also the Hugo docs: [Hugo Pipes](https://gohugo.io/hugo-pipes/).

## Customize Hyas SCSS

{{< alert icon="👉" text="Set variables in `./assets/scss/common/_variables.scss`." >}}

See also the Bootstrap code: [Variables](https://github.com/twbs/bootstrap/blob/main/scss/_variables.scss).

```bash
./assets/scss/app.scss
```

## Customize Hyas JS

```bash
./assets/js/app.js
```

## Add a Lambda function

See also: [Functions]({{< ref "netlify#functions" >}})

### Example

```bash
./assets/lambda/hi-from-lambda.js
```

```js
exports.handler = (event, context, callback) => {
  callback (null, {
    statusCode: 200,
    headers: {
      'Content-Type': 'application/json',
    },
    body: JSON.stringify({
      message: 'Hi from Lambda.',
    }),
  });
}
```
