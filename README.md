Codecov Swift Example
=====================

| [https://codecov.io][1] | [@codecov][2] | [hello@codecov.io][3] |
| ----------------------- | ------------- | --------------------- |

This repository serves as an **example** on how to use [Codecov Global][4] for Swift.

## Usage
Enable "Gather coverage data" in your test scheme:

![gather coverage data](docs/gather_coverage_data.png)

# Travis CI

Add to your `.travis.yml` file.
```yml
language: swift # or objective-c
osx_image: xcode7
script: ./test.sh
after_success:
  - bash <(curl -s https://codecov.io/bash)
```

## Private Repos
> Set `CODECOV_TOKEN` in your environment variables.

Add to your `.travis.yml` file.
```yml
env:
  global:
    - CODECOV_TOKEN=:uuid-repo-token

after_success:
  - bash <(curl -s https://codecov.io/bash)
```

View source and learn more about [Codecov Global Uploader][4]

[1]: https://codecov.io/
[2]: https://twitter.com/codecov
[3]: mailto:hello@codecov.io
[4]: https://github.com/codecov/codecov-python