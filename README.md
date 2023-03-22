<h2 align="center">
    {ProjectName}
</h2>

<p align="center">
The project is created under {CompanyName} for {ProjectPurpose}.
</p>

Table of Contents
=================

  * [Features / Technologies](#features--technologies)
  * [Codeigniter Packages](#codeigniter-packages)
  * [IDE](#ide)
  * [Requirements](#requirements)
  * [Local Installation](#local-installation)
  * [Git Development Guidelines](#git=development-guidelines)

### Features / Technologies

- [PHP v7.4](https://www.php.net/releases/7.4/en.php)
- [💚 Codeigniter v4](https://codeigniter4.github.io/) - an Application Development Framework - a toolkit - for people who build web sites using PHP.
- [MySQL v8](https://dev.mysql.com/) - the most popular Open Source SQL database management system, is developed, distributed, and supported by Oracle Corporation.
- ⚒️ [Composer](https://getcomposer.org/) - Dependency Manager for PHP

### Codeigniter Packages

- 

### IDE

- [PHPStorm](https://www.jetbrains.com/phpstorm/)
- [VSCode](https://code.visualstudio.com/)

### Requirements

Install the following programs
- [PHP](https://php.net) version 7.4 or newer is required, with the following PHP extensions are enabled:
    - intl
    - mbstring
    - json
    - mysqlnd
- [Composer](https://getcomposer.org)
- [MySQL](https://dev.mysql.com/)

### Local Installation

Clone this repository

```bash
git clone git@github.com:{OrgName}/{ProjectName}.git
```

Enter {ProjectName} directory

```bash
cd {ProjectName}
```

Install all the required packages

```bash
composer install
```

Copy env.example to .env

```bash
cp env.example .env
```

Update .env database attributes as your database Installation

```
database.default.hostname = localhost
database.default.database = ci4
database.default.username = root
database.default.password = root
database.default.DBDriver = MySQLi
database.default.DBPrefix =
database.default.port = 3306

database.tests.hostname = localhost
database.tests.database = ci4_test
database.tests.username = root
database.tests.password = root
database.tests.DBDriver = MySQLi
database.tests.DBPrefix =
database.tests.port = 3306
```

Run {ProjectName} local development server

```bash
php spark serve
```

This will launch the server and you can now view {ProjectName} in your browser at http://localhost:8080.

### Git Development Guides

#### Feature

- Go to `development` branch

```bash
git switch development
```

- Get the latest changes of `development` branch

```bash
git pull origin development
```

- Create a new `feature` branch based on `development` branch with using your task code follow with your task name

```bash
// branch naming example
git switch -c feature/T932-Create-to-dos
```

- Perform and commit your changes

```bash
git add .
git commit -m "{YourCommitMessageHere}"
```

- Get latest `development` changes, move his work on top of the latest

```bash
git switch development
git pull origin development
git switch feature/T932-Create-to-dos
git rebase development
```

- Perform corrections as needed (If any conflicts)

- Create a pull request [here](https://github.com/{OrgName}/{ProjectName}/compare) by selecting `development` as base and `{YourNewBranch}` as compare

- Let the code reviewer review your codes
