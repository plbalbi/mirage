[![](https://img.shields.io/badge/License-Apache%202.0-green.svg)](https://github.com/appbaseio/mirage/blob/dev/LICENSE.md) [![](https://img.shields.io/badge/angular-2.0.0--rc.4-blue.svg)](https://github.com/appbaseio/mirage/blob/dev/package.json#L20) <a href="https://codeclimate.com/github/appbaseio/mirage"><img src="https://codeclimate.com/github/appbaseio/mirage/badges/gpa.svg" /></a>


![](http://i.imgur.com/RoyFbSb.png?1)

## Mirage: The missing query explorer for Elasticsearch

1. **[Mirage: Intro](#1-mirage-intro)**   
2. **[Features](#2-features)**  
3. **[Roadmap](#3-roadmap)** 
4. **[Build Locally](#4-build-locally)**  
5. **[How to contribute](#5-how-to-contribute)** 
6. **[Get Mirage](#6-get-mirage)**


<br>

### 1. Mirage: Intro

The Elasticsearch query DSL supports 100+ query APIs ranging from full-text search, numeric range filters, geolocation queries to nested and span queries. 

Mirage is a modern, open-source web based query explorer for Elasticsearch. 

[![2-min Intro to Mirage](https://i.imgur.com/mBMBdfU.png)](https://vimeo.com/185000306)

It offers a blocks based GUI for composing Elasticsearch queries and comes with an on-the-fly transformer to show the corresponding JSON query API of Elasticsearch.

<br>

### 2. Features

* Mirage's GUI building blocks offer a smart way to creating queries. It uses the index's Elasticsearch mappings and the selected field's datatype to show only the applicable queries in the dropdown.

![Watch Queries being built in realtime](http://i.imgur.com/9ActpEK.gif)  

<br>

* Mirage provides two ways to add compound query clauses, 
  * `Add Conditions` allows adding additional clauses within the same query and  
  * `Nested Query` allows adding a nested query clause. 

![Intuitively layer complexity to your queries](http://i.imgur.com/uFpBv4e.gif)  

<br>

* Queries can be saved for later reuse. They can also be captured and shared by copying the URL.

![Save queries for later reuse](http://i.imgur.com/NMAi5tn.gif)

* See docs for any query from within the app.

![Browse docs from within Mirage](http://i.imgur.com/9bDf6ax.gif)

<br>

### 3. Roadmap

Mirage works with an Elasticsearch 2.x index currently. Below is the roadmap for query support.

✓ indicates queries already supported.  
➕ indicates queries we would like to support and see [contributions for](#5-how-to-contribute).  
❌ indicates queries that can't be supported currently.

| Full-text Queries      | Term Level Queries  | Joining Queries | Geo Queries          | Specialized Queries | Span Queries |
| :--------------------: |:-------------------:| :--------------:| :-------------------:|:-------------------:|:------------:|
| 	✓ Match               | 	✓ Term             | ➕ Nested       | ➕ GeoShape          | ➕ MoreLikeThis     | ➕ SpanTerm   |
| 	✓ Multi-match         | 	✓ Terms            | ➕ HasChild     | ➕ GeoBoundingBox    | ➕ Template         | ➕ SpanMulti  |
| 	✓ Query String        | 	✓ Range            | ➕ HasParent    | ➕ GeoDistance       | ❌ Script           | ➕ SpanFirst  |
| 	✓ Simple Query String | 	✓ Exists           |                 | ➕ GeoDistanceRange  |                     | ➕ SpanNear   |
| 	✓ Common Terms        | 	✓ Missing          |                 | ➕ GeoPolygon        |                     | ➕ SpanOr     |
|                        | 	✓ Prefix           |                 | ➕ GeoHashCell       |                     | ➕ SpanNot    |
|                        | 	✓ Wildcard         |                 |                      |                     | ➕ SpanContaining   |
|                        | 	✓ Regexp           |                 |                      |                     | ➕ SpanWithin   |
|                        | 	✓ Fuzzy            |                 |                      |                     |
|                        | 	✓ Ids              |                 |                      |                     |
|                        | ❌ Type             |                 |                      |                     |

Besides broadening the query support, we would like to see Mirage support Elasticsearch v5.0.

<br>

### 4. Build Locally

```sh
$ npm install 
$ bower install
$ npm start
```

This will start a local webserver running on port 3000 serving mirage locally.

#### Tests

```sh
$ npm test
```

will fire up the jasmine tests. 

#### `master` branch: Elasticsearch Plugin

```sh
$ npm run build_es_plugin
```

#### `chrome-extension` branch: Chrome extension

```sh
$ npm run build_chrome_extension
```

<br>

### 5. How to Contribute  

1. Find a query that can be supported from the [roadmap](#3-roadmap).  
2. Fork the mirage repo and update in "dev" branch.
3. [Create the query files](https://github.com/appbaseio/mirage/blob/dev/HOW-TO-CONTRIBUTE.md).  
4. Build locally and run `npm test`.
5. Submit a PR!

<br>

### 6. Get Mirage

Mirage is available as a hosted app and as a chrome extension.

#### Use [appbaseio.github.io/mirage](http://appbaseio.github.io/mirage) website  

or  

#### [Get the Chrome Extension.](https://chrome.google.com/webstore/detail/mirage/dcnlpfmnpoggchflmdnkgiepijgljoka)

---

Proudly built with ![](https://avatars0.githubusercontent.com/u/139426?v=3&s=20)
