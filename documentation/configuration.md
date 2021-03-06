# Lysis configuration

## The configuration file

Lysis configuration is `lysis.yml`, in your project folder.

It follows this scheme:

```
apis:
  <api url 1>:
    <api level parameters>
    generators:
      <generator 1>:
        <generator level parameters>
      <generator 2>:
        <...>
  <api url 1>:
    <...>
```

It means that:

- it is possible to work with many APIs in the same project
- it is possible to work with many generators in the same API

## Parameters

### API level parameters

For now, two parameters are available for each API:

- `basePath`: the base directory where other generators write files. Default value: ``.
- `hydraPrefix`: the hydra prefix. Default value: `hydra:`.

### Generator level parameters

Generator level parameters are specific to the generator.

Take a look to the generator documentation for further details.

## Example

```
apis:
  http://localhost:8000:
    basePath: 'src/app/backend'
    hydraPrefix: 'hydra:'
    generators:
      lysis-typescript-classes-generator:
        dir: 'classes'
      lysis-restangular-services-generator:
        dir: 'services'

```
