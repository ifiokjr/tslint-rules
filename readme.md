# @kj/tslint-rules

This is a pretty strict tslint configuration for your project.

It comes with a base configuration and a react specific configuration.

## Installation

```bash
yarn add prettier tslint typescript # Required peer dependencies
yarn add @kj/tslint-rules
```

In your tslint.json file add something like the following.

```json
{
  "extends": ["@kj/tslint-rules/react"],
  "rules": {
    "no-implicit-dependencies": [
      true,
      "dev",
      [
        "jest-axe",
        "jest",
        "jest-dom",
        "react-testing-library",
        "@test-utils",
        "@storybook",
        "jest-extended",
        "prosemirror-test-builder"
      ]
    ],
    "no-empty": false,
    "no-any": false,
    "no-object-literal-type-assertion": false,
    "no-console": false,
    "max-classes-per-file": false
  }
}
```

The important line contains `"extends": ["@kj/tslint-rules/react"]`.

If you don't need to support react then you can use `"extends": ["@kj/tslint-rules/base"]` instead.
