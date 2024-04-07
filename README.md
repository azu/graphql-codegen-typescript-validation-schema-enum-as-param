# graphql-codegen-typescript-validation-schema-enum-as-param

Test repository for [graphql-codegen-typescript-validation-schema](https://github.com/Code-Hex/graphql-codegen-typescript-validation-schema/tree/main).

- Issue: [How to handle enum on directive arguments? · Issue #611 · Code-Hex/graphql-codegen-typescript-validation-schema](https://github.com/Code-Hex/graphql-codegen-typescript-validation-schema/issues/611)

Enum on directive argument.

```graphql
directive @validateString(
    format: StringFormat
) on INPUT_FIELD_DEFINITION | ARGUMENT_DEFINITION

enum StringFormat {
    EMAIL
    IP
}

# All validation directives
input Example {
    email: String! @validateString(format: EMAIL)
    ip: String! @validateString(format: IP)
}
```

## Install

    npm ci
    npm run codegen

## Changelog

See [Releases page](https://github.com/azu/graphql-codegen-typescript-validation-schema-enum-as-param/releases).

## Running tests

Install devDependencies and Run `npm test`:

    npm test

## Contributing

Pull requests and stars are always welcome.

For bugs and feature requests, [please create an issue](https://github.com/azu/graphql-codegen-typescript-validation-schema-enum-as-param/issues).

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## Author

- azu: [GitHub](https://github.com/azu), [Twitter](https://twitter.com/azu_re)

## License

MIT © azu
