# eslint-plugin-stedi-aws-rules

Best practices around using AWS SDK in Javascript & Typescript projects.

[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release)

References:

- https://pages.awscloud.com/rs/112-TZM-766/images/2020_0316-SRV_Slide-Deck.pdf

## Installation

You'll first need to install [ESLint](http://eslint.org):

```
$ npm i eslint --save-dev
```

Next, install `@stedi-oss/eslint-plugin-stedi-aws-rules`:

```
npm install @stedi-oss/eslint-plugin-stedi-aws-rules --save-dev
```

## Usage

Add `stedi` to the plugins section of your `.eslintrc` configuration file. You can omit the `eslint-plugin-` prefix:

```json
{
  "plugins": ["@stedi-oss/stedi-aws-rules"]
}
```

Then configure the rules you want to use under the rules section.

```json
{
  "rules": {
    "@stedi-oss/stedi-aws-rules/no-aws-import": "error",
    "@stedi-oss/stedi-aws-rules/instrument-aws-clients": "error",
    "@stedi-oss/stedi-aws-rules/instrument-document-clients": "error"
  }
}
```

## Supported Rules

- [@stedi-oss/stedi-aws-rules/no-aws-import](docs/rules/no-aws-import.md)
- [@stedi-oss/stedi-aws-rules/instrument-aws-clients](docs/rules/instrument-aws-clients.md)
- [@stedi-oss/stedi-aws-rules/instrument-document-clients](docs/rules/instrument-document-clients.md)
- [@stedi-oss/stedi-aws-rules/no-direct-lambda-invoke.md](docs/rules/no-direct-lambda-invoke.md)

## Contributing

As Stedi uses this for own projects, we know this might not be the perfect approach for all the projects out there. If you have any ideas, just open an issue and tell us you think.

If you'd like to contribute, please fork the repository and make changes as you'd like. Pull requests are warmly welcome.

### Adding a new rule

To follow our structure, when bootstraping new rule please use [generator-eslint](https://github.com/eslint/generator-eslint) to do so.

Make sure you're in the top-level directory of this repo and type:

```sh
$ yo eslint:rule
```

## Releases

New releases are generated with each commit to the master using [semantic-release](https://github.com/semantic-release/semantic-release)

## License

[MIT License](https://opensource.org/licenses/MIT) © [Stedi](https://stedi.com)
