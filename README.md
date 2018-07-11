# stylelint-config-ultimate

> The ultimate shareable config for stylelint.

Extends [`stylelint-config-standard`](https://github.com/stylelint/stylelint-config-standard).

Turns on additional rules to enforce the common stylistic conventions found within a handful of CSS styleguides, including: [The Idiomatic CSS Principles](https://github.com/necolas/idiomatic-css),
[Google's CSS Style Guide](https://google.github.io/styleguide/htmlcssguide.html#CSS_Formatting_Rules), [Airbnb's Styleguide](https://github.com/airbnb/css#css), and [@mdo's Code Guide](http://codeguide.co/#css).

It favours flexibility over strictness for things like multi-line lists and single-line rulesets, and tries to avoid potentially divisive rules.

Use it as is or as a foundation for your own config.

To see the rules that this config uses, please read the [config itself](./index.js).

## Installation

```bash
npm install stylelint-config-ultimate --save-dev
```

## Usage

If you've installed `stylelint-config-ultimate` locally within your project, just set your `stylelint` config to:

```json
{
  "extends": "stylelint-config-ultimate"
}
```

If you've globally installed `stylelint-config-ultimate` using the `-g` flag, then you'll need to use the absolute path to `stylelint-config-ultimate` in your config e.g.

```json
{
  "extends": "/absolute/path/to/stylelint-config-ultimate"
}

#### Suggested additions

`stylelint-config-ultimate` is a great foundation for your own config. You can extend it to create a tailored and much stricter config:

-   Specify what quotes must be used using:
    -   [`font-family-name-quotes`](https://github.com/stylelint/stylelint/blob/master/lib/rules/font-family-name-quotes/README.md)
    -   [`function-url-quotes`](https://github.com/stylelint/stylelint/blob/master/lib/rules/function-url-quotes/README.md)
    -   [`selector-attribute-quotes`](https://github.com/stylelint/stylelint/blob/master/lib/rules/selector-attribute-quotes/README.md)
    -   [`string-quotes`](https://github.com/stylelint/stylelint/blob/master/lib/rules/string-quotes/README.md)
-   If you use [`autoprefixer`](https://github.com/postcss/autoprefixer) you'll want to disallow vendor prefixes using:
    -   [`at-rule-no-vendor-prefix`](https://github.com/stylelint/stylelint/blob/master/lib/rules/at-rule-no-vendor-prefix/README.md)
    -   [`media-feature-name-no-vendor-prefix`](https://github.com/stylelint/stylelint/blob/master/lib/rules/media-feature-name-no-vendor-prefix/README.md)
    -   [`property-no-vendor-prefix`](https://github.com/stylelint/stylelint/blob/master/lib/rules/property-no-vendor-prefix/README.md)
    -   [`selector-no-vendor-prefix`](https://github.com/stylelint/stylelint/blob/master/lib/rules/selector-no-vendor-prefix/README.md)
    -   [`value-no-vendor-prefix`](https://github.com/stylelint/stylelint/blob/master/lib/rules/value-no-vendor-prefix/README.md)
-   Control specificity using:
    -   [`max-nesting-depth`](https://github.com/stylelint/stylelint/blob/master/lib/rules/max-nesting-depth/README.md)
    -   [`selector-max-compound-selectors`](https://github.com/stylelint/stylelint/blob/master/lib/rules/selector-max-compound-selectors/README.md)
    -   [`selector-max-specificity`](https://github.com/stylelint/stylelint/blob/master/lib/rules/selector-max-specificity/README.md)
-   Specify acceptable selector types, units, properties, functions and words in comments using:
    -   [`at-rule-blacklist`](https://github.com/stylelint/stylelint/blob/master/lib/rules/at-rule-blacklist/README.md)
    -   [`at-rule-whitelist`](https://github.com/stylelint/stylelint/blob/master/lib/rules/at-rule-whitelist/README.md)
    -   [`color-named`](https://github.com/stylelint/stylelint/blob/master/lib/rules/color-named/README.md)
    -   [`color-no-hex`](https://github.com/stylelint/stylelint/blob/master/lib/rules/color-no-hex/README.md)
    -   [`comment-word-blacklist`](https://github.com/stylelint/stylelint/blob/master/lib/rules/comment-word-blacklist/README.md)
    -   [`declaration-no-important`](https://github.com/stylelint/stylelint/blob/master/lib/rules/declaration-no-important/README.md)
    -   [`declaration-property-unit-blacklist`](https://github.com/stylelint/stylelint/blob/master/lib/rules/declaration-property-unit-blacklist/README.md)
    -   [`declaration-property-unit-whitelist`](https://github.com/stylelint/stylelint/blob/master/lib/rules/declaration-property-unit-whitelist/README.md)
    -   [`declaration-property-value-blacklist`](https://github.com/stylelint/stylelint/blob/master/lib/rules/declaration-property-value-blacklist/README.md)
    -   [`declaration-property-value-whitelist`](https://github.com/stylelint/stylelint/blob/master/lib/rules/declaration-property-value-whitelist/README.md)
    -   [`function-blacklist`](https://github.com/stylelint/stylelint/blob/master/lib/rules/function-blacklist/README.md)
    -   [`function-url-scheme-blacklist`](https://github.com/stylelint/stylelint/blob/master/lib/rules/function-url-scheme-blacklist/README.md)
    -   [`function-url-scheme-whitelist`](https://github.com/stylelint/stylelint/blob/master/lib/rules/function-url-scheme-whitelist/README.md)
    -   [`function-whitelist`](https://github.com/stylelint/stylelint/blob/master/lib/rules/function-whitelist/README.md)
    -   [`media-feature-name-blacklist`](https://github.com/stylelint/stylelint/blob/master/lib/rules/media-feature-name-blacklist/README.md)
    -   [`media-feature-name-whitelist`](https://github.com/stylelint/stylelint/blob/master/lib/rules/media-feature-name-whitelist/README.md)
    -   [`property-blacklist`](https://github.com/stylelint/stylelint/blob/master/lib/rules/property-blacklist/README.md)
    -   [`property-whitelist`](https://github.com/stylelint/stylelint/blob/master/lib/rules/property-whitelist/README.md)
    -   [`selector-attribute-operator-blacklist`](https://github.com/stylelint/stylelint/blob/master/lib/rules/selector-attribute-operator-blacklist/README.md)
    -   [`selector-attribute-operator-whitelist`](https://github.com/stylelint/stylelint/blob/master/lib/rules/selector-attribute-operator-whitelist/README.md)
    -   [`selector-combinator-blacklist`](https://github.com/stylelint/stylelint/blob/master/lib/rules/selector-combinator-blacklist/README.md)
    -   [`selector-combinator-whitelist`](https://github.com/stylelint/stylelint/blob/master/lib/rules/selector-combinator-whitelist/README.md)
    -   [`selector-max-class`](https://github.com/stylelint/stylelint/blob/master/lib/rules/selector-max-class/README.md)
    -   [`selector-max-attribute`](https://github.com/stylelint/stylelint/blob/master/lib/rules/selector-max-attribute/README.md)
    -   [`selector-max-combinators`](https://github.com/stylelint/stylelint/blob/master/lib/rules/selector-max-combinators/README.md)
    -   [`selector-max-id`](https://github.com/stylelint/stylelint/blob/master/lib/rules/selector-max-id/README.md)
    -   [`selector-max-pseudo-class`](https://github.com/stylelint/stylelint/blob/master/lib/rules/selector-max-pseudo-class/README.md)
    -   [`selector-no-qualifying-type`](https://github.com/stylelint/stylelint/blob/master/lib/rules/selector-no-qualifying-type/README.md)
    -   [`selector-max-type`](https://github.com/stylelint/stylelint/blob/master/lib/rules/selector-max-type/README.md)
    -   [`selector-max-universal`](https://github.com/stylelint/stylelint/blob/master/lib/rules/selector-max-universal/README.md)
    -   [`selector-pseudo-class-blacklist`](https://github.com/stylelint/stylelint/blob/master/lib/rules/selector-pseudo-class-blacklist/README.md)
    -   [`selector-pseudo-class-whitelist`](https://github.com/stylelint/stylelint/blob/master/lib/rules/selector-pseudo-class-whitelist/README.md)
    -   [`selector-pseudo-element-blacklist`](https://github.com/stylelint/stylelint/blob/master/lib/rules/selector-pseudo-element-blacklist/README.md)
    -   [`selector-pseudo-element-whitelist`](https://github.com/stylelint/stylelint/blob/master/lib/rules/selector-pseudo-element-whitelist/README.md)
    -   [`unit-blacklist`](https://github.com/stylelint/stylelint/blob/master/lib/rules/unit-blacklist/README.md)
    -   [`unit-whitelist`](https://github.com/stylelint/stylelint/blob/master/lib/rules/unit-whitelist/README.md)
-   Specify acceptable naming patterns using:
    -   [`custom-media-pattern`](https://github.com/stylelint/stylelint/blob/master/lib/rules/custom-media-pattern/README.md)
    -   [`custom-property-pattern`](https://github.com/stylelint/stylelint/blob/master/lib/rules/custom-property-pattern/README.md)
    -   [`selector-class-pattern`](https://github.com/stylelint/stylelint/blob/master/lib/rules/selector-class-pattern/README.md)
    -   [`selector-id-pattern`](https://github.com/stylelint/stylelint/blob/master/lib/rules/selector-id-pattern/README.md)
    -   [`selector-nested-pattern`](https://github.com/stylelint/stylelint/blob/master/lib/rules/selector-nested-pattern/README.md)
-   Specify a notation when there are one or more valid representations using:
    -   [`font-weight-notation`](https://github.com/stylelint/stylelint/blob/master/lib/rules/font-weight-notation/README.md)
-   Specify what types of URLs are allowed using:
    -   [`function-url-no-scheme-relative`](https://github.com/stylelint/stylelint/blob/master/lib/rules/function-url-no-scheme-relative/README.md)
-   Specify a maximum line length using:
    -   [`max-line-length`](https://github.com/stylelint/stylelint/blob/master/lib/rules/max-line-length/README.md)

## [Changelog](CHANGELOG.md)

## [License](LICENSE)
