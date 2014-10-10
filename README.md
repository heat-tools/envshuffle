## envshuffle
Sets environment variables based on the contents of other environment
variables.

This is sometimes useful when using
[parameterized builds](https://circleci.com/docs/parameterized-builds)
with [CircleCI](https://circleci.com/), as environment variables set in the repo
build configuration cannot be overriden by variables passed into a parameterized
build request.

### Install
`pip install git+https://github.com/JasonBoyles/envshuffle`

### Usage
```shell
~:jgb $ OVERRIDE_FOO=fighters OVERRIDE_HOME=sweethome envshuffle bash -c 'echo FOO is ${FOO}, HOME is ${HOME}'
overriding var HOME
overriding var FOO
fighters sweethome
~:jgb $
```
