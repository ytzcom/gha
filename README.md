# Reusable Github Workflows

This repository contains workflows to run in your projects.

The available workflows are:

* Linters
  * TLint
  * PHPCS
  * PHPStan

* Testing
  * Laravel Artisan Test

* Deployment
  * Laravel Vapor

You can use these workflows by including a Job in your Workflow like so:

```
jobs:
  linters-tlint:
    name: Linters
    uses: lostlink/gha/.github/workflows/tlint.yml@main
  linters-phpcs:
    name: Linters
    uses: lostlink/gha/.github/workflows/phpcs.yml@main
  linters-phpstan:
    name: Linters
    uses: lostlink/gha/.github/workflows/phpstan.yml@main
    secrets:
      VAPOR_API_TOKEN: ${{ secrets.VAPOR_API_TOKEN }}
  test:
    name: Test
    uses: lostlink/gha/.github/workflows/test.yml@main
```

Updates will follow semantic versioning
