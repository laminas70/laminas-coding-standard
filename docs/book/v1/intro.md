# Introduction

## Installation

1. Install the module via Composer by running:

   ```bash
   $ composer require --dev laminas70/laminas-coding-standard
   ```

2. Add Composer scripts into your `composer.json`:

   ```json
   "scripts": {
     "cs-check": "phpcs",
     "cs-fix": "phpcbf"
   }
   ```

3. Create file `phpcs.xml` on base path of your repository with content:

   ```xml
   <?xml version="1.0"?>
   <ruleset name="Laminas Coding Standard">
       <rule ref="./vendor/laminas70/laminas-coding-standard/ruleset.xml"/>

       <!-- Paths to check -->
       <file>config</file>
       <file>src</file>
       <file>test</file>
   </ruleset>
   ```

You can add or exclude some locations in that file.
For a reference please see: https://github.com/squizlabs/PHP_CodeSniffer/wiki/Annotated-Ruleset

## Usage

* To run checks only:

  ```bash
  $ composer cs-check
  ```

* To automatically fix many CS issues:

  ```bash
  $ composer cs-fix
  ```
