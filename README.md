# PHP MVC Tutorial Repo

This repository tracks my progress while following Zura's PHP MVC tutorial series on YouTube. The goal is not to repackage his work as my own. The point of this repo is to keep the project history easier to study, step through, and revisit when working through the series.

A common problem with long-form tutorial content is that you can get stuck halfway through a lesson and the only reference available is the finished codebase. This repo is my way of solving that problem for myself by keeping the work separated into branches that map back to the tutorial progression.

## Credit

All credit for the original teaching, walkthrough, and project structure goes to Zura.

- Playlist: [PHP MVC Framework Tutorial](https://www.youtube.com/playlist?list=PLLQuc_7jk__Uk_QnJMPndbdKECcTEwTA1)
- Please support Zura by liking the videos, subscribing on YouTube, and following his social channels.

If you are using this repository, you should treat Zura's content as the primary source and this repo as a companion reference.

## Why this repo exists

This repository is useful if you want to:

- follow the tutorial at a slower pace
- compare your code against an intermediate checkpoint instead of only the final result
- jump back to a specific lesson without manually undoing later changes
- understand how the project evolves over time

## Branch convention

Each branch is named after the part of the tutorial it corresponds to.

- `part-1` = work from the first video or section
- `part-2` = next checkpoint
- and so on

That naming scheme makes it easier to switch directly to the point where you got stuck.

## Current project state

At the moment, this repository contains a small custom PHP MVC application with:

- a front controller in `public/index.php`
- a lightweight `Application` class
- a simple router with `GET` and `POST` route registration
- request and response handling under `core/`
- controller-based page rendering
- separate layouts for the main site and auth pages
- basic views for home, contact, login, register, and 404 pages

This is a learning project, so the value here is in understanding the structure and progression rather than treating it as a production-ready framework.

## Project structure

```text
.
|-- composer.json
|-- controllers/
|   |-- AuthController.php
|   `-- SiteController.php
|-- core/
|   |-- Application.php
|   |-- Controller.php
|   |-- Request.php
|   |-- Response.php
|   `-- Router.php
|-- public/
|   `-- index.php
|-- runtime/
`-- views/
    |-- layouts/
    |   |-- auth.php
    |   `-- main.php
    |-- _404.php
    |-- contact.php
    |-- home.php
    |-- login.php
    `-- register.php
```

## Available routes

Based on the current `public/index.php`, the app exposes these routes:

- `GET /` - home page
- `GET /contact` - contact page
- `POST /contact` - contact form handler stub
- `GET /login` - login page
- `POST /login` - login form submit target
- `GET /register` - register page

The register flow is clearly still in progress in this snapshot, which is expected for a tutorial-following repository.

## Getting started

### Requirements

- PHP 8.x recommended
- Composer

### Install dependencies

```bash
composer install
```

### Run locally

From the project root:

```bash
php -S localhost:8080 -t public
```

Then open:

```text
http://localhost:8080
```

## Notes for learners

If you are following along with the tutorial yourself, a practical workflow is:

1. Check out the branch that matches the lesson you are on.
2. Compare your files against that checkpoint.
3. Use the next branch only after you understand what changed.

That approach is more useful than jumping straight to the latest state of the repository, especially when the goal is to understand routing, controllers, layouts, and request flow.

## Attribution reminder

This repository exists to support learning. It should not be used to remove credit from the original tutorial author. If this repo helps, support Zura directly through the original playlist and his channels.
