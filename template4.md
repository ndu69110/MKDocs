---
date:
  created: 2022-01-31
  updated: 2023-02-01
categories:
  - Search
  - Performance
  - Holidays
tags:
  - MKDocs
  - new year
  - hogmanay
  - festive season
draft: false
links:
  - index.md
#readtime: 15
authors:
  - team

---

# Servas

[](https://github.com/beromir/Servas/tree/main#servas)

A self-hosted bookmark management tool.  
Servas is based on Laravel and Inertia.js and uses Tailwind CSS and Svelte for the frontend.

[![](https://github.com/beromir/Servas/raw/main/docs/images/home.jpg "Home view")](https://github.com/beromir/Servas/blob/main/docs/images/home.jpg)

## Features

[](https://github.com/beromir/Servas/tree/main#features)

-   **Tags:**  Organize your bookmarks with tags.
-   **Groups:**  Group your bookmarks. Groups can be nested.
-   **Smart Groups:**  Group your bookmarks based on their belonging tags.
-   **Firefox and Chrome browser extension:**  Add sites to Servas right from your browser.
-   **Multiple users:**  You can create multiple user accounts.
-   **Responsive design:**  Servas looks good on all your devices.
-   **Import/Export:**  Support for JSON and HTML bookmarks.
-   **Dark/light theme.**
-   **Two Factor Authentication available.**

## How to install

[](https://github.com/beromir/Servas/tree/main#how-to-install)

### Docker

[](https://github.com/beromir/Servas/tree/main#docker)

Servas is available as an  [official Docker image](https://hub.docker.com/r/beromir/servas).

The preferred way to use Servas is with  **SQLite**. This variant does not need an additional database container.  
You can find the example files here:

-   [compose.yaml](https://github.com/beromir/Servas/blob/main/docker/compose.prod.yaml)
-   [.env](https://github.com/beromir/Servas/blob/main/docker/.env.prod.example)

The Docker image also supports  **MySQL**  and  **MariaDB**.  
You can find the example files here:

-   [compose.yaml](https://github.com/beromir/Servas/blob/main/docker/mariadb-example/compose.prod.yaml)
-   [.env](https://github.com/beromir/Servas/blob/main/docker/mariadb-example/.env.prod.example)

```javascript
//comment
var i=toto
```
> testr
> > ddd
>
>  create the `.ev` file

**Initial steps:**

1.  Create  `.env`  file in the directory where the  `compose.yaml`  is located.
2.  Copy the content of the example env file into the  `.env`  file.
3.  Change the  `APP_URL`.
4.  Use a strong password for the  `DB_PASSWORD`  setting (only required if Servas is used with MariaDB).
5.  Start the containers with  `docker compose up -d`.
6.  Generate the application key:

docker exec -it servas php artisan key:generate --force

7.  Restart the containers with  `docker compose restart`.
8.  Open your browser and create a user account at  [https://your-servas-instance/register](https://your-servas-instance/register).

### Manual

[](https://github.com/beromir/Servas/tree/main#manual)

**Requirements:**

-   PHP 8.3
-   MariaDB, MySQL or SQLite
-   Git
-   Node.js
-   Composer

1.  Clone the repo.
2.  Install the Composer packages.

composer install --optimize-autoloader --no-dev

3.  Install the npm packages.

npm install

4.  Compile the assets.

npm run build

5.  Create  `.env`  file from the  `.env.example`  file.
6.  Change the settings in the  `.env`  file according to your needs.
7.  If you are using SQLite, you must remove the MySQL section in the  `.env`  file and uncomment the SQLite section.
8.  Run the database migrations.

php artisan migrate

9.  Generate the application key.

php artisan key:generate

## Configuration

[](https://github.com/beromir/Servas/tree/main#configuration)

You can change some application settings in the  `.env`  file.

Description

`.env`  key

Options

Enable/Disable user registration

`SERVAS_ENABLE_REGISTRATION`

`true`/`false`

Show/Hide version number in profile dropdown

`SERVAS_SHOW_APP_VERSION`

`true`/`false`

After making changes to the  `.env`  file, you must restart the application container.

## User Guide

[](https://github.com/beromir/Servas/tree/main#user-guide)

Register a new user at  [https://your-servas-instance/register](https://your-servas-instance/register).

## Browser Extensions

[](https://github.com/beromir/Servas/tree/main#browser-extensions)

**Firefox and Chrome:**  [https://github.com/beromir/servas-extension](https://github.com/beromir/servas-extension)

## Screenshots

[](https://github.com/beromir/Servas/tree/main#screenshots)

Visit the  [website](https://servas.app/#screenshots).