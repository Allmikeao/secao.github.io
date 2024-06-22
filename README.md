# PROSEC Cacuaco [![license](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](http://www.apache.org/licenses/LICENSE-2.0) [![prosec](https://codecov.io/gh/nasa/openmct/branch/master/graph/badge.svg?token=7DQIipp3ej)](https://codecov.io/gh/nasa/openmct) 

> [!NOTE]
> Por favor visite o nosso [`Site`](http://prosec.free.nf/) ou fale connosco apartir do nosso [`E-mail`](inbox.mikelange@gmail.com)


### Screenshot 2024-06-23 at 17:51:36]
<img src="https://i.ibb.co/6sP17Hb/IMG-20240622-172910.jpg" alt="IMG-20240622-172910" border="0">


## Caso de uso

Para usar o [PROSEC](http://prosec.totalh.net) é muito fácil, rápido e eficaz. É disponibilizado um formulário para que os usuários relatem das ocorrências criminosas ligado aos crimes de `Roubo` e `Furto` de veículos.

Siga os passos abaixo para o caso de uso.:

1. Nome:

```
O usuário deverá preencher o campo com o seu nome completo 
```

2. Telefone :

```
O usuário deverá preencher o campo com o seu número de telefone 
```

3. Email (Opcional): 

```
O usuário deverá preencher o campo com o seu email caso tenha
```

4. Assunto:

```
O usuário deverá preencher o campo, informando o assunto ou títular a sua denúncia 
```
5. Data e hora da ocorrência :

```
O usuário deverá preencher o campo, selecionando a hora e a data da ocorrência 
```

6. Messagem: 

```
O usuário deverá preencher o campo, detalhando tudo que houve
```

> [!IMPORTANT]
> Para que a sua ocorrência seja válida, terá de confirmar a [`reCAPTCHA`](HTTPS://), depois da [`reCAPTCHA`](http://) confirmar de que és um usuário humano, a sua ocorrência será enviada.

Para que não haja erros, preencha os campos com os dados precisos por cada campo.

Open MCT is built using [`npm`](http://npmjs.com/) and [`webpack`](https://webpack.js.org/).

## Documentation

Documentation is available on the [Open MCT website](https://nasa.github.io/openmct/documentation/).

### Examples

The clearest examples for developing Open MCT plugins are in the
[tutorials](https://github.com/nasa/openmct-tutorial) provided in
our documentation.

> [!NOTE]
> We want Open MCT to be as easy to use, install, run, and develop for as
> possible, and your feedback will help us get there! 
> Feedback can be provided via [GitHub issues](https://github.com/nasa/openmct/issues/new/choose), 
> [Starting a GitHub Discussion](https://github.com/nasa/openmct/discussions), 
> or by emailing us at [arc-dl-openmct@mail.nasa.gov](mailto:arc-dl-openmct@mail.nasa.gov).

## Developing Applications With Open MCT

For more on developing with Open MCT, see our documentation for a guide on [Developing Applications with Open MCT](./API.md#starting-an-open-mct-application).

## Compatibility

This is a fast moving project and we do our best to test and support the widest possible range of browsers, operating systems, and nodejs APIs. We have a published list of support available in our package.json's `browserslist` key.

The project uses `nvm` to ensure the node and npm version used, is coherent in all projects. Install nvm (non-windows), [here](https://github.com/nvm-sh/nvm) or the windows equivalent [here](https://github.com/coreybutler/nvm-windows)

If you encounter an issue with a particular browser, OS, or nodejs API, please file a [GitHub issue](https://github.com/nasa/openmct/issues/new/choose)

## Plugins

Open MCT can be extended via plugins that make calls to the Open MCT API. A plugin is a group 
of software components (including source code and resources such as images and HTML templates)
that is intended to be added or removed as a single unit.

As well as providing an extension mechanism, most of the core Open MCT codebase is also 
written as plugins.

For information on writing plugins, please see [our API documentation](./API.md#plugins).

## Tests

Our automated test coverage comes in the form of unit, e2e, visual, performance, and security tests. 

### Unit Tests
Unit Tests are written for [Jasmine](https://jasmine.github.io/api/edge/global)
and run by [Karma](http://karma-runner.github.io). To run:

`npm test`

The test suite is configured to load any scripts ending with `Spec.js` found
in the `src` hierarchy. Full configuration details are found in
`karma.conf.js`. By convention, unit test scripts should be located
alongside the units that they test; for example, `src/foo/Bar.js` would be
tested by `src/foo/BarSpec.js`.

### e2e, Visual, and Performance tests
The e2e, Visual, and Performance tests are written for playwright and run by playwright's new test runner [@playwright/test](https://playwright.dev/). 

To run the e2e tests which are part of every commit:

`npm run test:e2e:stable`

To run the visual test suite:

`npm run test:e2e:visual`

To run the performance tests:

`npm run test:perf`

The test suite is configured to all tests located in `e2e/tests/` ending in `*.e2e.spec.js`. For more about the e2e test suite, please see the [README](./e2e/README.md)

### Security Tests
Each commit is analyzed for known security vulnerabilities using [CodeQL](https://codeql.github.com/docs/codeql-language-guides/codeql-library-for-javascript/). The list of CWE coverage items is available in the [CodeQL docs](https://codeql.github.com/codeql-query-help/javascript-cwe/). The CodeQL workflow is specified in the [CodeQL analysis file](./.github/workflows/codeql-analysis.yml) and the custom [CodeQL config](./.github/codeql/codeql-config.yml).

### Test Reporting and Code Coverage

Each test suite generates a report in CircleCI. For a complete overview of testing functionality, please see our [Circle CI Test Insights Dashboard](https://app.circleci.com/insights/github/nasa/openmct/workflows/the-nightly/overview?branch=master&reporting-window=last-30-days)

Our code coverage is generated during the runtime of our unit, e2e, and visual tests. The combination of those reports is published to [codecov.io](https://app.codecov.io/gh/nasa/openmct/)

For more on the specifics of our code coverage setup, [see](TESTING.md#code-coverage)

# Glossary

Certain terms are used throughout Open MCT with consistent meanings
or conventions. Any deviations from the below are issues and should be
addressed (either by updating this glossary or changing code to reflect
correct usage.) Other developer documentation, particularly in-line
documentation, may presume an understanding of these terms.

* _plugin_: A plugin is a removable, reusable grouping of software elements.
  The application is composed of plugins.
* _composition_: In the context of a domain object, this refers to the set of
  other domain objects that compose or are contained by that object. A domain
  object's composition is the set of domain objects that should appear
  immediately beneath it in a tree hierarchy. A domain object's composition is
  described in its model as an array of id's; its composition capability
  provides a means to retrieve the actual domain object instances associated
  with these identifiers asynchronously.
* _description_: When used as an object property, this refers to the human-readable
  description of a thing; usually a single sentence or short paragraph.
  (Most often used in the context of extensions, domain
  object models, or other similar application-specific objects.)
* _domain object_: A meaningful object to the user; a distinct thing in
  the work support by Open MCT. Anything that appears in the left-hand
  tree is a domain object.
* _identifier_: A tuple consisting of a namespace and a key, which together uniquely
  identifies a domain object.
* _model_: The persistent state associated with a domain object. A domain
  object's model is a JavaScript object which can be converted to JSON
  without losing information (that is, it contains no methods.)
* _name_: When used as an object property, this refers to the human-readable
  name for a thing. (Most often used in the context of extensions, domain
  object models, or other similar application-specific objects.)
* _navigation_: Refers to the current state of the application with respect
  to the user's expressed interest in a specific domain object; e.g. when
  a user clicks on a domain object in the tree, they are _navigating_ to
  it, and it is thereafter considered the _navigated_ object (until the
  user makes another such choice.)
* _namespace_: A name used to identify a persistence store. A running open MCT 
application could potentially use multiple persistence stores, with the 

## Open MCT v2.0.0
Support for our legacy bundle-based API, and the libraries that it was built on (like Angular 1.x), have now been removed entirely from this repository.

For now if you have an Open MCT application that makes use of the legacy API, [a plugin](https://github.com/nasa/openmct-legacy-plugin) is provided that bootstraps the legacy bundling mechanism and API. This plugin will not be maintained over the long term however, and the legacy support plugin will not be tested for compatibility with future versions of Open MCT. It is provided for convenience only.

### How do I know if I am using legacy API?
You might still be using legacy API if your source code

* Contains files named bundle.js, or bundle.json,
* Makes calls to `openmct.$injector()`, or `openmct.$angular`,
* Makes calls to `openmct.legacyRegistry`, `openmct.legacyExtension`, or `openmct.legacyBundle`.


### What should I do if I am using legacy API?
Please refer to [the modern Open MCT API](https://nasa.github.io/openmct/documentation/). Post any questions to the [Discussions section](https://github.com/nasa/openmct/discussions) of the Open MCT GitHub repository.

## Related Repos

> [!NOTE]
> Although Open MCT functions as a standalone project, it is primarily an extensible framework intended to be used as a dependency with users' own plugins and packaging. Furthermore, Open MCT is intended to be used with an HTTP server such as Apache or Nginx. A great example of hosting Open MCT with Apache is `openmct-quickstart` and can be found in the table below.

| Repository | Description |
| --- | --- |
| [openmct-tutorial](https://github.com/nasa/openmct-tutorial) | A great place for beginners to learn how to use and extend Open MCT. |
| [openmct-quickstart](https://github.com/scottbell/openmct-quickstart) | A working example of Open MCT integrated with Apache HTTP server, YAMCS telemetry, and Couch DB for persistence.
| [Open MCT YAMCS Plugin](https://github.com/akhenry/openmct-yamcs) | Plugin for integrating YAMCS telemetry and command server with Open MCT. |
| [openmct-performance](https://github.com/unlikelyzero/openmct-performance) | Resources for performance testing Open MCT. |
| [openmct-as-a-dependency](https://github.com/unlikelyzero/openmct-as-a-dependency) | An advanced guide for users on how to build, develop, and test Open MCT when it's used as a dependency. |
# Autores

<div style='display: inline; align-items: center;'> 

<img src="https://i.ibb.co/SRmLGXf/1718726549566.jpg" alt="1718726549566" width="100" height="100" border="0"> Edson Simão <br>
<img src="https://i.ibb.co/ctQT3ZY/1718726610256.jpg" alt="1718726610256" width="100" height="100" border="0">  Daniel Miguel <br>
<img src="https://i.ibb.co/px3pVpq/Pics-Art-06-29-01-00-04.jpg" alt="Mike" width="100" height="100" border="0"> Mike L'ange
</div>

![GitHub Org's stars](https://img.shields.io/github/stars/camilafernanda?style=social)
Resultado