<!--

INSTRUCTIONS:

For each PR, add a changelog entry that describes what your PR does. Add it to the heading
for the appropriate package it modifies and include it in this format:
- [Description] ([Link to PR])

If your PR affects multiple packages, list it multiple times under headings for each package.
If it affects more general things such as dependency updates or non-package-specific changes,
add it under a "Dev / docs / playground" section.

You should also update the heading of the latest (upcoming) version if your PR change merits
it according to semantic versioning. For example, if your PR adds a breaking change, then you
should change the heading of the (upcoming) version to include a major version bump.

-->

# 6.0.0-beta.12

## @rjsf/core

- Updated `Form` to store the `schemaUtils.getRootSchema()` into the `state.schema` and use that everywhere as the `schema`

## @rjsf/shadcn

- Updated the building of `shadcn` to use the `lodashReplacer` with `tsc-alias` fixing [#4678](https://github.com/rjsf-team/react-jsonschema-form/issues/4678)

## @rjsf/utils

- Updated `SchemaUtils` and `createSchemaUtils()` to add a new `getRootSchema()` function

# 6.0.0-beta.11

## @rjsf/antd

- Set peerDependency for `@ant-design/icons` to `^6.0.0`, fixing [#4643](https://github.com/rjsf-team/react-jsonschema-form/issues/4643)
- Added `MultiSchemaFieldTemplate`

## @rjsf/chakra-ui

- Added `MultiSchemaFieldTemplate`
- Improve visual styling of error validation boxes
- Update `chakra-ui/react` package to `^3.19.1`

## @rjsf/core

- Refactored `MultiSchemaField` to use the `MultiSchemaFieldTemplate` provided by the registry.
- Added `MultiSchemaFieldTemplate` component to maintain the same functionality as the previous `MultiSchemaField` implementation.

## @rjsf/daisyui

- Added `MultiSchemaFieldTemplate`

## @rjsf/fluentui-rc

- Added `MultiSchemaFieldTemplate`

## @rjsf/mui

- Added `MultiSchemaFieldTemplate`

## @rjsf/primereact

- New theme!

## @rjsf/react-bootstrap

- Added `MultiSchemaFieldTemplate`

## @rjsf/semantic-ui

- Added `MultiSchemaFieldTemplate`

## @rjsf/shadcn

- Added `MultiSchemaFieldTemplate`

## @rjsf/utils

- Fixed issue where oneOf radio button could not be modified when defaults were set, fixing [#4634](https://github.com/rjsf-team/react-jsonschema-form/issues/4634)
- Fix default value for object properties such as enums that are rendered in select, radio inputs, etc.
- Add support for `MultiSchemaFieldTemplate`, with new `MultiSchemaFieldTemplateProps`, to the `TemplatesType` interface

## Dev / docs / playground

- Added documentation for the new `MultiSchemaFieldTemplate`

# 6.0.0-beta.10

## @rjsf/mui

- Fixed build process to remove the `tsc-alias` replacer that was adding `/index.js` onto the `@mui/Xxxx` imports since MUI 7 has proper ESM support 

# 6.0.0-beta.9

## @rjsf/antd

- Updated the `README.md` file for dependencies and snapshots due to updating to latest `antd`

## @rjsf/chakra-ui

- Updated `SelectWidget` to only pick the first element in a list when single selection is active, fixing [#4623](https://github.com/rjsf-team/react-jsonschema-form/issues/4623)
- Updated the `README.md` file for dependencies

## @rjsf/daisyui

- Updated the `README.md` file for dependencies
- Updated `package.json` to move `@fluentui` packages to peer and dev dependencies

## @rjsf/fluentui-rc

- Updated the `README.md` file for dependencies
- Updated `package.json` to move `daisyui` to peer and dev dependencies

## @rjsf/mui

- Updated the `README.md` file for dependencies
- BREAKING CHANGE: Upgraded MUI to version 7, dropping support for earlier versions due to conversion of `Grid`s to v7 version (a MUI breaking change)

## @rjsf/react-bootstrap

- Updated the `README.md` file for dependencies

## @rjsf/semantic-ui

- Updated the `README.md` file for dependencies
- Deprecated the theme due to it appearing to be a dead project

## @rjsf/shadcn

- Updated the `README.md` file for dependencies

## @rjsf/utils

- Fixed form data propagation with `patternProperties` [#4617](https://github.com/rjsf-team/react-jsonschema-form/pull/4617)
- Updated the `GlobalUISchemaOptions` types to extend `GenericObjectType` to support user-defined values for their extensions

## Dev / docs / playground

- Updated `playground` to use MUI version 7
- Updated `v6 upgrade guide.md` to note the breaking change for MUI 7 and deprecation of `semantic-ui`

# 6.0.0-beta.8

## @rjsf/chakra-ui

- Added `getChakra` to package exports
- Restored the `ui:options` customization
- Updated `SelectWidget` to only pick the first element in a list when single selection is active, fixing [#4623](https://github.com/rjsf-team/react-jsonschema-form/issues/4623)

## @rjsf/core

- Updated `LayoutGridField` to use the pre-existing `UI_GLOBAL_OPTIONS_KEY` instead of its own incorrect one.

## @rjsf/utils

- Fixed form data propagation with `patternProperties` [#4617](https://github.com/rjsf-team/react-jsonschema-form/pull/4617)
- Fixed issue where oneOf schema references could not be modified when defaults were set, fixing [#4580](https://github.com/rjsf-team/react-jsonschema-form/issues/4580).
- Updated the `GlobalUISchemaOptions` types to extend `GenericObjectType` to support user-defined values for their extensions

## Dev / docs / playground

- Updated precompiled schemas documentation in `validation.md` based on v6 changes, addressing [#4618](https://github.com/rjsf-team/react-jsonschema-form/issues/4618)

# 6.0.0-beta.7

## @rjsf/core

- Fixed crash in `LayoutGridField` when the 'name' field is missing in the grid schema for a component

# 6.0.0-beta.6

## @rjsf/utils

- Updated the `Field` type to add the optional `TEST_IDS?: TestIdShape` prop to it to support exposing the `TEST_IDS` static prop on `LayoutGridField`, `LayoutHeaderField` and `LayoutMultiSchemaField` for external users

# 6.0.0-beta.5

## Dev / docs / playground

- Updated the peer dependencies for all packages from `6.0.0-beta` to `^6.0.0-beta` to avoid `npm install` dependency resolution issues

# 6.0.0-beta.4

## Dev / docs / playground

- Updated the peer dependencies for all packages from `6` to `6.0.0-beta` to avoid `npm install` dependency resolution issues

# 6.0.0-beta.3

## Dev / docs / playground

- Updated the peer dependencies for all packages from `^6.0.0-beta.x` to `6` to avoid `npm install` dependency resolution issues

# 6.0.0-beta.2

## @rjsf/antd

- Updated `DescriptionField` to render the `description` using the `RichDescription` field

## @rjsf/chakra-ui

- Updated `DescriptionField` to render the `description` using the `RichDescription` field

## @rjsf/core

- Added new `RichDescription` component, refactored from `SchemaField` to support Rich Text descriptions in Markdown format
- Updated `DescriptionField` to render the `description` using the `RichDescription` field

## @rjsf/daisyui

- Updated `DescriptionField` to render the `description` using the `RichDescription` field
- Updated `FieldTemplate` to move the checkbox implementation into the `CheckboxWidget` adding the `description` for checkboxes
- Updated `package.json` to make the package publishable
- Updated `DaisyUIFrameProvider` to extract the bulk of the code into `DaisyUIFrameComponent` to add a `useEffect()` with a cleanup to remove the tailwind styles

## @rjsf/fluentui-rc

- Updated `DescriptionField` to render the `description` using the `RichDescription` field

## @rjsf/mui

- Updated `DescriptionField` to render the `description` using the `RichDescription` field

## @rjsf/react-bootstrap

- Updated `DescriptionField` to render the `description` using the `RichDescription` field
- Updated `CheckboxField` to remove the `checkbox` class that breaks the UI

## @rjsf/semantic-ui

- Updated `DescriptionField` to render the `description` using the `RichDescription` field

## @rjsf/shadcn

- Updated `DescriptionField` to render the `description` using the `RichDescription` field

## @rjsf/utils

- Updated the `description` field in field props to be a `string | ReactElement` and added `enableMarkdownInDescription` to the `GlobalUISchemaOptions` interface
- Support for bundled JSON Schemas [#4505](https://github.com/rjsf-team/react-jsonschema-form/issues/4505)
- Fixed issue with schema references in combinators(allOf, anyOf, oneOf) could not be modified when defaults were set, fixing [#4555](https://github.com/rjsf-team/react-jsonschema-form/issues/4555)

## Dev / docs / playground

- Updated the `snapshot-tests` to disable `getTestId()` for snapshots and updated the `formTests.tsx` to add tests for rich text descriptions for generic fields and the `CheckboxWidget`
- Updated the `uiSchema.md` to document new `enableMarkdownInDescription` prop
- Updated the `playground` to move `daisyui` theme choice after `chakra-ui` and to stop freezing the samples to avoid an `AJV` validation issue
  - Also removed `validator` from the `examples.ts` to fix [#4605](https://github.com/rjsf-team/react-jsonschema-form/issues/4605)
- Added a playground example for bundled JSON Schemas

# 6.0.0-beta.1

## @rjsf/antd

- BREAKING CHANGE: Refactored `ArrayFieldItemTemplate` to use the new `ArrayFieldItemButtonsTemplate`
- Updated the `ArrayFieldTemplate`, `ObjectFieldTemplate`, and `WrapIfAdditionalTemplate` to a unique id using the `buttonId()` function and adding consistent marker classes
- Implemented the `GridTemplate` component, adding it to the `templates` for the theme
- BREAKING CHANGE: Removed support for version 4 of `antd`
- Updated `ArrayFieldItemTemplate` to replace `Button.Group` with `Space.Compact` since `Button.Group` is deprecated in `antd` version 5
- Upgraded to `@ant-design/icon@5`
- BREAKING CHANGE: Removed the addition of `Bootstrap 3` classes from the `SchemaField` and added `rjsf-` prefix to marker classes, thereby changing theme `FieldTemplate` className prop output and associated snapshots

## @rjsf/chakra-ui

- BREAKING CHANGE: upgrade from v2 to v3
- BREAKING CHANGE: remove deprecated `@chakra-ui/icon` in favor of `lucide-react`
- BREAKING CHANGE: Refactored `ArrayFieldItemTemplate` to use the new `ArrayFieldItemButtonsTemplate`
- Updated the `ArrayFieldTemplate`, `ObjectFieldTemplate`, and `WrapIfAdditionalTemplate` to a unique id using the `buttonId()` function and adding consistent marker classes
- Implemented the `GridTemplate` component, adding it to the `templates` for the theme
- BREAKING CHANGE: Removed the addition of `Bootstrap 3` classes from the `SchemaField` and added `rjsf-` prefix to marker classes, thereby changing theme `FieldTemplate` className prop output and associated snapshots

## @rjsf/core

- BREAKING CHANGE: Updated `ArrayField` to provide the `buttonsProps` to the `ArrayFieldItemTemplateType`
- Added `ArrayFieldItemButtonsTemplate` component as a refactor of all the common buttons code from all the `ArrayFieldItemTemplate` implementations, adding a unique id using the `buttonId()` function
- Refactored `ArrayFieldItemTemplate` to use the new `ArrayFieldItemButtonsTemplate`
- Updated the `ArrayFieldTemplate`, `ObjectFieldTemplate`, and `WrapIfAdditionalTemplate` to a unique id using the `buttonId()` function and adding consistent marker classes
- Implemented the `GridTemplate` component, adding it to the `templates` for the theme
- Implemented the new `LayoutGridField`, `LayoutMultiSchemaField` and `LayoutHeaderField` fields, adding them to the `fields` list
- BREAKING CHANGE: Removed support for the deprecated `schema.enumNames` and `uiSchema.classNames` as well as the deprecated `acceptcharset` prop on `Form`
- BREAKING CHANGE: Moved the addition of `Bootstrap 3` classes from the `SchemaField` to the `WrapIfAdditionalTemplate`, thereby affecting all the other themes, fixing [#2280](https://github.com/rjsf-team/react-jsonschema-form/issues/2280)
- BREAKING CHANGE: Added `rjsf-` prefix onto the following marker classes used in the fields and templates:
  - `field`, `field-<schema.type>`, `field-error`, `field-hidden`, `field-array`, `field-array-of-<schema.type>`, `field-array-fixed-items`, `array-item`, `config-error`, `array-item-add`, `array-item-copy`, `array-item-move-down`, `array-item-move-up`, `array-item-remove`, `object-property-expand`
- Added support for `patternProperties` [#1944](https://github.com/rjsf-team/react-jsonschema-form/issues/1944)

## @rjsf/daisyui

- Added new theme!

## @rjsf/fluent-ui

- BREAKING CHANGE: Deleted this theme in favor of `fluentui-rc`

## @rjsf/fluentui-rc

- BREAKING CHANGE: Refactored `ArrayFieldItemTemplate` to use the new `ArrayFieldItemButtonsTemplate`
- Updated the `ArrayFieldTemplate`, `ObjectFieldTemplate`, and `WrapIfAdditionalTemplate` to a unique id using the `buttonId()` function and adding consistent marker classes
- Implemented the `GridTemplate` component, adding it to the `templates` for the theme
- BREAKING CHANGE: Removed the addition of `Bootstrap 3` classes from the `SchemaField` and added `rjsf-` prefix to marker classes, thereby changing theme `FieldTemplate` className prop output and associated snapshots

## @rjsf/material-ui

- BREAKING CHANGE: Deleted this theme in favor of `mui`

## @rjsf/mui

- BREAKING CHANGE: Refactored `ArrayFieldItemTemplate` to use the new `ArrayFieldItemButtonsTemplate`
- Updated the `ArrayFieldTemplate`, `ObjectFieldTemplate`, and `WrapIfAdditionalTemplate` to a unique id using the `buttonId()` function and adding consistent marker classes
- Updated the theme to use `Grid2` instead of the deprecated `Grid`
- Implemented the `GridTemplate` component, adding it to the `templates` for the theme
- BREAKING CHANGE: Removed the addition of `Bootstrap 3` classes from the `SchemaField` and added `rjsf-` prefix to marker classes, thereby changing theme `FieldTemplate` className prop output and associated snapshots

## @rjsf/semantic-ui

- BREAKING CHANGE: Refactored `ArrayFieldItemTemplate` to use the new `ArrayFieldItemButtonsTemplate`
- Updated the `ArrayFieldTemplate`, `ObjectFieldTemplate`, and `WrapIfAdditionalTemplate` to a unique id using the `buttonId()` function and adding consistent marker classes
- Implemented the `GridTemplate` component, adding it to the `templates` for the theme
- BREAKING CHANGE: Removed the addition of `Bootstrap 3` classes from the `SchemaField` and added `rjsf-` prefix to marker classes, thereby changing theme `FieldTemplate` className prop output and associated snapshots
- BREAKING CHANGE: Removed support for the v1 version of `semantic-ui-react`

## @rjsf/shadcn

- Added new theme!

## @rjsf/utils

- BREAKING CHANGE: Refactored the `ArrayFieldItemTemplateType` to extract out all the button related props to `ArrayFieldItemButtonsTemplateType`, adding `buttonsProps: ArrayFieldItemButtonsTemplateType` as a new prop
  - Also created a deprecated alias type `ArrayFieldTemplateItemType` that points to `ArrayFieldItemTemplateType` for backwards compatibility
- Added new `GridTemplateProps` type
- BREAKING CHANGE: Added two the following new, required props to `TemplatesType`:
  - `ArrayFieldItemButtonsTemplate: ComponentType<ArrayFieldItemButtonsTemplateType<T, S, F>>;`
  - `GridTemplate: ComponentType<GridTemplateProps>`
- BREAKING CHANGE: Updated the `SchemaUtilsType` to add new validator-based functions to the interface
- Added the following new non-validator utility functions:
  - `buttonId<T>(id: IdSchema<T> | string, btn: 'add' | 'copy' | 'moveDown' | 'moveUp' | 'remove')`: used to generate consistent ids for RJSF buttons
  - `getTestIds(): TestIdShape`: Returns an object of test IDs that can only be used in test mode, helpful for writing unit tests for React components
  - `hashObject(object: unknown): string`: Stringifies an `object` and returns the hash of the resulting string
  - `hashString(string: string): string`: Hashes a string into hex format
  - `lookupFromFormContext<T = any, S extends StrictRJSFSchema = RJSFSchema, F extends FormContextType = any>(regOrFc: Registry<T, S, F> | Registry<T, S, F>['formContext'], toLookup: string, fallback?: unknown)`: Given a React JSON Schema Form registry or formContext object, return the value associated with `toLookup`
- Added the following new validator-based utility functions:
  - `findFieldInSchema<T = undefined, S extends StrictRJSFSchema = RJSFSchema, F extends FormContextType = any>(validator: ValidatorType<T, S, F>, rootSchema: S, path: string | string[], schema: S, formData?: T, experimental_customMergeAllOf?: Experimental_CustomMergeAllOf<S>): FoundFieldType<S>`: Finds the field specified by the `path` within the root or recursed `schema`
  - `findSelectedOptionInXxxOf<T = any, S extends StrictRJSFSchema = RJSFSchema, F extends FormContextType = any>(validator: ValidatorType<T, S, F>, rootSchema: S, schema: S, fallbackField: string,xxx: 'anyOf' | 'oneOf', formData?: T, experimental_customMergeAllOf?: Experimental_CustomMergeAllOf<S>): S | undefined`: Finds the option that matches the selector field in the `schema` or undefined if nothing is selected
  - `getFromSchema<T = any, S extends StrictRJSFSchema = RJSFSchema, F extends FormContextType = any>(validator: ValidatorType<T, S, F>, rootSchema: S, schema: S, path: string | string[], defaultValue: T | S, experimental_customMergeAllOf?: Experimental_CustomMergeAllOf<S>): T | S`: Helper that acts like lodash's `get` but additionally retrieves `$ref`s as needed to get the path for schemas
- BREAKING CHANGE: Removed support for the deprecated `schema.enumNames` from `getOptionsList()` while switching the order of its generic types
- BREAKING CHANGE: Removed the deprecated `getMatchingOption()` and `mergeValidationData()` from the library export and the `SchemaUtilsType` interface
- BREAKING CHANGE: Removed the deprecated `toErrorList()` function from the `ValidatorType` interface
- BREAKING CHANGE: Removed the deprecated `RJSF_ADDITONAL_PROPERTIES_FLAG` constant
- Updated the `WrapIfAdditionalTemplateProps` to include `hideError` and `rawErrors` in support of moving `Bootstrap 3` marker classes out of `SchemaField`
- Added support for `patternProperties` [#1944](https://github.com/rjsf-team/react-jsonschema-form/issues/1944)
- Updated `getTemplate()` to allow per-field customization using string key from `Registry`, fixing [#3695](https://github.com/rjsf-team/react-jsonschema-form/issues/3695).
- Updated `TemplatesType` to allow for a string key to be used to reference a custom template in the `Registry`, fixing [#3695](https://github.com/rjsf-team/react-jsonschema-form/issues/3695)
- Updated tests to cover the new `getTemplate()` functionality

## @rjsf/validator-ajv6

- BREAKING CHANGE: This deprecated validator has been removed

## @rjsf/validator-ajv8

- BREAKING CHANGE: Removed the implementation of the deprecated `toErrorList()` function from the validator implementations

## Dev / docs / playground

- Updated the playground to Chakra UI v3
- Updated the playground to remove `fluent-ui` theme
- Updated the `custom-templates.md` documentation for the changes to the `ArrayFieldTemplateItem` and add the two new templates
- Updated the `utility-functions.md` documentation to add the `buttonId()` function
- Added the `v6.x upgrade guide.md` documentation
- Updated the `playground` to add a `Layout Grid` example and made the selected example now be part of the shared export
- Replaced Lerna with Nx, updated all lerna commands to use the Nx CLI
- BREAKING CHANGE: Updated all `peerDependencies` to change minimal `React` support to `>=18`
- Added documentation and playground example for `patternProperties`
- Updated `advanced-customization/custom-templates` with the new feature.

# 6.0.0-alpha.0

## @rjsf/bootstrap-4

- BREAKING CHANGE: Package has been replaced with `@rjsf/react-bootstrap`. `react-boostrap` v1 / Bootstrap 4 are no longer supported in RJSF v6.

## @rjsf/material-ui

- BREAKING CHANGE: Removed `@rjsf/material-ui` package. Material UI v4 (`@material-ui/core`) has been deprecated since September 2021. To use Material UI v5 (`@mui/core`) with RJSF, please use the `@rjsf/mui` theme instead.

## @rjsf/react-bootstrap

- Added new package to replace `@rjsf/bootstrap-4`
- `react-bootstrap` peer dependency bumped to `^2.0.0`, corresponding to Bootstrap 5
- CheckboxesWidget: Remove deprecated prop `custom`
- IconButton: Remove deprecated `block` prop
- RangeWidget: Use `FormRange` component
- SelectWidget: Use new FormSelect component, remove `bsPrefix` prop to achieve correct styling

## Dev / docs / playground

- Updated the playground to remove `material-ui-4` theme and replace the `bootstrap-4` theme with `react-bootstrap`

# 5.24.10

## Dev / docs / playground

- Updated all `package.json` files in the `packages` directories to remove the `exports` blocks, fixing [#4537](https://github.com/rjsf-team/react-jsonschema-form/issues/4537)

# 5.24.9

## @rjsf/antd

- Fixed ts errors in newer antd versions [#4525](https://github.com/rjsf-team/react-jsonschema-form/issues/4525)

## @rjsf/chakra-ui

- Restricted the chakra-react-select peerDependency to <6.0.0, fixing [#4539](https://github.com/rjsf-team/react-jsonschema-form/issues/4539)

## @rjsf/core

- Do not display input field in MultiSchemaField with null type

## @rjsf/mui

- Fixed issue in BaseInputTemplate where input props were passed to `slotProps.htmlInput`, which does not work in MUI v5.

## @rjsf/utils

- Fixed issue with schema combinators(allOf, anyOf, oneOf) could not be modified when defaults were set, fixing [#4555](https://github.com/rjsf-team/react-jsonschema-form/issues/4555)

## Dev / docs / playground

- Updated docs for ArrayFieldItemTemplate to include prop `onCopyIndexClick`, fixing [#4507](https://github.com/rjsf-team/react-jsonschema-form/issues/4507)
- Use antd 5 in playground
- Updated docs to clarify that errors raised within a widget are not caught during form validation
- Updated docs where objects typed as RJSFValidationError were not valid ([#4558](https://github.com/rjsf-team/react-jsonschema-form/issues/4558))

# 5.24.8

## @rjsf/antd

- Fixed the total disable of the `RadioWidget`, fixing [#4481](https://github.com/rjsf-team/react-jsonschema-form/issues/4481)

## @rjsf/validator-ajv8

- Fixed up the ESM build to properly handle ESM imports for `compileSchemaValidatorsCode()` by adding a new `ajvReplacer.ts` and using it

## Dev / docs / playground

- Updated `snapshot-tests` to add validation of disable `RadioWidget` via the `Form` prop as well as `uiSchema`

# 5.24.7

## Dev / docs / playground

- Fixed build issues with small change to `core/src/tsconfig.json` and improvements to the `exports` for ESM support
- Run NX serially in the pipelines to avoid odd out-of-sequence build issues

# 5.24.6

## @rjsf/core

- Fixed `src/tsconfig.json` to add the `tsc-alias` block to support proper fixing up of ESM import

# 5.24.5

## @rjsf/utils

- Fixed `package.json` to remove `node` from the `exports` block to fix ESM support

# 5.24.4

## @rjsf/utils

- Fixed issue with customValidate errors are not cleared when the form is valid [4365](https://github.com/rjsf-team/react-jsonschema-form/pull/4365) due to regression
- Add missing `experimental_customMergeAllOf` argument to `ensureFormDataMatchingSchema` introduced by [4388](https://github.com/rjsf-team/react-jsonschema-form/pull/4388)

## Dev / docs / playground

- Improved the ESM support for all public packages by adding explicit `exports` to each public `package.json`
- Updated the ESM builds to use `tsc-alias` to add `.js` onto all ESM imports

# 5.24.3

## @rjsf/utils

- Rollback [4446](https://github.com/rjsf-team/react-jsonschema-form/pull/4446) due to regression

## Dev / docs / playground

- Fixed issue with selector, where validator was getting refreshed on clicking on anything in selector. [#4472](https://github.com/rjsf-team/react-jsonschema-form/pull/4472)

# 5.24.2

## @rjsf/utils

- switch `lodash.isEqualWith` to `fast-equals.createCustomEqual` providing `areFunctionsEqual` assuming any functions are equal.
- Fixed issue with oneOf selector can be modified in readonly mode, fixing [#4460](https://github.com/rjsf-team/react-jsonschema-form/issues/4460)
- Fixed issue with fields inside an array can't be set to empty when a default is set, fixing [#4456](https://github.com/rjsf-team/react-jsonschema-form/issues/4456)
- Fixed issue with file accept attribute, fixing [#4404](https://github.com/rjsf-team/react-jsonschema-form/issues/4404).

## @rjsf/mui

- Fixed issue with file accept attribute, fixing [#4404](https://github.com/rjsf-team/react-jsonschema-form/issues/4404).

# 5.24.1

## @rjsf/utils

- Fixed documentation for `getChangedFields()`

## Dev / docs / playground

- Updated the peer dependencies for `@rjsf/*` to be `5.24.x`
- Added documentation for `getChangedFields()`

# 5.24.0

## @rjsf/core

- Fixed issue with schema if/then/else conditions where switching to then/else subschemas did not reflect the actual validation errors in the onChange event, fixing [#4249](https://github.com/rjsf-team/react-jsonschema-form/issues/4249) and improving performance.
- Fixed issue error message will not be cleared after the controlled Form formData is changed. Fixes [#4426](https://github.com/rjsf-team/react-jsonschema-form/issues/4426)

## @rjsf/utils

- Fixed issue with formData not updating when dependencies change, fixing [#4325](https://github.com/rjsf-team/react-jsonschema-form/issues/4325)
- Fixed issue with assigning default values to formData with deeply nested required properties, fixing [#4399](https://github.com/rjsf-team/react-jsonschema-form/issues/4399)
- Fixed issue error message will not be cleared after the controlled Form formData is changed. Fixes [#4426](https://github.com/rjsf-team/react-jsonschema-form/issues/4426)
- Fix for AJV [$data](https://ajv.js.org/guide/combining-schemas.html#data-reference) reference in const property in schema treated as default/const value. The issue is mentioned in [#4361](https://github.com/rjsf-team/react-jsonschema-form/issues/4361).
- Switched uses of `lodash.isEqual()` to `@rjsf/utils.deepEquals`.

## @rjsf/validator-ajv8

- Partially fixed issue where dependency errors do not show `title` or `ui:title`. This fix only applicable if we use an ajv-i18n localizer. Ref. [#4402](https://github.com/rjsf-team/react-jsonschema-form/issues/4402).
- Switched uses of `lodash.isEqual()` to `@rjsf/utils.deepEquals` at precompiledValidator.

# 5.23.2

## @rjsf/core

- Fix default value population when switching between options in `MultiSchemaField` [#4375](https://github.com/rjsf-team/react-jsonschema-form/pull/4375). Fixes [#4367](https://github.com/rjsf-team/react-jsonschema-form/issues/4367)

## @rjsf/utils

- Short-circuit `File` and `Date` constructor access in isObject to optimize performance in scenarios where `globalThis` is a `Proxy` that incurs overhead for each class constructor access ([#4413](https://github.com/rjsf-team/react-jsonschema-form/pull/4413)). Fixes [#4409](https://github.com/rjsf-team/react-jsonschema-form/issues/4409)

## @rjsf/validator-ajv8

- Fixed issue where `ui:title` in anyOf/oneOf is not shown in error messages. Fixes [#4368](https://github.com/rjsf-team/react-jsonschema-form/issues/4368)

# 5.23.1

## @rjsf/chakra-ui

- Updated `package.json` to restrict `@chakra-ui/react`'s peer dependency to be < 3.0.0, fixing [#4390](https://github.com/rjsf-team/react-jsonschema-form/issues/4390)

## @rjsf/core

- Updated `NumberField` to properly pass through the `errorSchema` and `id` in the onChange handler, fixing [#4382](https://github.com/rjsf-team/react-jsonschema-form/issues/4382)

## Dev / docs / playground

- Updated the peer dependencies for `@rjsf/*` to be `5.23.x`

# 5.23.0

## @rjsf/core

- Updated `SchemaField` to no longer make schema fields with const read-only by default, partially fixing [#4344](https://github.com/rjsf-team/react-jsonschema-form/issues/4344)

## @rjsf/utils

- Updated `Experimental_DefaultFormStateBehavior` to add a new `constAsDefaults` option
- Updated `getDefaultFormState()` to use the new `constAsDefaults` option to control how const is used for defaulting, fixing [#4344](https://github.com/rjsf-team/react-jsonschema-form/issues/4344), [#4361](https://github.com/rjsf-team/react-jsonschema-form/issues/4361) and [#4377](https://github.com/rjsf-team/react-jsonschema-form/issues/4377)
- Use `experimental_customMergeAllOf` option in functions that have previously missed it.
- Updated `ErrorSchemaBuilder` methods `addErrors` and `setErrors` to prevent duplicate error messages.

## @rjsf/validator-ajv8

- Fixed issue where error messages do not have `title` or `ui:title` if a `Localizer` function is used. Fixes [#4387](https://github.com/rjsf-team/react-jsonschema-form/issues/4387)

## Dev / docs / playground

- Updated the playground to add a selector for the `constAsDefaults` option

# 5.22.4

## @rjsf/utils

- Fixed issue with array schema defaults not applying properly when formData is an empty array, fixing [#4335](https://github.com/rjsf-team/react-jsonschema-form/issues/4335).

## Dev / docs / playground

- Fix issue 'Maximum call stack size exceeded' with playground share with large content.

# 5.22.3

## @rjsf/utils

- Fixed deep nested dependencies issue with assigning values to formData, fixing [#4334](https://github.com/rjsf-team/react-jsonschema-form/issues/4334)

# 5.22.2

## @rjsf/core

- Fix an issue where only the first file was uploaded when users selected multiple files for upload.
- Fixed validation regression Form not revalidating after formData change, fixing [#4343](https://github.com/rjsf-team/react-jsonschema-form/issues/4343)

## @rjsf/validator-ajv8

- Fixed `AJV8Validator#transformRJSFValidationErrors` to replace the error message field with either the `uiSchema`'s `ui:title` field if one exists or the `parentSchema` title if one exists. Fixes [#4348](https://github.com/rjsf-team/react-jsonschema-form/issues/4348)

# 5.22.1

## Dev / docs / playground

- Bumped peer dependencies to 5.22.x due to updated type definition and API changes in @rjsf/utils

# 5.22.0

## @rjsf/core

- Updated `MultiSchemaField` to call the `onChange` handler after setting the new option, fixing [#3997](https://github.com/rjsf-team/react-jsonschema-form/issues/3977) and [#4314](https://github.com/rjsf-team/react-jsonschema-form/issues/4314)

## @rjsf/utils

- Added `experimental_customMergeAllOf` option to `retrieveSchema()` and `getDefaultFormState()` to allow custom merging of `allOf` schemas
- Made fields with const property pre-filled and readonly, fixing [#2600](https://github.com/rjsf-team/react-jsonschema-form/issues/2600)
- Added `mergeDefaultsIntoFormData` option to `Experimental_DefaultFormStateBehavior` type to control how to handle merging of defaults
- Updated `mergeDefaultsWithFormData()` to add new optional `defaultSupercedesUndefined` that when true uses the defaults rather than `undefined` formData, fixing [#4322](https://github.com/rjsf-team/react-jsonschema-form/issues/4322)
- Updated `getDefaultFormState()` to pass true to `mergeDefaultsWithFormData` for `defaultSupercedesUndefined` when `mergeDefaultsIntoFormData` has the value `useDefaultIfFormDataUndefined`, fixing [#4322](https://github.com/rjsf-team/react-jsonschema-form/issues/4322)
- Updated `getClosestMatchingOption()` to improve the scoring of sub-property objects that are provided over ones that aren't, fixing [#3997](https://github.com/rjsf-team/react-jsonschema-form/issues/3977) and [#4314](https://github.com/rjsf-team/react-jsonschema-form/issues/4314)

## Dev / docs / playground

- Updated the `form-props.md` to add documentation for the new `experimental_customMergeAllOf` props and the `experimental_defaultFormStateBehavior.mergeDefaultsIntoFormData` option
- Updated the `utility-functions.md` to add documentation for the new optional `defaultSupercedesUndefined` parameter and the two missing optional fields on `getDefaultFormState()`
- Updated the `custom-templates.md` to add a section header for wrapping `BaseInputTemplate`
- Updated the playground to add controls for the new `mergeDefaultsIntoFormData` option
  - In the process, moved the `Show Error List` component over one column, making it inline radio buttons rather than a select

# 5.21.2

## @rjsf/core

- Updated `SchemaField` to pass `required` flag to `_AnyOfField`/`_OneOfField`
- Updated `Form` to deal with null objects in `filterErrorsBasedOnSchema()`, fixing [#4306](https://github.com/rjsf-team/react-jsonschema-form/issues/4306)

## @rjsf/utils

- Updated `ErrorSchemaBuilder` to support adding, updating, and removing paths that are numbers, fixing [#4297](https://github.com/rjsf-team/react-jsonschema-form/issues/4297)
- Updated `retrieveSchema` to not merge `contains` properties in `allOf` schema lists, fixing [#2923](https://github.com/rjsf-team/react-jsonschema-form/issues/2923#issuecomment-1946034240)

## Dev / docs / playground

- Updated the `custom-widgets-fields.md` to add examples of wrapping a widget/field

# 5.21.1

## @rjsf/utils

- Revert of updating `deepEquals()` from [#4292]

## @validator-ajv8

- Revert of using `deepEquals()` instead of `lodash.isEqual()` from [#4292]

# 5.21.0

## @rjsf/core

- Updated `Form` to fix `focusOnError()` to support the ids that include dots, fixing [#4279](https://github.com/rjsf-team/react-jsonschema-form/issues/4279)

## @rjsf/mui

- Updated the peer dependencies for `@mui/material` and `@mui/icon-material`, fixing [4283](https://github.com/rjsf-team/react-jsonschema-form/issues/4283)

## @rjsf/utils

- Fixes an issue with dependencies computeDefaults to ensure we can get the dependencies defaults [#4271](https://github.com/rjsf-team/react-jsonschema-form/issues/4271)
- Updated `deepEquals()` to use `fast-equals.createCustomEqual()` instead of `lodash.isEqualWith()`, fixing [#4291](https://github.com/rjsf-team/react-jsonschema-form/issues/4291)
  - Switched uses of `lodash.isEqual()` to `deepEquals()` in many of the utility functions as well

## @validator-ajv8

- Use `@rjsf/utils` `deepEquals()` instead of `lodash.isEqual()` to improve performance, fixing [#4291](https://github.com/rjsf-team/react-jsonschema-form/issues/4291)

## Dev / docs / playground

- Updated the playground to use `@mui/*` version 6, changing the name of the dropdown from `material-ui-5` to `mui`

# 5.20.1

## Dev / docs / playground

- Updated the peer dependencies to `5.20.x` due to types and API changes in `@rjsf/utils`

# 5.20.0

## @rjsf/core

- Support allowing raising errors from within a custom Widget [#2718](https://github.com/rjsf-team/react-jsonschema-form/issues/2718)
- Updated `ArrayField`, `BooleanField` and `StringField` to call `optionsList()` with the additional `UiSchema` parameter, fixing [#4215](https://github.com/rjsf-team/react-jsonschema-form/issues/4215) and [#4260](https://github.com/rjsf-team/react-jsonschema-form/issues/4260)

## @rjsf/utils

- Updated the `WidgetProps` type to add `es?: ErrorSchema<T>, id?: string` to the params of the `onChange` handler function
- Updated `UIOptionsBaseType` to add the new `enumNames` prop to support an alternate way to provide labels for `enum`s in a schema, fixing [#4215](https://github.com/rjsf-team/react-jsonschema-form/issues/4215)
- Updated `optionsList()` to take an optional `uiSchema` that is used to extract alternate labels for `enum`s or `oneOf`/`anyOf` in a schema, fixing [#4215](https://github.com/rjsf-team/react-jsonschema-form/issues/4215) and [#4260](https://github.com/rjsf-team/react-jsonschema-form/issues/4260)
  - NOTE: The generics for `optionsList()` were expanded from `<S extends StrictRJSFSchema = RJSFSchema>` to `<S extends StrictRJSFSchema = RJSFSchema, T = any, F extends FormContextType = any>` to support the `UiSchema`.

## Dev / docs / playground

- Update the `custom-widget-fields.md` to add documentation for how to raise errors from a custom widget or field

# 5.19.4

## @rjsf/core

- Fix XSS when rendering schema validation errors [#4254](https://github.com/rjsf-team/react-jsonschema-form/issues/2718)
  - NOTE: This will have potential consequences if you are using the [translateString](https://rjsf-team.github.io/react-jsonschema-form/docs/api-reference/form-props/#translatestring) feature and are trying to render HTML. Switching to [Markdown](https://www.markdownguide.org/) will solve your problems.

## @rjsf/utils

- Updated the `ValidatorType` interface to add an optional `reset?: () => void` prop that can be implemented to reset a validator back to initial constructed state
  - Updated the `ParserValidator` to provide a `reset()` function that clears the schema map
- Also updated the default translatable string to use `Markdown` rather than HTML tags since we now render them with `Markdown`

## @rjsf/validator-ajv8

- Updated the `AJV8Validator` to implement the `reset()` function to remove cached schemas in the `ajv` instance

## Dev / docs / playground

- Updated the `Validator` dropdown to add `AJV8 (discriminator)` which sets the AJV validator [discriminator](https://ajv.js.org/json-schema.html#discriminator) option to `true` to support testing schemas with that option in them

# 5.19.3

## @rjsf/antd

- SelectWidget now displays an empty option when appropriate, fixing [#4197](https://github.com/rjsf-team/react-jsonschema-form/issues/4197)

## @rjsf/chakra-ui

- SelectWidget now displays an empty option when appropriate, fixing [#4197](https://github.com/rjsf-team/react-jsonschema-form/issues/4197)

## @rjsf/fluentui-rc

- SelectWidget now displays an empty option when appropriate, fixing [#4197](https://github.com/rjsf-team/react-jsonschema-form/issues/4197)

## @rjsf/material-ui

- SelectWidget now displays an empty option when appropriate, fixing [#4197](https://github.com/rjsf-team/react-jsonschema-form/issues/4197)

## @rjsf/mui

- SelectWidget now displays an empty option when appropriate, fixing [#4197](https://github.com/rjsf-team/react-jsonschema-form/issues/4197)

## @rjsf/semantic-ui

- SelectWidget now displays an empty option when appropriate, fixing [#4197](https://github.com/rjsf-team/react-jsonschema-form/issues/4197)

# 5.19.2

## @rjsf/core

- Removed `.only` on tests that was accidentally added in `5.19.0`

# 5.19.1

## Dev / docs / playground

- Bumped the peer dependencies to `5.19.x` due to use of new API in `5.19.0`

# 5.19.0

## @rjsf/antd

- Updated `AltDateWidget` to use the new `dateRangeOptions()` function in `utils` to support relative Years and reversing the order of the Year choices

## @rjsf/chakra-ui

- Updated `AltDateWidget` to use the new `dateRangeOptions()` function in `utils` to support relative Years and reversing the order of the Year choices

## @rjsf/core

- Fixed case where `readOnly` from a JSON Schema was not applied in SchemaField ([#4236](https://github.com/rjsf-team/react-jsonschema-form/issues/4236))
- Updated `AltDateWidget` to use the new `dateRangeOptions()` function in `utils` to support relative Years and reversing the order of the Year choices

## @rjsf/utils

- Added a new `dateRangeOptions()` function to implement relative Years in (via negative ranges) and reversing the order of the Year choices

## Dev / docs / playground

- Added documentation for the new `dateRangeOptions()` function as well as showing examples of using relative Years and reversed Year ordering

# 5.18.6

## @rjsf/antd

- Fix disabled property of options in CheckboxesWidget and RadioWidget ([#4216](https://github.com/rjsf-team/react-jsonschema-form/pull/4216))

## @rjsf/core

- Fixed `omitExtraData` not working in `onSubmit` and `validateForm`; fixing [#4187](https://github.com/rjsf-team/react-jsonschema-form/issues/4187), [#4165](https://github.com/rjsf-team/react-jsonschema-form/issues/4165) and [#4109](https://github.com/rjsf-team/react-jsonschema-form/issues/4109)

## @rjsf/utils

- Fix IdSchema and PathSchema types ([#4196](https://github.com/rjsf-team/react-jsonschema-form/pull/4196))

## @rjsf/validator-ajv6

- Fix IdSchema and PathSchema types ([#4196](https://github.com/rjsf-team/react-jsonschema-form/pull/4196))

## @rjsf/validator-ajv8

- Fix IdSchema and PathSchema types ([#4196](https://github.com/rjsf-team/react-jsonschema-form/pull/4196))

# 5.18.5

## @rjsf/antd

- Updated widgets to handle undefined `target` in `onFocus` and `onBlur` handlers

## @rjsf/bootstrap4

- Updated widgets to handle undefined `target` in `onFocus` and `onBlur` handlers

## @rjsf/chakra-ui

- Updated widgets to handle undefined `target` in `onFocus` and `onBlur` handlers

## @rjsf/core

- Fix case where NumberField would not properly reset the field when using programmatic form reset (#4202)[https://github.com/rjsf-team/react-jsonschema-form/issues/4202]
- Updated widgets to handle undefined `target` in `onFocus` and `onBlur` handlers
- Fix field disable or readonly property can't cover globalOptions corresponding property (#4212)[https://github.com/rjsf-team/react-jsonschema-form/pull/4212]
- Added support for `default` values in `additionalProperties` in [#4199](https://github.com/rjsf-team/react-jsonschema-form/issues/4199), fixing [#3195](https://github.com/rjsf-team/react-jsonschema-form/issues/3915)

## @rjsf/fluent-ui

- Updated widgets to handle undefined `target` in `onFocus` and `onBlur` handlers

## @rjsf/fluentui-rc

- Updated widgets to handle undefined `target` in `onFocus` and `onBlur` handlers

## @rjsf/material-ui

- Updated widgets to handle undefined `target` in `onFocus` and `onBlur` handlers

## @rjsf/mui

- Updated widgets to handle undefined `target` in `onFocus` and `onBlur` handlers

## @rjsf/semantic-ui

- Updated widgets to handle undefined `target` in `onFocus` and `onBlur` handlers

## @rjsf/validator-ajv6

- Improved performance issues with large schema dependencies and oneOf conditions [#4203](https://github.com/rjsf-team/react-jsonschema-form/issues/4203).

## @rjsf/validator-ajv8

- Improved performance issues with large schema dependencies and oneOf conditions [#4203](https://github.com/rjsf-team/react-jsonschema-form/issues/4203).

# 5.18.4

## Dev / docs / playground

- Fixed typo in `constants.ts`, `Form.tsx`

# 5.18.3

## @rjsf/semantic-ui

- Added support for version 2 in the `peerDependencies`

## Dev / docs / playground

- Bumped devDependencies on `react` to `18.x`
- Fixed typo in `custom-widgets-fields.md` in the documentation
- Updated the `LICENSE.md` to include the proper copyright dates and owner

# 5.18.2

## @rjsf/core

- Fixed Programmatic submit not working properly in Firefox [#3121](https://github.com/rjsf-team/react-jsonschema-form/issues/3121)

## @rjsf/utils

- [#4116](https://github.com/rjsf-team/react-jsonschema-form/issues/4116) Fix Maximum call stack size exceeded when encountering circular definitions ([Link to PR](https://github.com/rjsf-team/react-jsonschema-form/pull/4123))

# 5.18.0

## @rjsf/antd

- Fix issue where the theme provided by the ConfigProvider under antd v5 wasn't respected thereby rendering the form items unusable under dark themes [#4129](https://github.com/rjsf-team/react-jsonschema-form/issues/4129)

## @rjsf/core

- Fix Error state not resetting when schema changes [#4079](https://github.com/rjsf-team/react-jsonschema-form/issues/4079)

## @rjsf/mui

- Fixed the `SelectWidget` and `BaseInputTemplate` to filter out `errorSchema` and `autocomplete` from the `textFieldProps` being spread onto the `TextField`, fixing [#4134](https://github.com/rjsf-team/react-jsonschema-form/issues/4134)

## @rjsf/utils

- Added a new `skipEmptyDefault` option in `emptyObjectFields`, fixing [#3880](https://github.com/rjsf-team/react-jsonschema-form/issues/3880)
- Added a new `computeSkipPopulate` option in `arrayMinItems`, allowing custom logic to skip populating arrays with default values, implementing [#4121](https://github.com/rjsf-team/react-jsonschema-form/pull/4121).
- Fixed bug where the string `"\</strong>"` would get printed next to filenames when uploading files, and restored intended bolding of filenames fixing [#4120](https://github.com/rjsf-team/react-jsonschema-form/issues/4120).

## Dev / docs / playground

- Updated the documentation to describe how to use the `skipEmptyDefault` option.
- Fixed missing import of `Form` in usage documentation - fixing [#4127](https://github.com/rjsf-team/react-jsonschema-form/issues/4127)

# 5.17.1

## @rjsf/chakra-ui

- Added support for `UiSchema` `"ui:rows"` option for `textarea` elements, fixing [#4070](https://github.com/rjsf-team/react-jsonschema-form/issues/4070).

## @rjsf/core

- [#4091](https://github.com/rjsf-team/react-jsonschema-form/issues/4091) Added `errorSchema` to `ArrayFieldTemplate` props.

## @rjsf/utils

- [#4080](https://github.com/rjsf-team/react-jsonschema-form/issues/4080) - BREAKING CHANGE: Removed the `base64` object from the `@rjsf/utils` package. Note that this is a breaking change if you relied on the `base64` object exported by `@rjsf/utils`. Since this change caused [#4080](https://github.com/rjsf-team/react-jsonschema-form/issues/4080), and was only internally used by playground code, we are shipping this change in a patch release.
- [#4091](https://github.com/rjsf-team/react-jsonschema-form/issues/4091) Added `errorSchema` to the `ArrayFieldTemplateProps` type.

## Dev / docs / playground

- [#4080](https://github.com/rjsf-team/react-jsonschema-form/issues/4080) - Moved the `base64` encoder/decoder object to the Playground package.
- Added test configuration and script to the Playground.

# 5.17.0

## @rjsf/core

- Added support for `anyOf`/`oneOf` in `uiSchema`s in the `MultiSchemaField`, fixing [#4039](https://github.com/rjsf-team/react-jsonschema-form/issues/4039)
- Fix potential XSS vulnerability in the preview button of FileWidget, fixing [#4057](https://github.com/rjsf-team/react-jsonschema-form/issues/4057)

## @rjsf/utils

- [#4024](https://github.com/rjsf-team/react-jsonschema-form/issues/4024) Added `base64` to support `encoding` and `decoding` using the `UTF-8` charset to support the characters out of the `Latin1` range.
- Updated `enumOptionsValueForIndex()` to fix issue that filtered enum options with a value that was 0, fixing [#4067](https://github.com/rjsf-team/react-jsonschema-form/issues/4067)
- Changes the way of parsing the data URL, to fix [#4057](https://github.com/rjsf-team/react-jsonschema-form/issues/4057)

## Dev / docs / playground

- [#4024](https://github.com/rjsf-team/react-jsonschema-form/issues/4024) Updated the base64 references from (`atob` and `btoa`) to invoke the functions from the new `base64` object in `@rjsf/utils`.
- Updated the `uiSchema.md` documentation to describe how to use the new `anyOf`/`oneOf` support

# 5.16.1

## Dev / docs / playground

- Bumped peer dependencies due to new utils function

# 5.16.0

## @rjsf/core

- Pass indexed title from array into its items, adding enhancement asked in [#3983](https://github.com/rjsf-team/react-jsonschema-form/issues/3983)
- Removed `dateElementProps` function implementation, and replaced it with `getDateElementProps` from `@rjsf/utils`.
- Modify submit method to make it a public method, fixing [#4015](https://github.com/rjsf-team/react-jsonschema-form/issues/4015)
- Support file deletion for `format: "data-url"` in `FileWidget`, fixing [#3957](https://github.com/rjsf-team/react-jsonschema-form/issues/3957).

## @rjsf/antd

- Removed `dateElementProps` function implementation, and replaced it with `getDateElementProps` from `@rjsf/utils`.

## @rjsf/chakra-ui

- Removed `dateElementProps` function implementation, and replaced it with `getDateElementProps` from `@rjsf/utils`.

## @rjsf/mui

- Updated the `FieldErrorTemplate` and `FieldHelpTemplate` to support html-based errors that cause `<xxxx> cannot appear as a descendant of <p>` browser warnings, fixing [#4031](https://github.com/rjsf-team/react-jsonschema-form/issues/4031)

## @rjsf/utils

- Added `getDateElementProps()` to refactor duplicate function in `core`, `antd` & `chakra-ui` AltDateWidget's source code. The same function, implements the feature requested in [#297](https://github.com/rjsf-team/react-jsonschema-form/issues/297)

## Dev / docs / playground

- Updated docs and playground with the implementation guide of newly added date re-order feature.

# 5.15.1

## @rjsf/core

- fix `getFieldNames`. Now correctly defines an array of primitives.

## @rjsf/validator-ajv6

- Updated the `AJV6Validator` class to expose the internal `ajv` object, allowing access to support a fix related to [#3972](https://github.com/rjsf-team/react-jsonschema-form/issues/3972)

## @rjsf/validator-ajv8

- Updated the `AJV8Validator` class to expose the internal `ajv` object, allowing access to support a fix related to [#3972](https://github.com/rjsf-team/react-jsonschema-form/issues/3972)

## Dev / docs / playground

- Updated the documentation to describe how to use the newly exposed `ajv` variable

# 5.15.0

## @rjsf/mui

- fix gap in text and select widget outlines when `"ui:label": false` is specified.

## @rjsf/utils

- Updated `resolveAllReferences()` to use own recurse list for each object properties, fixing [#3961](https://github.com/rjsf-team/react-jsonschema-form/issues/3961)
- Added an experimental flag `allOf` to `experimental_defaultFormStateBehavior` for populating defaults when using `allOf` schemas [#3969](https://github.com/rjsf-team/react-jsonschema-form/pull/3969)

## Dev / playground

- add missing typescript project reference for `utils` in `validator-ajv6` and `validator-ajv8` packages tsconfigs
- Added a dropdown for changing the `experimental_defaultFormStateBehavior.allOf` behaviour in the playground

# 5.14.3

## @rjsf/core

- add `retrieveSchema` at `Form` state to memoize the result of `schemUtils.retrieveSchema`

## @rjsf/fluentui-rc

- Updated README.md references
- Fixed width of `ArrayFieldItemTemplate` items

## Dev

- update tsconfigs:
  - `"importHelpers": false` to remove need for tslib dependency [#3958](https://github.com/rjsf-team/react-jsonschema-form/issues/3958)
  - increase compilation target level from es6 to es2018 (so there are no need for transpiling object spread/rest feature)
  - add missing typescript project reference for `snapshot-tests` in a root tsconfig, update it to also use es modules

# 5.14.2

## @rjsf/antd

- Fixed the `peerDependencies` for `@ant-design/icons` to also support v5, fixing [#3507](https://github.com/rjsf-team/react-jsonschema-form/issues/3507)

## @rjsf/core

- avoid call `retrieveSchema` twice during `getStateFromProps` and `mustValidate` is true [#3959](https://github.com/rjsf-team/react-jsonschema-form/pull/3959)

## @rjsf/mui

- Resolve the React error caused by the propagation of the `hideError` property to the DOM element, fixing [#3945](https://github.com/rjsf-team/react-jsonschema-form/issues/3945)

## @rjsf/material-ui

- Resolve the React error caused by the propagation of the `hideError` property to the DOM element, fixing [#3945](https://github.com/rjsf-team/react-jsonschema-form/issues/3945)

## @rjsf/utils

- Update `sanitizeDataForNewSchema()` to avoid spreading strings and Arrays into the returned value when the old schema is of type `string` or `array` and the new schema is of type `object`. Fixing [#3922](https://github.com/rjsf-team/react-jsonschema-form/issues/3922)

# 5.14.1

## @rjsf/utils

- Update `sanitizeDataForNewSchema()` to avoid spreading strings and Arrays into the returned value when the old schema is of type `string` or `array` and the new schema is of type `object`. Fixing [#3922](https://github.com/rjsf-team/react-jsonschema-form/issues/3922)
- update types for `labelValue` to have more granular return types, fixing [#3946](https://github.com/rjsf-team/react-jsonschema-form/issues/3946)

## Dev / playground

- Added Fluent UI v9 (React Components) theme to playground
- Update Fluent UI v9 and playground project references
- Update eslint ignores to exclude new typescript build output folders

# 5.14.0

## @rjsf/fluentui-rc

- Added theme for Fluent UI v9 (React Components), fixing [#3659](https://github.com/rjsf-team/react-jsonschema-form/issues/3659)

## @rjsf/snapshot-tests

Move theme snapshot tests into separate package

## Dev / playground

- update configuration to use typescript project references, start type checking the tests

# 5.13.6

## @rjsf/core

- Updated `StringField` to pass `hideError` prop to `Widget` so that all fields are consistent. Missed this file in previous patch

# 5.13.5

## @rjsf/core

- Updated `StringField` and `BooleanField` to pass `hideError` prop to `Widget` so that all fields are consistent

# 5.13.4

## @rjsf/core

- Updated `SchemaField` to show errors for `anyOf`/`oneOf` when being rendered as select control, fixing [3908](https://github.com/rjsf-team/react-jsonschema-form/issues/3908)

# 5.13.3

## @rjsf/antd

- Fixed the `SelectWidget` so that filtering works by reworking how `options` are passed to the underlying `Select`

## @rjsf/core

- Replaced the deprecated `UNSAFE_componentWillReceiveProps()` method in the Form.tsx component with an improved solution utilizing the React lifecycle methods: `getSnapshotBeforeUpdate()` and `componentDidUpdate()`. Fixing [#1794](https://github.com/rjsf-team/react-jsonschema-form/issues/1794)
- Fixed the `ArrayField` implementation to never pass an undefined schema for fixed arrays to other methods, fixing [#3924](https://github.com/rjsf-team/react-jsonschema-form/issues/3924)
- Fixed a refresh issue in `getSnapshotBeforeUpdate()` caused by the fix for #1794, fixing [#3927](https://github.com/rjsf-team/react-jsonschema-form/issues/3927)

## @rjsf/utils

- Updated `toPathSchemaInternal()` util to generate correct path schemas for fixed arrays by picking up individual schemas in the `items` array, fixing [#3909](https://github.com/rjsf-team/react-jsonschema-form/issues/3909)

# 5.13.2

## @rjsf/utils

- Updated `resolveAnyOrOneOfSchemas()` to not take a `recurseList` anymore, and instead always pass an empty array down to `resolveAllReferences()`, fixing [#3902](https://github.com/rjsf-team/react-jsonschema-form/issues/3902)
  - Also updated `parseSchema()` and `resolveDependencies()` to no longer pass `recurseList` to `resolveAnyOrOneOfSchemas()`

## @rjsf/validator-ajv8

- Updated `AJV8PrecompiledValidator` to add a new `ensureSameRootSchema()` function that is called in both `rawValidation()` and `isValid()`
  - This function adds an optimization to avoid resolving the root schema unless necessary

# 5.13.1

## @rjsf/core

- Updated `ArrayField` to move errors in the errorSchema when the position of array items changes for the insert and copy cases.

## @rjsf/material-ui

- Removed an unnecessary `Grid` container component in the `ArrayFieldTemplate` component that wrapped the `ArrayFieldItemTemplate`, fixing [#3863](https://github.com/rjsf-team/react-jsonschema-form/issues/3863)
- Fixed an issue where `SelectWidget` switches from controlled to uncontrolled when `enumOptions` does not include a value, fixing [#3844](https://github.com/rjsf-team/react-jsonschema-form/issues/3844)

## @rjsf/mui

- Removed an unnecessary `Grid` container component in the `ArrayFieldTemplate` component that wrapped the `ArrayFieldItemTemplate`, fixing [#3863](https://github.com/rjsf-team/react-jsonschema-form/issues/3863)
- Fixed an issue where `SelectWidget` switches from controlled to uncontrolled when `enumOptions` does not include a value, fixing [#3844](https://github.com/rjsf-team/react-jsonschema-form/issues/3844)

## @rjsf/utils

- Added `getOptionMatchingSimpleDiscriminator()` function
- `getMatchingOption` and `getClosestMatchingOption` now bypass `validator.isValid()` calls when simple discriminator is provided, fixing [#3692](https://github.com/rjsf-team/react-jsonschema-form/issues/3692)
- Fix data type in `FieldTemplateProps['onChange']`
- Updated `retrieveSchema()` to properly resolve references inside of `properties` and array `items` while also dealing with recursive `$ref`s, fixing [#3761](https://github.com/rjsf-team/react-jsonschema-form/issues/3761)
  - Updated `schemaParser()` and `getClosestMatchingOption()` to pass the new `recursiveRef` parameter added to internal `retrieveSchema()` APIs
- Added/updated all the necessary tests to restore the `100%` test coverage that was lost when updating to Jest 29
  - Updated `getDefaultFormState()` to remove an unnecessary check for `formData` being an object since it is always guaranteed to be one, thereby allowing full testing coverage
- Updated `getSchemaType()` to return the first schema `type` when it is an array not containing `'null'`, fixing [#3875](https://github.com/rjsf-team/react-jsonschema-form/issues/3875)

## @rjsf/validator-ajv8

- Updated the `validator` and `precompiledValidator` tests to the restore `100%` coverage that was lost when updating to Jest 29
  - Updated `isValid()` for the `validator` commenting out an if condition that was preventing `100%` coverage, with a TODO to fix it later

## Dev / docs / playground

- Added the `@types/jest` as a global `devDependency` so that developer tools properly recognize the jest function types

# 5.13.0

## @rjsf/antd

- Bump Antd version from v4 to v5.
- Intentionally kept peer dependencies to v4 so that this change doesn't make breaking change for @rfjs/antd users.
- However, if users of @rjsf/antd want to use v5 styling, they need to wrap your application with the `StyleProvider` from `@ant-design/cssinjs`. They need not have to install this package, its a transitive package coming from antd.

```tsx
import { StyleProvider } from '@ant-design/cssinjs';

const Component = () => {
  return (
    <StyleProvider>
      <YourFormComponents />
    </StyleProvider>
  );
};
```

## @rjsf/core

- Updated `MultiSchemaField` to only merge top level required field fixing duplicate field and description.
- Fixed programmatic validation (`validateForm()`) removes previous errors if all data is now valid.

## @rjsf/chakra-ui

- Fixed a faulty check of the `isMultiple` option in `MultiSchemaField`. It no longer offers multiple choice inside a select field in a `oneOf` case in Chakra UI, fixing [#3848](https://github.com/rjsf-team/react-jsonschema-form/issues/3848)

## Dev / docs / playground

- Fixed custom validation playground example ([#3856](https://github.com/rjsf-team/react-jsonschema-form/issues/3856))

# 5.12.1

## @rjsf/validator-ajv8

- Updated `AJV8PrecompiledValidator.rawValidation()` to resolve root schema with formData when comparing input schema, fixing [#3825](https://github.com/rjsf-team/react-jsonschema-form/issues/3825)

## @rjsf/core

- Updated `MultiSchemaField` to merge all top level fields except properties for anyOf/oneOf options, fixing [#3808](https://github.com/rjsf-team/react-jsonschema-form/issues/3808) and [#3787](https://github.com/rjsf-team/react-jsonschema-form/issues/3787)

## @rjsf/antd

- Updated CheckboxesWidget to not show duplicate title, fixing [#3815](https://github.com/rjsf-team/react-jsonschema-form/issues/3815)

## @rjsf/utils

- Updated `retrieveSchemaInternal` allOf logic for precompiled schemas to resolve top level properties fixing [#3817](https://github.com/rjsf-team/react-jsonschema-form/issues/3817)

# 5.12.0

## @rjsf/utils

- Experimental feature:
  - Added `experimental_defaultFormStateBehavior = { arrayMinItems: { populate: 'never' } }` (feature [#3796](https://github.com/rjsf-team/react-jsonschema-form/issues/3796))

## @rjsf/validator-ajv8

- Exposing new function `compileSchemaValidatorsCode` to allow creating precompiled validator without a file. This is useful in case when precompiled validator is to be created dynamically. [#3793](https://github.com/rjsf-team/react-jsonschema-form/pull/3793)

## Dev / docs / playground

- update playground vite config to use sources directly, allowing to reload changes in it without additional build step
- moving from `dts-cli` to use individual dev tools directly, updating package publish config
  - tsc for generating type definitions and esm modules
  - esbuild for CJS bundle
  - rollup for UMD bundle
- Updated the `form-props` documentation `arrayMinItems`, added description for `never`.
- Updated the `playground` to add the option for the new `arrayMinItems.populate = 'never'`.

# 5.11.2

## @rjsf/material-ui

- Removed unnecessary import of old `@types/material-ui` which can cause typescript issues in some situations

## @rjsf/utils

- Updated the `resolveAllReferences()` function to use object spreading to update properties and items in a schema rather than directly modifying the schema to avoid issues with frozen object, fixing [#3805](https://github.com/rjsf-team/react-jsonschema-form/issues/3805)

# 5.11.1

## @rjsf/core

- Updated `SchemaField` to ignore errors for `anyOf`/`oneOf` parent schema, fixing [1295](https://github.com/rjsf-team/react-jsonschema-form/issues/1295)

## @rjsf/utils

- Created new `resolveAllReferences()` function to resolve all references within a schema's properties and array items.
- Updated `getClosestMatchingOption()` to use `resolveAllReferences()` for all oneOf/anyOf schemas
- Updated `resolveAnyOrOneOfSchemas()` to use `resolveAllReferences()` for all oneOf/anyOf schemas
- Better handle the `null` case in `withIdRefPrefix`, fixing [#3792](https://github.com/rjsf-team/react-jsonschema-form/pull/3792)

# 5.11.0

## @rjsf/core

- Updated `MultiSchemaField` to use `mergeSchema()` for merging in the remaining schema for `anyOf`/`oneOf`
- Added new `extraErrorsBlockSubmit` prop to `Form` that allows the extra asynchronous errors to block a form submit, fixing [#3757](https://github.com/rjsf-team/react-jsonschema-form/issues/3757)

## @rjsf/utils

- Updated `retrieveSchemaInternal()` to always resolve allOf schema without merging when `expandAllBranches` is set, fixing compiled schema issue always throwing error with `mergeAllOf`
- Updated `getDefaultFormState()` to use `mergeSchema()` for merging in the remaining schema for `anyOf`/`oneOf`
- Updated `retrieveSchema()` to use `mergeSchema()` for merging in the remaining schema for `anyOf`/`oneOf`

## Dev / docs / playground

- Switched to using npm workspaces for the sub-package hierarchy
  - NOTE: Developers may need to run the `npm run refresh-node-modules` script first to get the build and tests to work correctly
- Backfilled Docusaurus site with documentation for v3, v4

# 5.10.0

## @rjsf/core

- Updated `getFieldComponent()` to support rendering a custom component by given schema id ($id). [#3740](https://github.com/rjsf-team/react-jsonschema-form/pull/3740)
- Updated `MultiSchemaField` to merge the selected `oneOf/anyOf` value into base `schema`, fixing [#3744](https://github.com/rjsf-team/react-jsonschema-form/issues/3744)

## @rjsf/utils

- Updated `getClosestMatchingOption()` to resolve refs in options before computing the closest matching option, fixing an issue with using precompiled validators
  - Also, added support for nested `anyOf` and `discriminator` support in the recursive `calculateIndexScore()`
- Updated `getDefaultFormState()` to merge the remaining schema into `anyOf/oneOf` schema selected during the computation of values, fixing [#3744](https://github.com/rjsf-team/react-jsonschema-form/issues/3744)
- Updated `retrieveSchema()` to merge the remaining schema into the `anyOf/oneOf` schema selected during the resolving of dependencies, fixing [#3744](https://github.com/rjsf-team/react-jsonschema-form/issues/3744)

## Dev / docs / playground

- Updated the `custom-widgets-fields` documentation to add the new added behaviour of `getFieldComponent()` function. [#3740](https://github.com/rjsf-team/react-jsonschema-form/pull/3740)
- Updated the `playground` to add an example of the new added behaviour of `getFieldComponent()` function. [#3740](https://github.com/rjsf-team/react-jsonschema-form/pull/3740)

# 5.9.0

## @rjsf/utils

- Updated `getDefaultFormState()` to fix a bug where `experimental_defaultFormStateBehavior: { emptyObjectFields: 'populateRequiredDefaults' }` wasn't working for object properties with `$ref`s
- Experimental feature **breaking change**:
  - Updated the `experimental_defaultFormStateBehavior.arrayMinItems` from simple flag to an object containing two optional fields, `populate` and `mergeExtraDefaults`
    - The new `arrayMinItems.mergeExtraDefaults` flag, when "true", allows users to merge defaults onto the end of `formData` arrays when `minItems` is specified
  - If you were previously passing `experimental_defaultFormStateBehavior` as `{ arrayMinItems = 'requiredOnly }` on the `Form`, now you would pass `{ arrayMinItems: { populate: 'requiredOnly' } }`
- Added a new, optional `mergeExtraArrayDefaults=false` flag to the `mergeDefaultWithFormData()` utility function to support the new `arrayMinItems.mergeExtraDefaults` experimental feature

## Dev / docs / playground

- Updated the `utility-functions` documentation to add the new `mergeExtraArrayDefaults` flag for the `mergeDefaultWithFormData()` function
- Updated the `form-props` documentation to update the `arrayMinItems` documentation for the new object behavior
- Updated the `playground` to add a checkbox for the new `arrayMinItems.mergeExtraDefaults` flag

# 5.8.2

## @rjsf/validator-ajv8

- Explicitly cache schemas by their hash when checking data is valid to avoid multiple compilations for schemas without IDs leading to poor performance [#3721](https://github.com/rjsf-team/react-jsonschema-form/pull/3721)

# 5.8.1

## Dev / docs / playground

- Updated peer dependencies in all packages to `^5.8.x`

# 5.8.0

## @rjsf/bootstrap-4

- Updated FieldTemplate Component to display description from SchemaField and make it consistent for all the available themes

## @rjsf/chakra-ui

- Updated FieldTemplate Component to display description from SchemaField and make it consistent for all the available themes

## @rjsf/core

- Updated SchemaField to be able to render markdown in the description field
- Updated `MultiSchemaField.getMatchingOption` to use option index from `getClosestMatchingOption`, fixing [#3693](https://github.com/rjsf-team/react-jsonschema-form/issues/3693) and
  [#3705](https://github.com/rjsf-team/react-jsonschema-form/issues/3705)

## @rjsf/fluent-ui

- Updated FieldTemplate Component to display description from SchemaField and make it consistent for all the available themes

## @rjsf/material-ui

- Updated FieldTemplate Component to display description from SchemaField and make it consistent for all the available themes

## @rjsf/mui

- Updated FieldTemplate Component to display description from SchemaField and make it consistent for all the available themes

## @rjsf/semantic-ui

- Updated FieldTemplate Component to display description from SchemaField and make it consistent for all the available themes

## @rjsf/utils

- Updated `getClosestMatchingOption` to return selected option if all options score the same, fixing [#3693](https://github.com/rjsf-team/react-jsonschema-form/issues/3693) and [#3705](https://github.com/rjsf-team/react-jsonschema-form/issues/3705)
- Updated `resolveCondition` to default formData as empty object when evaluating if expression, fixing [#3706](https://github.com/rjsf-team/react-jsonschema-form/issues/3706)
- Updated `retrieveSchemaInternal` to return failed merged allOf sub schemas for expandAllBranches flag, fixing [#3689](https://github.com/rjsf-team/react-jsonschema-form/issues/3700)
- Updated `hashForSchema` to sort schema fields in consistent order before stringify to prevent different hash ids for the same schema
- Updated `enumOptionsSelectValue` to allow picking falsy enumOptions, fixing [#3716](https://github.com/rjsf-team/react-jsonschema-form/issues/3716)

## @rjsf/validator-ajv8

- Updated `AJV8PrecompiledValidator.rawValidation()` to use resolve root schema when comparing input schema, fixing [#3708](https://github.com/rjsf-team/react-jsonschema-form/issues/3708)

## Dev / docs / playground

- Updated sample data and documentation about the markdown in `RJSFSchema` description
- Fixed broken playground examples ([#3696](https://github.com/rjsf-team/react-jsonschema-form/issues/3696))
- Added experimental_defaultFormStateBehavior.emptyObjectFields control to Playground
- Fixed bug where subthemes would not appear in Playground

# 5.7.3

## @rjsf/utils

- Updated `getClosestMatchingOption` `JUNK_OPTION` schema with a well known $id
- Updated `schemaParser` to resolve array items field, fixing [#3689](https://github.com/rjsf-team/react-jsonschema-form/issues/3689)

## @rjsf/validator-ajv8

- Updated `AJV8PrecompiledValidator.isValid()` to return false for junk schema option, fixing [#3677](https://github.com/rjsf-team/react-jsonschema-form/issues/3677)

# 5.7.2

## @rjsf/validator-ajv8

- Removed the importing of internal `ajv` types by simplifying the `CompiledValidateFunction` type to avoid a bunch of Typescript errors encountered by users of the package

# 5.7.1

## @rjsf/validator-ajv8

- Updated the build for all but the `cjs` development version, to not export the `compileSchemaValidators()` function to avoid "Module not found: Can't resolve 'fs' error" issues, fixing [#3668](https://github.com/rjsf-team/react-jsonschema-form/issues/3668)

## @rjsf/core

- Added protection against a null `field` in the `focusOnError` method in `Form`

## Dev / docs / playground

- Updated the `validation` documentation to add a note with a web-resource to help folks work around the "Module not found: Can't resolve 'fs' error" issue for development environments
- Updated all of the `package-lock.json` files to bump peer-dependencies to `5.7.x`, fixing [#3669](https://github.com/rjsf-team/react-jsonschema-form/issues/3669)

# 5.7.0

## @rjsf/antd

- Fix [#3608](https://github.com/rjsf-team/react-jsonschema-form/issues/3608) by ensuring the root field is always wrapped in Form.Item
- Fix [#3594](https://github.com/rjsf-team/react-jsonschema-form/issues/3594) by removing the duplicate title for `SelectWidget` and description for `CheckboxWidget`

## @rjsf/core

- Updated the `MultiSchemaField` to use the new `getDiscriminatorFieldFromSchema()` API
- Added new `experimental_defaultFormStateBehavior` prop to `Form`
  - to specify alternate behavior when dealing with the rendering of array fields where `minItems` is set but field is not `required` (fixes [#3363](https://github.com/rjsf-team/react-jsonschema-form/issues/3363)) ([#3602](https://github.com/rjsf-team/react-jsonschema-form/issues/3602))
  - to handle setting object defaults based on the value of `emptyObjectFields` supporting required fields only and skipping defaults entirely, fixing [#2980](https://github.com/rjsf-team/react-jsonschema-form/issues/2980)
- Fixed regression [#3650](https://github.com/rjsf-team/react-jsonschema-form/issues/3650) in `FileWidget` to again support adding multiple files to arrays

## @rjsf/fluent-ui

- Added support for `additionalProperties` to fluent-ui theme, fixing [#2777](https://github.com/rjsf-team/react-jsonschema-form/issues/2777).
- Upgraded to `8.x` version of `@fluentui/react` maintaining backwards compatibility to version 7, fixing [#3463](https://github.com/rjsf-team/react-jsonschema-form/issues/3463)

## @rjsf/utils

- Added two new APIs `getDiscriminatorFieldFromSchema()` (a refactor of code from `MultiSchemaField`) and `hashForSchema()`
  - Updated `getDefaultFormState()` and `toPathSchema()` to use `getDiscriminatorFieldFromSchema()` to provide a discriminator field to `getClosestMatchingOption()` calls.
- Refactored the `retrieveSchema()` internal API functions to support implementing an internal `schemaParser()` API for use in precompiling schemas, in support of [#3543](https://github.com/rjsf-team/react-jsonschema-form/issues/3543)
- Fixed `toPathSchema()` to handle `properties` in an object along with `anyOf`/`oneOf`, fixing [#3628](https://github.com/rjsf-team/react-jsonschema-form/issues/3628) and [#1628](https://github.com/rjsf-team/react-jsonschema-form/issues/1628)
- Refactored optional parameters for `computeDefaults()` into destructured props object to reduce clutter when only specifying later of the optional argument, fixing [#3602](https://github.com/rjsf-team/react-jsonschema-form/issues/3602)
- Fixed `computeDefaults()` to handle `$ref` in an object along with `anyOf`/`oneOf`, fixing [#3633](https://github.com/rjsf-team/react-jsonschema-form/issues/3633)

## @rjsf/validator-ajv8

- Added two new APIs `compileSchemaValidators()` and `createPrecompiledValidator()` implemented to support using precompiled validators build with AJV 8, fixing [#3543](https://github.com/rjsf-team/react-jsonschema-form/issues/3543)

## Dev / docs / playground

- Added documentation to `custom-templates` describing how to extend the `BaseInputTemplate`
- Added **minItems behavior for array field** live setting, fixing [#3602](https://github.com/rjsf-team/react-jsonschema-form/issues/3602)
- Upgraded playground to `8.x` version of `@fluentui/react`, fixing [#3463](https://github.com/rjsf-team/react-jsonschema-form/issues/3463)
- Added documentation to `validation` describing the new precompiled validators feature
- Added new `validator-ajv8.md` documentation to the `api-reference` directory as well as putting it into the `sidebar.js`

# 5.6.2

## Dev / docs / playground

- Fixed issues with `post-versioning` that caused the 5.6.1 branch to not be publishable

# 5.6.1

## Dev / docs / playground

- Updated the `contributing` documentation to improve the `Releasing` section to include a new `npm run post-versioning` step
  - Implemented a new `bump-peer-deps.js` script to help implement the new scripts included in the `post-versioning` step

# 5.6.0

## @rjsf/antd

- Treat multiple as a boolean rather than comparing against `undefined` in the `SelectWidget`, fixing [#3595](https://github.com/rjsf-team/react-jsonschema-form/issues/3595)

## @rjsf/core

- Switched `Form` to use the new `validatorDataMerge()` and `toErrorList()` functions instead of the now deprecated `schemaUtils.mergeValidatorData()` and `schemaUtils.getValidator().toErrorList()`
- Added option to provide a callback function to `focusOnFirstError` ([3590](https://github.com/rjsf-team/react-jsonschema-form/pull/3590))
- Updated `MultiSchemaField` to handle the OpenAPI `discriminator` extension on `anyOf/oneOf` fields by passing it into `getClosestMatchingOption()` if it exists, fixing [#3512](https://github.com/rjsf-team/react-jsonschema-form/issues/3512)
- Updated `SchemaField` function to use `getSchemaType` rather than `schema.type` to set the proper class name.

## @rjsf/utils

- Refactored the `createErrorHandler()`, `toErrorList()`, `toErrorSchema()` and `unwrapErrorHandler()` functions from the `@rjsf/validator-ajv6` and `@rjsf/validator-ajv8` implementations since they were identical
  - As a result, the `mergeValidationData()` function was deprecated in favor of the new `validationDataMerge()` function that uses the refactored `toErrorList()` function
  - Refactored the `ROOT_SCHEMA_PREFIX` constant as well
- Updated `ValidatorType` and `SchemaUtilsType` to deprecate the `toErrorList()` and `mergeValidationData()` functions, respectively
- Updated the `getClosestMatchingOption()` and `getFirstMatchingOption()` to pass the new `discriminatorField` to the `getMatchingOption()` function
- Updated `getMatchingOption()` to use `discriminatorField` when it is present in the `options` object properties to drill into the object to detect if that one field is valid
- Updated `SchemaUtilsType` and the associated forward functions in `createSchemaUtils` to add the new `discriminatorField?: string` optional parameter
- Updated `toIdSchema()` function to use `getSchemaType(schema) === 'object'` rather than `schema.type === 'object'` to get the proper pathing for ids, fixing [#2044](https://github.com/rjsf-team/react-jsonschema-form/issues/2044)

## @rjsf/validator-ajv6

- Removed the refactored functions and constant from the `AJV6Validator` in favor of using the new functions and constant from `@rjsf/utils`

## @rjsf/validator-ajv8

- Removed the refactored functions and constant from the `AJV8Validator` in favor of using the new functions and constant from `@rjsf/utils`

## Dev / docs / playground

- Updated the `utility-functions` documentation to describe the new refactored functions as well as deprecating the `mergeValidationData()` function
- Updated the `playground` to properly restore `liveSettings` from shared links and added a switch for `noHtml5Validation` in the live settings rather than having it set to `true` always
  - Also added a new `Blank` example to help users easily paste their code

# 5.5.2

## @rjsf/material-ui

- Switched to using `TextField` for the `WrapIfAdditionalTemplate` label key input to match the `@rjsf/mui` fix

## @rjsf/mui

- Switched to using `TextField` for the `WrapIfAdditionalTemplate` label key input, fixing [#3578](https://github.com/rjsf-team/react-jsonschema-form/issues/3578)

## Dev / docs / playground

- Updated the `templates` passed into the main `Form` to not include undefined values, fixing [#3576](https://github.com/rjsf-team/react-jsonschema-form/issues/3576) and [#3579](https://github.com/rjsf-team/react-jsonschema-form/issues/3579)

# 5.5.1

## @rjsf/core

- Updated `Form` to include the top `disabled` property in the `ui:submitButtonOptions` so the submit button will be disabled when the whole form is disabled. Fixes [#3264](https://github.com/rjsf-team/react-jsonschema-form/issues/3264).

## @rjsf/utils

- Added protections against infinite recursion of `$ref`s for the `toIdSchema()`, `toPathSchema()` and `getDefaultFormState()` functions, fixing [#3560](https://github.com/rjsf-team/react-jsonschema-form/issues/3560)
- Updated `getDefaultFormState()` to handle object-based `additionalProperties` with defaults using `formData` in addition to values contained in a `default` object, fixing [#2593](https://github.com/rjsf-team/react-jsonschema-form/issues/2593)
- Updated internal helper `withExactlyOneSubschema()` inside of `retrieveSchema()` to use the `isValid()` function rather than `validateFormData()` when determining the one-of branch

## Dev / docs / playground

- Refactored some parts of `playground` to make it cleaner
  - This includes fixing the spelling of the `disabled` flag being passed into the `Form` from the incorrect `disable` spelling
- Formatted the entire monorepo which included 6 unformatted files outside of `playground`
- Removed `react-app-polyfill` package from `playgound`. This ends IE11 support
- Fix a handful of broken docs links, fixing [#3553](https://github.com/rjsf-team/react-jsonschema-form/issues/3553)

# 5.5.0

## @rjsf/antd

- Updated tests to use centralized snapshots from `core`

## @rjsf/bootstrap-4

- Updated tests to use centralized snapshots from `core`

## @rjsf/chakra-ui

- Updated tests to use centralized snapshots from `core`

## @rjsf/core

- Updated `FileWidget` to pass false for `required` once a value has been specified, fixing [#3504](https://github.com/rjsf-team/react-jsonschema-form/issues/3504)
- Updated `ObjectField` to pass the `errorSchema` to the `ObjectFieldTemplate` to allow custom templates access to the errors
- Centralized snapshot tests from each theme into `core`, adding snapshots tests for `core` as well

## @rjsf/fluent-ui

- Updated tests to use centralized snapshots from `core`

## @rjsf/material-ui

- Updated tests to use centralized snapshots from `core`

## @rjsf/mui

- Updated tests to use centralized snapshots from `core`

## @rjsf/semantic-ui

- Updated tests to use centralized snapshots from `core`

## @rjsf/utils

- Added `errorSchema` as an optional prop on `ObjectFieldTemplateProps`

## Dev / docs / playground

- Converted the `playground` to use Typescript, including some refactoring of code to make that job easier
- Updated the `custom-templates` documentation to add `errorSchema` to the props for `ObjectFieldTemplate`

# 5.4.0

## @rjsf/antd

- Added the ability to use a tooltip for a description
- Updated `ObjectFieldTemplate` to hide the titles and descriptions when `displayLabel` is true (including globally), fixing [#3231](https://github.com/rjsf-team/react-jsonschema-form/issues/3231)
- Updated `CheckboxWidget` to show the `description` using the `DescriptionFieldTemplate`, fixing [#2791](https://github.com/rjsf-team/react-jsonschema-form/issues/2791)
- Updated `CheckboxesWidget` and `SelectWidget` to show the `label` using the `TitleFieldTemplate`, fixing [#2134](https://github.com/rjsf-team/react-jsonschema-form/issues/2134)

## @rjsf/bootstrap-4

- Updated `ObjectFieldTemplate` to hide the titles and descriptions when `displayLabel` is true (including globally), fixing [#3231](https://github.com/rjsf-team/react-jsonschema-form/issues/3231)
- Updated `CheckboxWidget` to show the `description` using the `DescriptionFieldTemplate`, fixing [#2791](https://github.com/rjsf-team/react-jsonschema-form/issues/2791)
- Updated `RangeWidget` to fix the label hiding bug using `labelValue()`

## @rjsf/chakra-ui

- Fix: MUI radio widget initializes as uncontrolled when schema has no default value, fixing [#3511](https://github.com/rjsf-team/react-jsonschema-form/issues/3511)
- Updated `ObjectFieldTemplate` to hide the titles and descriptions when `displayLabel` is true (including globally), fixing [#3231](https://github.com/rjsf-team/react-jsonschema-form/issues/3231)
- Updated `CheckboxesWidget`, `CheckboxWidget`, `RadioWidget` and `SelectWidget` to hide labels when `hideLabel` is true using the new `labelValue()` helper (including globally)
- Updated `CheckboxWidget` to show the `description` using the `DescriptionFieldTemplate`, fixing [#2791](https://github.com/rjsf-team/react-jsonschema-form/issues/2791)

## @rjsf/core

- Updated `FileWidget` to show a preview of images and a download link for non-images when the `filePreview` options is set to true in the `UiSchema`
- Updated `ArrayField`, `BooleanField`, `MultiSelectField` and `StringField` to pass `label` (read from `uiSchema.title` || `schema.title` || `name`) and `hideLabel` down to all of the `Widgets` they render, fixing [#827](https://github.com/rjsf-team/react-jsonschema-form/issues/827), [#2636](https://github.com/rjsf-team/react-jsonschema-form/issues/2636), [#2399](https://github.com/rjsf-team/react-jsonschema-form/issues/2399) and [#3531](https://github.com/rjsf-team/react-jsonschema-form/issues/3531)
- Updated `ObjectField`, `ObjectFieldTemplate`, `ArrayFieldDescriptionTemplate`, `ArrayFieldTitleTemplate` and `CheckboxWidget` to hide the titles and descriptions when `hideLabel` is true using the new `labelValue()` helper (including globally), fixing [#3231](https://github.com/rjsf-team/react-jsonschema-form/issues/3231)
- Updated `CheckboxWidget` to use the `labelValue()` function for hiding labels

## @rjsf/fluent-ui

- Updated `FieldTemplate` and `ObjectFieldTemplate` to hide the titles and descriptions when `displayLabel` is true (including globally), fixing [#3231](https://github.com/rjsf-team/react-jsonschema-form/issues/3231)
- Updated `BaseInputTemplate`, `CheckboxesWidget`, `CheckboxWidget`, `ColorWidget`, `DateWidget`, `RadioWidget`, `RangeWidget`, `SelectWidget` and `UpDownWidget` to hide labels when `hideLabel` is true using the new `labelValue()` helper (including globally)
  - Also extracted a new `FluentLabel` component out of `CheckboxesWidget`, `ColorWidget`, `RangeWidget` and `UpDownWidget`
- Updated `CheckboxWidget` to show the `description` using the `DescriptionFieldTemplate`, fixing [#2791](https://github.com/rjsf-team/react-jsonschema-form/issues/2791)

## @rjsf/material-ui

- Fix: MUI radio widget initializes as uncontrolled when schema has no default value, fixing [#3511](https://github.com/rjsf-team/react-jsonschema-form/issues/3511)
- Updated `ObjectFieldTemplate` to hide the titles and descriptions when `displayLabel` is true (including globally), fixing [#3231](https://github.com/rjsf-team/react-jsonschema-form/issues/3231)
- Updated `BaseInputTemplate`, `CheckboxesWidget`, `CheckboxWidget`, `RadioWidget`, `RangeWidget` and `SelectWidget` to hide labels when `hideLabel` is true using the new `labelValue()` helper (including globally)
- Updated `CheckboxWidget` to show the `description` using the `DescriptionFieldTemplate`, fixing [#2791](https://github.com/rjsf-team/react-jsonschema-form/issues/2791)

## @rjsf/mui

- Fix: MUI radio widget initializes as uncontrolled when schema has no default value, fixing [#3511](https://github.com/rjsf-team/react-jsonschema-form/issues/3511)
- Updated `ObjectFieldTemplate` to hide the titles and descriptions when `displayLabel` is true (including globally), fixing [#3231](https://github.com/rjsf-team/react-jsonschema-form/issues/3231)
- Updated `BaseInputTemplate`, `CheckboxesWidget`, `CheckboxWidget`, `RadioWidget`, `RangeWidget` and `SelectWidget` to hide labels when `hideLabel` is true using the new `labelValue()` helper (including globally)
- Updated `CheckboxWidget` to show the `description` using the `DescriptionFieldTemplate`, fixing [#2791](https://github.com/rjsf-team/react-jsonschema-form/issues/2791)

## @rjsf/semantic-ui

-
- Updated `ObjectFieldTemplate` to hide the titles and descriptions when `displayLabel` is true (including globally), fixing [#3231](https://github.com/rjsf-team/react-jsonschema-form/issues/3231)
- Updated `BaseInputTemplate`, `CheckboxesWidget`, `CheckboxWidget`, `SelectWidget` and `TextareaWidget` to hide labels when `hideLabel` is true using the new `labelValue()` helper (including globally)
- Updated `CheckboxWidget` to show the `description` using the `DescriptionFieldTemplate`, fixing [#2791](https://github.com/rjsf-team/react-jsonschema-form/issues/2791)

## @rjsf/utils

- Updated the `UiSchema` to support the optional `filePreview?: boolean` option and to add a new `TranslatableString.PreviewLabel` to the `enums`
- Updated the `WidgetProps` to add an optional `hideLabel?: boolean` field to better support hiding labels
- Added a new `labelValue()` helper function to better support hiding labels

## @rjsf/validator-ajv8

- Improve `toErrorList()` and `unwrapErrorHandler()` by ensuring objects before recursing

## Dev / docs / playground

- Added a new `AntD Customization` documentation with references to it in the `form-props` and `uiSchema` documentation
- Updated the `uiSchema` documentation to add the `filePreview` option
- Updated the `widgets` documentation to add the new, optional `hideLabel` prop
- Updated the `utility-functions` documentation to add the new `labelValue()` function

# 5.3.1

## @rjsf/core

- Updated `AltDateWidget` to remove an infinite loop caused by two conflicting effects by merging them with additional checking of original `value` against the current value, fixing [#3516](https://github.com/rjsf-team/react-jsonschema-form/issues/3516)

## @rjsf/utils

- Updated the documentation of `getTestValidator()` and the `schema.test.ts` file to help developers

## @rjsf/validator-ajv6

- Updated the documentation of `getTestValidator()` and the `schema.test.ts` file to help developers

## @rjsf/validator-ajv8

- Updated the documentation of `getTestValidator()` and the `schema.test.ts` file to help developers

## Dev / docs / playground

- Updated the `internals` documentation to use a React ref in the example, fixing [#3520](https://github.com/rjsf-team/react-jsonschema-form/issues/3520)
- Updated the `contributing` documentation to describe the new development process needed for a `Vite` playground, fixing [#3478](https://github.com/rjsf-team/react-jsonschema-form/issues/3478)
  - Also fixed the `package.json` files to remove `npm start` in the subdirectories and change the root one to describe the new process
- Updated the `semantic-ui/uiSchema` documentation to switch the default for `horizontalButtons` to be true per changes made in `5.3.0`

# 5.3.0

## @rjsf/antd

- Added support to make a copy of an array item directly after the item selected to be copied (feature is off by default), fixing [#1261](https://github.com/rjsf-team/react-jsonschema-form/issues/1261) and [#1712](https://github.com/rjsf-team/react-jsonschema-form/issues/1712)
- Fixed `package.json` to properly add required dependencies explicitly which were installed implicitly

## @rjsf/bootstrap-4

- Added support to make a copy of an array item directly after the item selected to be copied (feature is off by default), fixing [#1261](https://github.com/rjsf-team/react-jsonschema-form/issues/1261) and [#1712](https://github.com/rjsf-team/react-jsonschema-form/issues/1712)

## @rjsf/chakra-ui

- Added support to make a copy of an array item directly after the item selected to be copied (feature is off by default), fixing [#1261](https://github.com/rjsf-team/react-jsonschema-form/issues/1261) and [#1712](https://github.com/rjsf-team/react-jsonschema-form/issues/1712)

## @rjsf/core

- `Reset` function added for `Programmatically Reset` action. `Reset` function will reset form data and validation errors. Form data will set to default values.
- Implemented a new `TimeWidget` that works for all themes
- Added support to make a copy of an array item directly after the item selected to be copied (feature is off by default), fixing [#1261](https://github.com/rjsf-team/react-jsonschema-form/issues/1261) and [#1712](https://github.com/rjsf-team/react-jsonschema-form/issues/1712)
- Also added the missing translation for the `InvalidObjectField` error in `ObjectField`
- Added support for the handling of the global UiSchema options in `Form`, `ArrayField`, `ObjectField` and `SchemaField`

## @rjsf/fluent-ui

- Fix `RadioWidget`'s onChange return value.
- Added support to make a copy of an array item directly after the item selected to be copied (feature is off by default), fixing [#1261](https://github.com/rjsf-team/react-jsonschema-form/issues/1261) and [#1712](https://github.com/rjsf-team/react-jsonschema-form/issues/1712)

## @rjsf/material-ui

- Updated `BaseInputTemplate` so that it shrinks a `time` formatted input
- Added support to make a copy of an array item directly after the item selected to be copied (feature is off by default), fixing [#1261](https://github.com/rjsf-team/react-jsonschema-form/issues/1261) and [#1712](https://github.com/rjsf-team/react-jsonschema-form/issues/1712)

## @rjsf/mui

- Updated `BaseInputTemplate` so that it shrinks a `time` formatted input
- Added support to make a copy of an array item directly after the item selected to be copied (feature is off by default), fixing [#1261](https://github.com/rjsf-team/react-jsonschema-form/issues/1261) and [#1712](https://github.com/rjsf-team/react-jsonschema-form/issues/1712)

## @rjsf/semantic-ui

- Added support to make a copy of an array item directly after the item selected to be copied (feature is off by default), fixing [#1261](https://github.com/rjsf-team/react-jsonschema-form/issues/1261) and [#1712](https://github.com/rjsf-team/react-jsonschema-form/issues/1712)

## @rjsf/utils

- Updated the widget matrix used by `getWidget()` to support the `time` to `TimeWidget` mapping
- Added a new `TranslatableString` enums `CopyButton` and `InvalidObjectField` that localizes the information extracted from `ObjectField` as markdown
- Updated the `ArrayFieldTemplateItemType` to add support for copying array items
- Refactored `UIOptionsBaseType` to extract the `addable`, `orderable`, `removable`, `label` and `duplicateKeySuffixSeparator` into a new `GlobalUISchemaOptions` type that adds `copyable`
  - Extended `UIOptionsBaseType` from `GlobalUISchemaOptions`
  - In `UiSchema` added a new optional `ui:globalOptions` prop of type `GlobalUISchemaOptions` and a new `UI_GLOBAL_OPTIONS_KEY` constant
  - Added a new optional prop `globalUiOptions` object of type `GlobalUISchemaOptions` in `Registry` as well as `CopyButton` in `ButtonTemplates`
- Updated `getUiOptions()` and `getDisplayLabel()` (and its `SchemaUtilsType` counterpart) to take an optional `GlobalUISchemaOptions` parameter that is used to include global options into the returned `uiOptions`

## Dev / docs / playground

- Updated the playground to add a `Programmatically Reset` button to clear states which are form data and validation errors.
- Updated the `Date & time` example to show off the new `TimeWidget`.
- Updated the `custom-widgets-fields` and `widgets` documentation to mention the new `TimeWidget` and its support for the `time` format.
- Updated the documentation for `custom-templates`, `internals`, `uiSchema`, `utility-functions` and `arrays` for the new copy array feature as well as the global UI Schema options support
- Updated the `arrays` example to add examples for the new `copyable` feature

# 5.2.1

## @rjsf/antd

- Updated `BaseInputTemplate` to favor the special `onChangeOverride` provided by the `core` `FileWidget`
- Removed explicit import of `React`, switching imports to explicit ones after fixing linting rules to not require `React` for JSX

## @rjsf/bootstrap-4

- Updated `BaseInputTemplate` to favor the special `onChangeOverride` provided by the `core` `FileWidget`, deleting the theme's `FileWidget`, fixing [#2095](https://github.com/rjsf-team/react-jsonschema-form/issues/2095)
- Removed explicit import of `React`, switching imports to explicit ones after fixing linting rules to not require `React` for JSX

## @rjsf/chakra-ui

- Updated `BaseInputTemplate` to favor the special `onChangeOverride` provided by the `core` `FileWidget`
- Removed explicit import of `React`, switching imports to explicit ones after fixing linting rules to not require `React` for JSX

## @rjsf/core

- Ensure that `name` is consistently passed to all `Widgets` through the field components, fixing [#1763](https://github.com/rjsf-team/react-jsonschema-form/issues/1763)
- Updated the `FileWidget` to render the input using the `BaseInputTemplate` passing a special `onChangeOverride` function to deal with the file events, fixing [#2095](https://github.com/rjsf-team/react-jsonschema-form/issues/2095)
- Removed explicit import of `React`, switching imports to explicit ones after fixing linting rules to not require `React` for JSX

## @rjsf/fluent-ui

- Updated `BaseInputTemplate` to favor the special `onChangeOverride` provided by the `core` `FileWidget`
- Removed explicit import of `React`, switching imports to explicit ones after fixing linting rules to not require `React` for JSX

## @rjsf/material-ui

- Updated `BaseInputTemplate` to favor the special `onChangeOverride` provided by the `core` `FileWidget` and to support automatically shrinking the label for the `date`, `datetime-local` and `file` types
  - Removed the `DateWidget` and `DateTimeWidget` since they were only created to provide the label shrinking property
- Removed explicit import of `React`, switching imports to explicit ones after fixing linting rules to not require `React` for JSX

## @rjsf/mui

- Updated `BaseInputTemplate` to favor the special `onChangeOverride` provided by the `core` `FileWidget` and to support automatically shrinking the label for the `date`, `datetime-local` and `file` types
  - Removed the `DateWidget` and `DateTimeWidget` since they were only created to provide the label shrinking property
- Removed explicit import of `React`, switching imports to explicit ones after fixing linting rules to not require `React` for JSX

## @rjsf/semantic-ui

- Updated `BaseInputTemplate` to favor the special `onChangeOverride` provided by the `core` `FileWidget`
- Removed explicit import of `React`, switching imports to explicit ones after fixing linting rules to not require `React` for JSX

## @rjsf/utils

- Added the `name` prop to the `WidgetProps` type, fixing [#1763](https://github.com/rjsf-team/react-jsonschema-form/issues/1763)
- Fixed `dataURItoBlob()` to handle the exception thrown by `atob()` when it is passed a malformed URL, returning an `blob` that indicates the error in the `type` prop
- Fixed `replaceStringParameters()` to improve the replaceable parameters logic so that it works properly when a parameter also contains a replaceable parameter identifier
- Removed explicit import of `React`, switching imports to explicit ones after fixing linting rules to not require `React` for JSX

## Dev / docs / playground

- Updated the `custom-widgets-fields` documentation to ensure the new `WidgetProps` `name` prop is documented
- Added Algolia DocSearch to the documentation site

# 5.2.0

## @rjsf/antd

- Updated `ErrorList`, `IconButton`s, `WrapIfAdditionalTemplate` and `AltDateWidget` to use the new `translateString()` function to support localization

## @rjsf/bootstrap-4

- Updated `AddButton`, `ErrorList`, `IconButton`s and `WrapIfAdditionalTemplate` to use the new `translateString()` function to support localization

## @rjsf/chakra-ui

- Updated `AddButton`, `ErrorList`, `IconButton`s, `WrapIfAdditionalTemplate` and `AltDateWidget` to use the new `translateString()` function to support localization

## @rjsf/core

- Updated `ArrayField`, `BooleanField`, `MultiSchemaField`, `ObjectField`, `SchemaField`, `AddButton`, `IconButton`s, `ErrorList`, `WrapIfAdditionalTemplate` and `AltDateWidget` and `FileWidget` to use the new `translateString()` function to support localization
  - Also updated `Form` to take a new optional `translateString` prop and `getDefaultRegistry()` to set `translateString` to `englishStringTranslator()`

## @rjsf/fluent-ui

- Updated `AddButton`, `ColorWidget`, `ErrorList`, `IconButton`s and `UpDownWidget` to use the new `translateString()` function to support localization

## @rjsf/material-ui

- Updated `AddButton`, `ErrorList`, `IconButton`s and `WrapIfAdditionalTemplate` to use the new `translateString()` function to support localization
- Patch `RangeWidget` to support `0` as range slider value, fixing [#3458](https://github.com/rjsf-team/react-jsonschema-form/issues/3458)

## @rjsf/mui

- Updated `AddButton`, `ErrorList`, `IconButton`s and `WrapIfAdditionalTemplate` to use the new `translateString()` function to support localization
- Patch `RangeWidget` to support `0` as range slider value, fixing [#3458](https://github.com/rjsf-team/react-jsonschema-form/issues/3458)

## @rjsf/semantic-ui

- Updated `AddButton`, `ErrorList`, `IconButton`s and `WrapIfAdditionalTemplate` to use the new `translateString()` function to support localization

## Dev / docs / playground

- Updated the `utility-functions` documentation for the `enums` and `englishStringTranslator()` & `replaceStringParameters()` functions
- Updated the `form-props` documentation for the new, optional `translateString` prop on `Form`
- Updated the playground's `numbers` example to use a range slider with a valid negative and `0` value

# 5.1.0

## @rjsf/bootstrap-4

- Updated the `AltDateTimeWidget` in `@rjsf/core` to add `className="list-inline-item"` to the `LI` tags

## @rjsf/chakra-ui

- Fixed the `SelectWidget` to allow the proper display of the selected value, fixing [#3422](https://github.com/rjsf-team/react-jsonschema-form/issues/3422)

## @rjsf/core

- Fixed `Form` to remove passing `excludeObjectChildren` to `getDefaultFormState()`, fixing [#3424](https://github.com/rjsf-team/react-jsonschema-form/issues/3424) and [#675](https://github.com/rjsf-team/react-jsonschema-form/issues/675)
- Added new feature prop `focusOnFirstError`, that if true, will cause the first field with an error to be focused on when a submit has errors

## @rjsf/utils

- Updated `computeDefaults()` to fix additionalProperties defaults not being propagated, fixing [#2593](https://github.com/rjsf-team/react-jsonschema-form/issues/2593)
  - Also made sure to properly deal with empty `anyOf`/`oneOf` lists by simply returning undefined
  - Add support for adding an empty object when that object is marked as required in a schema

## Dev / docs / playground

- Updated the playground to add a control for `focusOnFirstError` and the `form-props` documentation for it as well

# 5.0.2

## @rjsf/utils

- Added the `idPrefix`, `idSeparator` and `rawErrors` optional props to `FieldProps` since they were missing

## Dev / docs / playground

- Migrated latest documentation to Docusaurus, which is deployed to GitHub Pages.
- Updated readthedocs.io documentation site to guide users to the new docs site.
- Updated links in documentation and package README files to point to new site.
- Updated the `custom-widgets-field` documentation for the new `FieldProps`

# 5.0.1

- Updated the `peerDependencies` in all packages to remove the `-beta.x` tags from the `@rjsf/xxxx` packages

# 5.0.0

## @rjsf/antd

- Updated `CheckboxesWidget`, `RadioWidget` and `SelectWidget` to use indexes as values to support `enumOptions` with object values, fixing [#1494](https://github.com/rjsf-team/react-jsonschema-form/issues/1494)

## @rjsf/bootstrap-4

- Updated `CheckboxesWidget`, `RadioWidget` and `SelectWidget` to use indexes as values to support `enumOptions` with object values, fixing [#1494](https://github.com/rjsf-team/react-jsonschema-form/issues/1494)

## @rjsf/chakra-ui

- Updated `CheckboxesWidget`, `RadioWidget` and `SelectWidget` to use indexes as values to support `enumOptions` with object values, fixing [#1494](https://github.com/rjsf-team/react-jsonschema-form/issues/1494)

## @rjsf/core

- Updated `CheckboxesWidget`, `RadioWidget` and `SelectWidget` to use indexes as values to support `enumOptions` with object values, fixing [#1494](https://github.com/rjsf-team/react-jsonschema-form/issues/1494)

## @rjsf/fluent-ui

- Updated `CheckboxesWidget`, `RadioWidget` and `SelectWidget` to use indexes as values to support `enumOptions` with object values, fixing [#1494](https://github.com/rjsf-team/react-jsonschema-form/issues/1494)

## @rjsf/material-ui

- Updated `CheckboxesWidget`, `RadioWidget` and `SelectWidget` to use indexes as values to support `enumOptions` with object values, fixing [#1494](https://github.com/rjsf-team/react-jsonschema-form/issues/1494)

## @rjsf/mui

- Updated `CheckboxesWidget`, `RadioWidget` and `SelectWidget` to use indexes as values to support `enumOptions` with object values, fixing [#1494](https://github.com/rjsf-team/react-jsonschema-form/issues/1494)

## @rjsf/semantic-ui

- Updated `CheckboxesWidget`, `RadioWidget` and `SelectWidget` to use indexes as values to support `enumOptions` with object values, fixing [#1494](https://github.com/rjsf-team/react-jsonschema-form/issues/1494)

## @rjsf/utils

- Added `enumOptionsIndexForValue()`, `enumOptionsIsSelected()`, `enumOptionsValueForIndex()` functions to support fixing [#1494](https://github.com/rjsf-team/react-jsonschema-form/issues/1494)
  - Updated `enumOptionsDeselectValue()`, `enumOptionsSelectValue()` and `optionId()` to use indexes instead of values
  - Deleted the `processSelectValue()` that was added in the beta and is no longer needed
- Updated `getSchemaType()` to remove the inference of type from `anyOf`/`oneOf`, fixing [#3412](https://github.com/rjsf-team/react-jsonschema-form/issues/3412)

## Dev / docs / playground

- Updated the `utility-functions` documentation for the new and updated methods mentioned above, as well as deleting the documentation for `processSelectValue()`
- Updated the playground to add a new `Enum Objects` example to highlight the use of indexes for `enumOptions`
- Updated `5.x migration guide` to document the change from values to indexes for the `enumOptions` based controls.

# 5.0.0-beta.20

## @rjsf/antd

- Fixed `schema.examples` to deduplicate when `schema.default` exists in the examples, fixing [#3393](https://github.com/rjsf-team/react-jsonschema-form/issues/3393)

## @rjsf/bootstrap-4

- Fixed `schema.examples` to deduplicate when `schema.default` exists in the examples, fixing [#3393](https://github.com/rjsf-team/react-jsonschema-form/issues/3393)

## @rjsf/chakra-ui

- Fixed `schema.examples` to deduplicate when `schema.default` exists in the examples, fixing [#3393](https://github.com/rjsf-team/react-jsonschema-form/issues/3393)

## @rjsf/core

- Updated `MultiSchemaField` to pass `undefined` as the value to the widget when the `selectedOption` is -1, supporting `SelectWidget` implementations that allow the user to clear the selected value of the `anyOf`/`oneOf` field.
- Updated `Form` to support receiving an optional `ref` prop.
- Updated `Form` to restore providing empty root level objects, fixing [#3391](https://github.com/rjsf-team/react-jsonschema-form/issues/3391)
- Fixed `schema.examples` to deduplicate when `schema.default` exists in the examples, fixing [#3393](https://github.com/rjsf-team/react-jsonschema-form/issues/3393)

## @rjsf/fluent-ui

- Fixed `schema.examples` to deduplicate when `schema.default` exists in the examples, fixing [#3393](https://github.com/rjsf-team/react-jsonschema-form/issues/3393)

## @rjsf/material-ui

- Fixed `schema.examples` to deduplicate when `schema.default` exists in the examples, fixing [#3393](https://github.com/rjsf-team/react-jsonschema-form/issues/3393)

## @rjsf/mui

- Fixed `schema.examples` to deduplicate when `schema.default` exists in the examples, fixing [#3393](https://github.com/rjsf-team/react-jsonschema-form/issues/3393)

## @rjsf/semantic-ui

- Fixed `schema.examples` to deduplicate when `schema.default` exists in the examples, fixing [#3393](https://github.com/rjsf-team/react-jsonschema-form/issues/3393)

# 5.0.0-beta.19

## @rjsf/core

- Updated `MultiSchemaField` to cache options with refs in state and to output better labels for options without them when a title is available in either the `schema` or `uiSchema`
- Improved fix for [#2691](https://github.com/rjsf-team/react-jsonschema-form/issues/2691) to remove the breaking change caused by the original fix [#2980](https://github.com/rjsf-team/react-jsonschema-form/issues/2980) as follows:
  - Added a new `ui:fieldReplacesAnyOrOneOf` flag to the `uiSchema` that when true will allow users to opt-out of the `anyOf`/`oneOf` wrapping of a custom field

## @rjsf/utils

- Updated `toPathSchema()` to handle `oneOf`/`anyOf` by picking the closest option and generating the path for it, fixing [#2262](https://github.com/rjsf-team/react-jsonschema-form/issues/2262)
- Added new `uiSchema` only flag `ui:fieldReplacesAnyOrOneOf` that, if true allows the user to opt-out of the `anyOf`/`oneOf` wrapping of a custom field

## Dev / docs / playground

- Updated the `uiSchema` documentation for `ui:fieldReplacesAnyOrOneOf`

# 5.0.0-beta.18

## @rjsf/core

- Updated `MultiSchemaField` to utilize the new `getClosestMatchingOption()` and `sanitizeDataForNewSchema()` functions, fixing the following issues:
  - [#3236](https://github.com/rjsf-team/react-jsonschema-form/issues/3236)
  - [#2978](https://github.com/rjsf-team/react-jsonschema-form/issues/2978)
  - [#2944](https://github.com/rjsf-team/react-jsonschema-form/issues/2944)
  - [#2202](https://github.com/rjsf-team/react-jsonschema-form/issues/2202)
  - [#2183](https://github.com/rjsf-team/react-jsonschema-form/issues/2183)
  - [#2086](https://github.com/rjsf-team/react-jsonschema-form/issues/2086)
  - [#2069](https://github.com/rjsf-team/react-jsonschema-form/issues/2069)
  - [#1661](https://github.com/rjsf-team/react-jsonschema-form/issues/1661)
  - And probably others
- Updated `ObjectField` to deal with `additionalProperties` with `oneOf`/`anyOf`, fixing [#2538](https://github.com/rjsf-team/react-jsonschema-form/issues/2538)
- Updated `Form`, `MultiSchemaField`, `ObjectField` and `SchemaField` to properly support making `formData` optional, fixing [#3305](https://github.com/rjsf-team/react-jsonschema-form/issues/3305)

## @rjsf/material-ui

- Fix shrinking of `SelectWidget` label only if value is not empty, fixing [#3369](https://github.com/rjsf-team/react-jsonschema-form/issues/3369)

## @rjsf/mui

- Fix shrinking of `SelectWidget` label only if value is not empty, fixing [#3369](https://github.com/rjsf-team/react-jsonschema-form/issues/3369)

## @rjsf/utils

- Added new `getClosestMatchingOption()`, `getFirstMatchingOption()` and `sanitizeDataForNewSchema()` schema-based utility functions
  - Deprecated `getMatchingOption()` and updated all calls to it in other utility functions to use `getFirstMatchingOption()`
- Updated `stubExistingAdditionalProperties()` to deal with `additionalProperties` with `oneOf`/`anyOf`, fixing [#2538](https://github.com/rjsf-team/react-jsonschema-form/issues/2538)
- Updated `getSchemaType()` to grab the type of the first element of a `oneOf`/`anyOf`, fixing [#1654](https://github.com/rjsf-team/react-jsonschema-form/issues/1654)
- Updated all props or function parameters of the generic type `T` to allow for them to be optionally provided, fixing [#3305](https://github.com/rjsf-team/react-jsonschema-form/issues/3305)
  - This was done in both the types file and the actual implementation code

## @rjsf/validator-ajv6

- Updated places where `formData` was required as a function argument to make it optional, fixing [#3305](https://github.com/rjsf-team/react-jsonschema-form/issues/3305)

## @rjsf/validator-ajv8

- Updated places where `formData` was required as a function argument to make it optional, fixing [#3305](https://github.com/rjsf-team/react-jsonschema-form/issues/3305)

## Dev / docs / playground

- Updated the playground to `onFormDataEdited()` to only change the formData in the state if the `JSON.stringify()` of the old and new values are different, partially fixing [#3236](https://github.com/rjsf-team/react-jsonschema-form/issues/3236)
- Updated the playground `npm start` command to always use the `--force` option to avoid issues where changes made to other packages weren't getting picked up due to `vite` caching
- Updated the documentation for `utility-functions` and the `5.x upgrade guide` to add the new utility functions and to document the deprecation of `getMatchingOption()`
  - Also updated `utility-functions`, making all optional parameters without a default (as denoted by the syntax `[<parameter>]: <type>`) to add ` | undefined` onto the type to make it clear it supports passing in undefined as a value.

# 5.0.0-beta.17

## @rjsf/antd

- Enable searching in the `SelectWidget` by the label that the user sees rather than by the value
- Added support for new `style` prop on `FieldTemplate` and `WrapIfAdditionalTemplate` rendering them on the outermost wrapper, partially fixing [#1200](https://github.com/rjsf-team/react-jsonschema-form/issues/1200)
- Updated all the user "input" controls to have an `aria-describedby` value built using the `ariaDescribedByIds()` function, partially fixing [#959](https://github.com/rjsf-team/react-jsonschema-form/issues/959)
  - Also updated the generation of ids for the title, description, error, examples, options and help blocks using the associated new id generation utilty functions

## @rjsf/bootstrap-4

- Added support for new `style` prop on `FieldTemplate` and `WrapIfAdditionalTemplate` rendering them on the outermost wrapper, partially fixing [#1200](https://github.com/rjsf-team/react-jsonschema-form/issues/1200)
- Updated `CheckboxesWidget` to treat the value as an array when selecting/deselecting values and when determining the checked state - fixing [#2141](https://github.com/rjsf-team/react-jsonschema-form/issues/2141)
- Updated all the user "input" controls to have an `aria-describedby` value built using the `ariaDescribedByIds()` function, partially fixing [#959](https://github.com/rjsf-team/react-jsonschema-form/issues/959)
  - Also updated the generation of ids for the title, description, error, examples, options and help blocks using the associated new id generation utilty functions

## @rjsf/chakra-ui

- Added support for new `style` prop on `FieldTemplate` and `WrapIfAdditionalTemplate` rendering them on the outermost wrapper, partially fixing [#1200](https://github.com/rjsf-team/react-jsonschema-form/issues/1200)
- Updated `CheckboxesWidget` to treat the value as an array when selecting/deselecting values and when determining the checked state - fixing [#2141](https://github.com/rjsf-team/react-jsonschema-form/issues/2141)
- Updated all the user "input" controls to have an `aria-describedby` value built using the `ariaDescribedByIds()` function, partially fixing [#959](https://github.com/rjsf-team/react-jsonschema-form/issues/959)
  - Also updated the generation of ids for the title, description, error, examples, options and help blocks using the associated new id generation utilty functions

## @rjsf/core

- Updated `SchemaField` to handle the new `style` prop in the `uiSchema` similarly to `classNames`, passing it to the `FieldTemplate` and removing it from being passed down to children.
  - Also, added support for new `style` prop on `FieldTemplate` and `WrapIfAdditionalTemplate` rendering them on the outermost wrapper
  - This partially fixes [#1200](https://github.com/rjsf-team/react-jsonschema-form/issues/1200)
- Updated `CheckboxesWidget` to treat the value as an array when selecting/deselecting values and when determining the checked state - fixing [#2141](https://github.com/rjsf-team/react-jsonschema-form/issues/2141)
- Updated all the user "input" controls to have an `aria-describedby` value built using the `ariaDescribedByIds()` function, partially fixing [#959](https://github.com/rjsf-team/react-jsonschema-form/issues/959)
  - Also updated the generation of ids for the title, description, error, examples, options and help blocks using the associated new id generation utilty functions

## @rjsf/fluent-ui

- Added support for new `style` prop on `FieldTemplate` rendering them on the outermost wrapper, partially fixing [#1200](https://github.com/rjsf-team/react-jsonschema-form/issues/1200)
- Updated `CheckboxesWidget` to treat the value as an array when selecting/deselecting values and when determining the checked state - fixing [#2141](https://github.com/rjsf-team/react-jsonschema-form/issues/2141)
- Updated all the user "input" controls to have an `aria-describedby` value built using the `ariaDescribedByIds()` function, partially fixing [#959](https://github.com/rjsf-team/react-jsonschema-form/issues/959)
  - Also updated the generation of ids for the title, description, error, examples, options and help blocks using the associated new id generation utilty functions

## @rjsf/material-ui

- Updated `SelectWidget` to support additional `TextFieldProps` in a manner similar to how `BaseInputTemplate` does
- Added support for new `style` prop on `FieldTemplate` and `WrapIfAdditionalTemplate` rendering them on the outermost wrapper, partially fixing [#1200](https://github.com/rjsf-team/react-jsonschema-form/issues/1200)
- Updated `CheckboxesWidget` to treat the value as an array when selecting/deselecting values and when determining the checked state - fixing [#2141](https://github.com/rjsf-team/react-jsonschema-form/issues/2141)
- Updated all the user "input" controls to have an `aria-describedby` value built using the `ariaDescribedByIds()` function, partially fixing [#959](https://github.com/rjsf-team/react-jsonschema-form/issues/959)
  - Also updated the generation of ids for the title, description, error, examples, options and help blocks using the associated new id generation utilty functions

## @rjsf/mui

- Updated `SelectWidget` to support additional `TextFieldProps` in a manner similar to how `BaseInputTemplate` does
- Added support for new `style` prop on `FieldTemplate` and `WrapIfAdditionalTemplate` rendering them on the outermost wrapper, partially fixing [#1200](https://github.com/rjsf-team/react-jsonschema-form/issues/1200)
- Updated `CheckboxesWidget` to treat the value as an array when selecting/deselecting values and when determining the checked state - fixing [#2141](https://github.com/rjsf-team/react-jsonschema-form/issues/2141)
- Updated all the user "input" controls to have an `aria-describedby` value built using the `ariaDescribedByIds()` function, partially fixing [#959](https://github.com/rjsf-team/react-jsonschema-form/issues/959)
  - Also updated the generation of ids for the title, description, error, examples, options and help blocks using the associated new id generation utilty functions

## @rjsf/semantic-ui

- Added support for new `style` prop on `FieldTemplate` and `WrapIfAdditionalTemplate` rendering them on the outermost wrapper, partially fixing [#1200](https://github.com/rjsf-team/react-jsonschema-form/issues/1200)
- Updated `CheckboxesWidget` to treat the value as an array when selecting/deselecting values and when determining the checked state - fixing [#2141](https://github.com/rjsf-team/react-jsonschema-form/issues/2141)
- Updated all the user "input" controls to have an `aria-describedby` value built using the `ariaDescribedByIds()` function, partially fixing [#959](https://github.com/rjsf-team/react-jsonschema-form/issues/959)
  - Also updated the generation of ids for the title, description, error, examples, options and help blocks using the associated new id generation utilty functions

## @rjsf/utils

- Updated the `FieldTemplateProps`, `WrapIfAdditionalTemplateProps` and `UIOptionsBaseType` types to add `style?: StyleHTMLAttributes<any>`, partially fixing [#1200](https://github.com/rjsf-team/react-jsonschema-form/issues/1200)
- Added `enumOptionsDeselectValue()` and `enumOptionsSelectValue()` as a loose refactor of the duplicated functions in the various `CheckboxesWidget` implementations
- Updated the `FieldTemplateProps`, `WrapIfAdditionalTemplateProps` and `UIOptionsBaseType` types to add `style?: StyleHTMLAttributes<any>`, partially fixing [#1200](https://github.com/rjsf-team/react-jsonschema-form/issues/1200)
- Added new `ariaDescribedByIds()`, `descriptionId()`, `errorId()`, `examplesId()`, `helpId()` `optionId()` and `titleId()` id generator functions

## @rjsf/validator-ajv8

- Remove alias for ajv -> ajv8 in package.json. This fixes [#3215](https://github.com/rjsf-team/react-jsonschema-form/issues/3215).
- Updated `AJV8Validator#transformRJSFValidationErrors` to return more human-readable error messages. The ajv8 `ErrorObject` message is enhanced by replacing the error message field with either the `uiSchema`'s `ui:title` field if one exists or the `parentSchema` title if one exists. Fixes [#3246](https://github.com/rjsf-team/react-jsonschema-form/issues/3246)

## Dev / docs / playground

- In the playground, change Vite `preserveSymlinks` to `true`, which provides an alternative fix for [#3228](https://github.com/rjsf-team/react-jsonschema-form/issues/3228) since the prior fix caused [#3215](https://github.com/rjsf-team/react-jsonschema-form/issues/3215).
- Updated the `custom-templates.md` and `uiSchema.md` to document the new `style` prop
- Updated the `validation.md` documentation to describe the new `uiSchema` parameter passed to the `customValidate()` and `transformError()` functions
- Updated the `utility-functions` documentation to add the new `enumOptionsDeselectValue()` and `enumOptionsSelectValue()` functions and to describe the new id generator functions
- Updated the `5.x migration guide` documentation to describe potential breaking `id` changes

# 5.0.0-beta.16

## @rjsf/antd

- Updated the usage of the `ButtonTemplates` to pass the new required `registry` prop, filtering it out in the actual implementations before spreading props, fixing - [#3314](https://github.com/rjsf-team/react-jsonschema-form/issues/3314)
- Updated the test for the `CheckboxWidget` validating that the `schema.title` is passed as the label, fixing [#3302](https://github.com/rjsf-team/react-jsonschema-form/issues/3302)
- Updated the theme to accept generic types, exporting `generateXXX` functions for `Form`, `Theme`, `Templates` and `Widgets` to support using the theme with user-specified type generics, partially fixing [#3072](https://github.com/rjsf-team/react-jsonschema-form/issues/3072)
- Updated the use of the deprecated `withConfigConsumer` with the `ConfigConsumer` component instead, fixing [#3336](https://github.com/rjsf-team/react-jsonschema-form/issues/3336)

## @rjsf/bootstrap-4

- Updated the usage of the `ButtonTemplates` to pass the new required `registry` prop, filtering it out in the actual implementations before spreading props, fixing - [#3314](https://github.com/rjsf-team/react-jsonschema-form/issues/3314)
- Updated `CheckboxWidget` to get the `required` state of the checkbox from the `schemaRequiresTrueValue()` utility function rather than the `required` prop, fixing [#3317](https://github.com/rjsf-team/react-jsonschema-form/issues/3317)
- Updated the test for the `CheckboxWidget` validating that the `schema.title` is passed as the label, fixing [#3302](https://github.com/rjsf-team/react-jsonschema-form/issues/3302)
- Updated the theme to accept generic types, exporting `generateXXX` functions for `Form`, `Theme`, `Templates` and `Widgets` to support using the theme with user-specified type generics, partially fixing [#3072](https://github.com/rjsf-team/react-jsonschema-form/issues/3072)

## @rjsf/chakra-ui

- Updated the usage of the `ButtonTemplates` to pass the new required `registry` prop, filtering it out in the actual implementations before spreading props, fixing - [#3314](https://github.com/rjsf-team/react-jsonschema-form/issues/3314)
- Updated `CheckboxWidget` to get the `required` state of the checkbox from the `schemaRequiresTrueValue()` utility function rather than the `required` prop, fixing [#3317](https://github.com/rjsf-team/react-jsonschema-form/issues/3317)
- Updated the test for the `CheckboxWidget` validating that the `schema.title` is passed as the label, fixing [#3302](https://github.com/rjsf-team/react-jsonschema-form/issues/3302)
- Updated the theme to accept generic types, exporting `generateXXX` functions for `Form`, `Theme`, `Templates` and `Widgets` to support using the theme with user-specified type generics, partially fixing [#3072](https://github.com/rjsf-team/react-jsonschema-form/issues/3072)

## @rjsf/core

- Updated the usage of the `ButtonTemplates` to pass the new required `registry` prop, filtering it out in the actual implementations before spreading props, fixing - [#3314](https://github.com/rjsf-team/react-jsonschema-form/issues/3314)
  - Also, passed `registry` into the `SubmitButton` inside of the `Form` as part of this fix
- Updated `ArrayField` to pass the new `totalItems` and `canAdd` props to the `ArrayFieldItemTemplate` instances, fixing [#3315](https://github.com/rjsf-team/react-jsonschema-form/issues/3315)
  - Also refactored the near duplicate logic for `onAddClick` and `onAddIndexClick` into a new `_handleAddClick()` function, fixing [#3316](https://github.com/rjsf-team/react-jsonschema-form/issues/3316)
- Fix passing of generic types to a few helper methods, partially fixing [#3072](https://github.com/rjsf-team/react-jsonschema-form/issues/3072)
- Updated the types for `ValidatorType`, `CustomValidator` and `ErrorTransformer` to add the new generics, as well as passing `uiSchema` to the `validateFormData()` call, partially fixing [#3170](https://github.com/rjsf-team/react-jsonschema-form/issues/3170)

## @rjsf/fluent-ui

- Updated the usage of the `ButtonTemplates` to pass the new required `registry` prop, filtering it out in the actual implementations before spreading props, fixing - [#3314](https://github.com/rjsf-team/react-jsonschema-form/issues/3314)
- Updated the test for the `CheckboxWidget` validating that the `schema.title` is passed as the label, fixing [#3302](https://github.com/rjsf-team/react-jsonschema-form/issues/3302)
- Updated the theme to accept generic types, exporting `generateXXX` functions for `Form`, `Theme`, `Templates` and `Widgets` to support using the theme with user-specified type generics, partially fixing [#3072](https://github.com/rjsf-team/react-jsonschema-form/issues/3072)

## @rjsf/material-ui

- Updated the usage of the `ButtonTemplates` to pass the new required `registry` prop, filtering it out in the actual implementations before spreading props, fixing - [#3314](https://github.com/rjsf-team/react-jsonschema-form/issues/3314)
- Updated the test for the `CheckboxWidget` validating that the `schema.title` is passed as the label, fixing [#3302](https://github.com/rjsf-team/react-jsonschema-form/issues/3302)
- Updated the theme to accept generic types, exporting `generateXXX` functions for `Form`, `Theme`, `Templates` and `Widgets` to support using the theme with user-specified type generics, partially fixing [#3072](https://github.com/rjsf-team/react-jsonschema-form/issues/3072)

## @rjsf/mui

- Updated the usage of the `ButtonTemplates` to pass the new required `registry` prop, filtering it out in the actual implementations before spreading props, fixing - [#3314](https://github.com/rjsf-team/react-jsonschema-form/issues/3314)
- Updated the test for the `CheckboxWidget` validating that the `schema.title` is passed as the label, fixing [#3302](https://github.com/rjsf-team/react-jsonschema-form/issues/3302)
- Updated the theme to accept generic types, exporting `generateXXX` functions for `Form`, `Theme`, `Templates` and `Widgets` to support using the theme with user-specified type generics, partially fixing [#3072](https://github.com/rjsf-team/react-jsonschema-form/issues/3072)

## @rjsf/semantic-ui

- Updated the usage of the `ButtonTemplates` to pass the new required `registry` prop, filtering it out in the actual implementations before spreading props, fixing - [#3314](https://github.com/rjsf-team/react-jsonschema-form/issues/3314)
- Updated `CheckboxWidget` to get the `required` state of the checkbox from the `schemaRequiresTrueValue()` utility function rather than the `required` prop, fixing [#3317](https://github.com/rjsf-team/react-jsonschema-form/issues/3317)
  - Also fixed the `CheckboxWidget` missing label issue [#3302](https://github.com/rjsf-team/react-jsonschema-form/issues/3302)
- Updated the test for the `CheckboxWidget` validating that the `schema.title` is passed as the label, fixing [#3302](https://github.com/rjsf-team/react-jsonschema-form/issues/3302)
- Updated the theme to accept generic types, exporting `generateXXX` functions for `Form`, `Theme`, `Templates` and `Widgets` to support using the theme with user-specified type generics, partially fixing [#3072](https://github.com/rjsf-team/react-jsonschema-form/issues/3072)

## @rjsf/utils

- Updated the `SubmitButtonProps` and `IconButtonProps` to add required `registry` prop, fixing - [#3314](https://github.com/rjsf-team/react-jsonschema-form/issues/3314)
- Updated the `ArrayFieldTemplateItemType` to add the new `totalItems` and `canAdd` props, fixing [#3315](https://github.com/rjsf-team/react-jsonschema-form/issues/3315)
- Updated the `CustomValidator` and `ErrorTransformer` types to take the full set of `T`, `S`, `F` generics in order to accept a new optional `uiSchema` property, partially fixing [#3170](https://github.com/rjsf-team/react-jsonschema-form/issues/3170)
- Updated the `ValidatorType` to add the `F` generic to allow the `validateFormData()` function to take a new optional `uiSchema` parameter, partially fixing [#3170](https://github.com/rjsf-team/react-jsonschema-form/issues/3170)
  - Updated many of the schema-based utility functions to take the additional generics as well to fulfill the `ValidatorType` interface change

## @rjsf/validator-ajv6

- Updated the `customizeValidator` and `AJV6Validator` implementations to add the `S` and `F` generics, so that `validateFormData()` can accept a new optional `uiSchema` parameter that is passed to `transformErrors()` and `customValidate()`, partially fixing [#3170](https://github.com/rjsf-team/react-jsonschema-form/issues/3170)

## @rjsf/validator-ajv8

- Updated the `customizeValidator` and `AJV8Validator` implementations to add the `F` generic, so that `validateFormData()` can accept a new optional `uiSchema` parameter that is passed to `transformErrors()` and `customValidate()`, partially fixing [#3170](https://github.com/rjsf-team/react-jsonschema-form/issues/3170)

## Dev / docs / playground

- Fixed the documentation for `ArrayFieldItemTemplate`, `SubmitButtonProps` and `IconButtonProps` as part of the fix for [#3314](https://github.com/rjsf-team/react-jsonschema-form/issues/3314) and [#3315](https://github.com/rjsf-team/react-jsonschema-form/issues/3315)
- Updated the documentation in `form-props.md` for `children`, fixing [#3322](https://github.com/rjsf-team/react-jsonschema-form/issues/3322)
- Added new `typescript.md` documentation to `Advanced Customization` describing how to use custom generics as part of the fix for [#3072](https://github.com/rjsf-team/react-jsonschema-form/issues/3072)
- Updated the documentation in `utilty-functions.md` to add the new `F` generic to all the places which needed them

# 5.0.0-beta.15

## @rjsf/core

- Pass the `schema` along to the `ArrayFieldItemTemplate` as part of the fix for [#3253](https://github.com/rjsf-team/react-jsonschema-form/issues/3253)
- Tweak Babel configuration to emit ES5-compatible output files, fixing [#3240](https://github.com/rjsf-team/react-jsonschema-form/issues/3240)

## @rjsf/material-ui

- Reverse the condition used in the `onChange` handler in the `RangeWidget`, fixing [#2161](https://github.com/rjsf-team/react-jsonschema-form/issues/2161)

## @rjsf/mui

- Reverse the condition used in the `onChange` handler in the `RangeWidget`, fixing [#2161](https://github.com/rjsf-team/react-jsonschema-form/issues/2161)

## @rjsf/utils

- Update the `ArrayFieldItemTemplate` to add `schema` as part of the fix for [#3253](https://github.com/rjsf-team/react-jsonschema-form/issues/3253)
- Fix improper merging of nested `allOf`s ([#3025](https://github.com/rjsf-team/react-jsonschema-form/pull/3025), [#3227](https://github.com/rjsf-team/react-jsonschema-form/pull/3227)), fixing [#2923](https://github.com/rjsf-team/react-jsonschema-form/pull/2929)
- Added a new `ErrorSchemaBuilder` class to enable building a proper `ErrorSchema` without crazy castings, fixing [#3239](https://github.com/rjsf-team/react-jsonschema-form/issues/3239)

## @rjsf/validator-ajv6

- Updated the validator to use the `ErrorSchemaBuilder` in the `toErrorSchema()` function to simplify the implementation

## @rjsf/validator-ajv8

- Updated the validator to use the `ErrorSchemaBuilder` in the `toErrorSchema()` function to simplify the implementation
- Updated the validator to properly map missing required field errors in the `ErrorSchema`, fixing [#3260](https://github.com/rjsf-team/react-jsonschema-form/issues/3260)

## Dev / docs / playground

- Fixed the documentation for `ArrayFieldItemTemplate` as part of the fix for [#3253](https://github.com/rjsf-team/react-jsonschema-form/issues/3253)
- Added documentation for `ErrorSchemaBuilder` in the `utility-functions.md`, fixing [#3239](https://github.com/rjsf-team/react-jsonschema-form/issues/3239)

# 5.0.0-beta.14

## @rjsf/antd

- No longer render extra 0 for array without errors, fixing [#3233](https://github.com/rjsf-team/react-jsonschema-form/issues/3233)

## @rjsf/core

- Added `ref` definition to `ThemeProps` fixing [#2135](https://github.com/rjsf-team/react-jsonschema-form/issues/2135)
- Updated the `onChange` handler in `Form` to use the new `preventDuplicates` mode of `mergeObjects()` when merging `extraErrors` when live validation is off, fixing [#3169](https://github.com/rjsf-team/react-jsonschema-form/issues/3169)

## @rjsf/material-ui

- Fix RangeWidget missing htmlFor and schema.title [#3281](https://github.com/rjsf-team/react-jsonschema-form/pull/3281)

## @rjsf/mui

- Fix RangeWidget missing htmlFor and schema.title [#3281](https://github.com/rjsf-team/react-jsonschema-form/pull/3281)

## @rjsf/utils

- Updated `computedDefaults` (used by `getDefaultFormState`) to skip saving the computed default if it's an empty object unless `includeUndefinedValues` is truthy, fixing [#2150](https://github.com/rjsf-team/react-jsonschema-form/issues/2150) and [#2708](https://github.com/rjsf-team/react-jsonschema-form/issues/2708)
- Expanded the `getDefaultFormState` util's `includeUndefinedValues` prop to accept a boolean or `"excludeObjectChildren"` if it does not want to include undefined values in nested objects
- Updated `mergeObjects` to add new `preventDuplicates` mode when concatenating arrays so that only unique values from the source object array are copied to the destination object array
- Fix `isObject` to correctly identify 'Date' as not an object, similar to 'File', thus preventing them from being merged with Object default values.

## Dev / docs / playground

- Removed extraneous leading space on the examples in the validation documentation, fixing [#3282](https://github.com/rjsf-team/react-jsonschema-form/issues/3282)
- Updated the documentation for `mergeObjects()` for the new `preventDuplicates` mode of concatenating arrays
- Updated the documentation for unpkg releases to the correct name fixing the confusion found in [#3262](https://github.com/rjsf-team/react-jsonschema-form/issues/3262)

# 5.0.0-beta.13

## @rjsf/playground

- Fix Vite development server [#3228](https://github.com/rjsf-team/react-jsonschema-form/issues/3228)

## @rjsf/validator-ajv8

- BREAKING CHANGE: Disable form data validation for invalid JSON Schemas. Use @rjsf/validator-ajv6 if you need to validate against invalid schemas.
- Fix additionalProperties validation [#3213](https://github.com/rjsf-team/react-jsonschema-form/issues/3213)
- Report all schema errors thrown by Ajv. Previously, we would only report errors thrown for a missing meta-schema. This behavior is unchanged for @rjsf/validator-ajv6.
- Disable Ajv strict mode by default.
- Add RJSF-specific additional properties keywords to Ajv to prevent errors from being reported in strict mode.
- For JSON Schemas with `$id`s, use a pre-compiled Ajv validation function when available.
- No longer fail to validate inner schemas with `$id`s, fixing [#2821](https://github.com/rjsf-team/react-jsonschema-form/issues/2181).

# 5.0.0-beta.12

## @rjsf/antd

- Updated the tests to use the `@rjsf/validator-ajv8` fixing [#3110](https://github.com/rjsf-team/react-jsonschema-form/issues/3110)

## @rjsf/bootstrap

- Updated the tests to use the `@rjsf/validator-ajv8` fixing [#3110](https://github.com/rjsf-team/react-jsonschema-form/issues/3110)

## @rjsf/chakra-ui

- Automatically close single-choice Select widget on selection
- Updated the tests to use the `@rjsf/validator-ajv8` fixing [#3110](https://github.com/rjsf-team/react-jsonschema-form/issues/3110)

## @rjsf/core

- BREAKING CHANGE: ShowErrorList prop changed to support `false`, `top` or `bottom`; `true` is no longer a valid value as the default changed from `true` to `top` [#634](https://github.com/rjsf-team/react-jsonschema-form/issues/634)
- Added the new generic, `S extends StrictRJSFSchema = RJSFSchema`, for `schema`/`rootSchema` to every component that needed it.
- Fix omitExtraData with field names with dots #2643
- Updated the tests to use the `@rjsf/validator-ajv8` fixing [#3110](https://github.com/rjsf-team/react-jsonschema-form/issues/3110)
- Changed the `F = any` generic to be `F extends FormContextType = any` to better support how `formContext` is defined and used, partially fixing [#3072](https://github.com/rjsf-team/react-jsonschema-form/issues/3072)

## @rjsf/fluent-ui

- Updated the tests to use the `@rjsf/validator-ajv8` fixing [#3110](https://github.com/rjsf-team/react-jsonschema-form/issues/3110)

## @rjsf/material-ui

- Updated the tests to use the `@rjsf/validator-ajv8` fixing [#3110](https://github.com/rjsf-team/react-jsonschema-form/issues/3110)

## @rjsf/mui

- Updated the tests to use the `@rjsf/validator-ajv8` fixing [#3110](https://github.com/rjsf-team/react-jsonschema-form/issues/3110)

## @rjsf/semantic-ui

- Updated the tests to use the `@rjsf/validator-ajv8` fixing [#3110](https://github.com/rjsf-team/react-jsonschema-form/issues/3110)

## @rjsf/utils

- Beta-only potentially BREAKING CHANGE: Changed all types that directly or indirectly defined `schema`/`rootSchema` to add the generic `S extends StrictRJSFSchema = RJSFSchema` and use `S` as the type for them.
  - `StrictRJSFSchema` was added as the alias to `JSON7Schema` and `RJSFSchema` was modified to be `StrictRJSFSchema & GenericObjectType`
  - This new generic was added BEFORE the newly added `F = any` generic because it is assumed that more people will want to change the schema than the formContext types
  - This provides future support for the newer draft versions of the schema
- Updated the `ValidatorType` interface to add a new `rawValidation()` method for use by the playground
- Added the `FormContextType` alias to `GenericObjectType` and changing the `F = any` generic to be `F extends FormContextType = any` to better support how `formContext` is defined and used, partially fixing [#3072](https://github.com/rjsf-team/react-jsonschema-form/issues/3072)

## @rjsf/validator-ajv6

- Fixed a few type casts given the new expanded definition of the `RJSFSchema` type change
- Deprecated this library in favor of the `@rjsf/validator-ajv8`
- Refactored out the `rawValidation()` function for use by the playground

## @rjsf/validator-ajv8

- Updated the typing to add the new `S extends StrictRJSFSchema = RJSFSchema` generic and fixed up type casts
- Added the `AjvClass` prop to the `CustomValidatorOptionsType` to support using the `Ajv2019` or `Ajv2020` class implementation instead of the default `Ajv` class; fixing [#3189](https://github.com/rjsf-team/react-jsonschema-form/issues/3189)
- Refactored out the `rawValidation()` function for use by the playground

## Dev / docs / playground

- Updated the `5.x upgrade guide` and `utility-functions.md` to document the new `StrictRJSFSchema`, the `S` generic and changing the `F` generic extend
- Updated the `validation` guide to document the new `AjvClass` prop on `CustomValidatorOptionsType` and mentioning the deprecation of `@rjsf/validator-ajv6`
- Updated the playground to add support for using the AJV 8 validator with the `draft-2019-09` and `draft-2020-12` schemas and to make the `AJV8` validator the default validator, marking `AJV6` as deprecated
- Updated all the documentation to switch to Typescript notation where missing along with switching to using the `@rjsf/validator-ajv8` validator as the default
- Added a way of doing a raw Ajv validation in the playground to determine whether an issue is with RJSF or Ajv

# 5.0.0-beta.11

## @rjsf/antd

- Updated `FieldTemplate` to no longer render additional, unnecessary white space for fields that have empty `help` and `extra` information, fixing [#3147](https://github.com/rjsf-team/react-jsonschema-form/issues/3174)
- Updated `ArrayFieldTemplate` to always render `ArrayFieldDescriptionTemplate` since that template deals with the optional `description`
- Pass the `schema` into the `ArrayFieldDescriptionTemplate`, `ArrayFieldTitleTemplate`, `DescriptionFieldTemplate` and `TitleFieldTemplate`, fixing [#3176](https://github.com/rjsf-team/react-jsonschema-form/issues/3176)

## @rjsf/bootstrap-4

- Make label generation consistent with other themes by refactoring the code into the `FieldTemplate` instead of having the widgets implementing the label, fixing [#2007](https://github.com/rjsf-team/react-jsonschema-form/issues/2007)
- Updated `ArrayFieldTemplate` to always render `ArrayFieldDescriptionTemplate` since that template deals with the optional `description`
- Pass the `schema` into the `ArrayFieldDescriptionTemplate`, `ArrayFieldTitleTemplate`, `DescriptionFieldTemplate` and `TitleFieldTemplate`, fixing [#3176](https://github.com/rjsf-team/react-jsonschema-form/issues/3176)

## @rjsf/chakra-ui

- Added support for `chakra-react-select` v4, fixing [#3152](https://github.com/rjsf-team/react-jsonschema-form/issues/3152)
- In `SelectWidget` use `Select` from `chakra-react-select` for both single- and multiple-choice select
- In `SelectWidget` multiple-choice select display label rather than value for selected items
- Updated `ArrayFieldTemplate` to always render `ArrayFieldDescriptionTemplate` since that template deals with the optional `description`
- Pass the `schema` into the `ArrayFieldDescriptionTemplate`, `ArrayFieldTitleTemplate`, `DescriptionFieldTemplate` and `TitleFieldTemplate`, fixing [#3176](https://github.com/rjsf-team/react-jsonschema-form/issues/3176)

## @rjsf/core

- Extended `Form.onChange` to optionally return the `id` of the field that caused the change, fixing [#2768](https://github.com/rjsf-team/react-jsonschema-form/issues/2768)
- Fixed a regression in earlier v5 beta versions where additional properties could not be added when `additionalProperties` was `true` ([#3719](https://github.com/rjsf-team/react-jsonschema-form/pull/3719)).
- Fixed a regression in v5 beta version where BooleanField was altering readonly props ([#3188](https://github.com/rjsf-team/react-jsonschema-form/pull/3188).
- Updated `ArrayFieldDescriptionTemplate` and `ArrayFieldTitleTemplate` to not render content when `ui:label` is false, fixing [#2535](https://github.com/rjsf-team/react-jsonschema-form/issues/2535)
- Updated `ArrayFieldTemplate` to always render `ArrayFieldDescriptionTemplate` since that template deals with the optional `description`
- Pass the `schema` into the `ArrayFieldDescriptionTemplate`, `ArrayFieldTitleTemplate`, `DescriptionFieldTemplate` and `TitleFieldTemplate`, fixing [#3176](https://github.com/rjsf-team/react-jsonschema-form/issues/3176)

## @rjsf/fluent-ui

- Updated `ArrayFieldTemplate` to always render `ArrayFieldDescriptionTemplate` since that template deals with the optional `description`
- Pass the `schema` into the `ArrayFieldDescriptionTemplate`, `ArrayFieldTitleTemplate`, `DescriptionFieldTemplate` and `TitleFieldTemplate`, fixing [#3176](https://github.com/rjsf-team/react-jsonschema-form/issues/3176)

## @rjsf/material-ui

- Updated `ArrayFieldTemplate` to always render `ArrayFieldDescriptionTemplate` since that template deals with the optional `description`
- Pass the `schema` into the `ArrayFieldDescriptionTemplate`, `ArrayFieldTitleTemplate`, `DescriptionFieldTemplate` and `TitleFieldTemplate`, fixing [#3176](https://github.com/rjsf-team/react-jsonschema-form/issues/3176)

## @rjsf/mui

- Updated `ArrayFieldTemplate` to always render `ArrayFieldDescriptionTemplate` since that template deals with the optional `description`
- Pass the `schema` into the `ArrayFieldDescriptionTemplate`, `ArrayFieldTitleTemplate`, `DescriptionFieldTemplate` and `TitleFieldTemplate`, fixing [#3176](https://github.com/rjsf-team/react-jsonschema-form/issues/3176)

## @rjsf/semantic-ui

- Updated `ArrayFieldTemplate` to always render `ArrayFieldDescriptionTemplate` since that template deals with the optional `description`
- Pass the `schema` into the `ArrayFieldDescriptionTemplate`, `ArrayFieldTitleTemplate`, `DescriptionFieldTemplate` and `TitleFieldTemplate`, fixing [#3176](https://github.com/rjsf-team/react-jsonschema-form/issues/3176)

## @rjsf/utils

- Updated the `onChange` prop on `FieldProps` and `FieldTemplateProps` to add an optional `id` parameter to the callback.
- Updated the `DescriptionFieldProps` and `TitleFieldProps` to add a new required `schema` prop. Also updated the `ArrayFieldDescriptionTemplate` and `ArrayFieldTitleTemplate` to make `description` and `title` optional while pulling all the other props but `id` from the associated type.

## Dev / docs / playground

- Added an error boundary to prevent the entire app from crashing when an error is thrown by Form. See [#3164](https://github.com/rjsf-team/react-jsonschema-form/pull/3164) for closed issues.
- Updated the playground to log the `id` of the field being changed on the `onChange` handler
- Updated `form-props.md` to describe the new `id` parameter being returned by the `Form.onChange` handler
- Updated `custom-templates.md` to add the new `schema` prop to the `ArrayFieldDescriptionTemplate`, `ArrayFieldTitleTemplate`, `DescriptionFieldTemplate` and `TitleFieldTemplate` documentation
- Updated the `contributing.md` to describe setting up the `husky` precommit hooks for the first time `git clone` of the repo; Also added guidance for developing on underpowered computers; Finally discussed code-coverage requirements for some packages.

# 5.0.0-beta.10

## @rjsf/antd

- Convert `WrapIfAdditional` to `WrapIfAdditionalTemplate`
- Added `name` to the `input` components that were missing it to support `remix`
- Fixed `CheckboxesWidget` and `RadioWidget` to have unique `id`s for each radio element by appending the `option.value`, protecting against non-arrays
- Converted `antd` to Typescript, indirectly fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/3123)

## @rjsf/bootstrap

- Convert `WrapIfAdditional` to `WrapIfAdditionalTemplate`
- Added `name` to the `input` components that were missing it to support `remix`
- Simplified the `CheckboxWidgets` code to eliminate a ternary in favor of a simple `inline={inline}` property since all the rest of the props were the same
- Fixed `CheckboxesWidget` and `RadioWidget` to have unique `id`s for each radio element by appending the `option.value`, removing unnecessary casts to `any` and protecting against non-arrays
- Fixed an issue where `CheckboxesWidget` incorrectly rendered inner `<form>` elements around each checkbox, fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/2355)

## @rjsf/chakra-ui

- Convert `WrapIfAdditional` to `WrapIfAdditionalTemplate`
- Added `name` to the `input` components that were missing it to support `remix`
- Fixed `CheckboxesWidget` and `RadioWidget` to have unique `id`s for each radio element by appending the `option.value`, removing unnecessary casts to `any` and protecting against non-arrays

## @rjsf/core

- Convert `WrapIfAdditional` to `WrapIfAdditionalTemplate`
- Added `name` to the `input` components that were missing it to support `remix`
- Fixed `CheckboxesWidget` and `RadioWidget` to have unique `id`s for each radio element by appending the `option.value`
- Updated the `validate()` method on `Form` to make `schemaUtils` an optional third parameter rather than a required first parameter, making the signature backwards compatible with what was provided in previous versions.

## @rjsf/fluent-ui

- Add stubbed `WrapIfAdditionalTemplate`. `additionalProperties` is currently not supported in `@rjsf/fluent-ui` (See [#2777](https://github.com/rjsf-team/react-jsonschema-form/issues/2777)).
- Added `name` or `id` (for those fluent components not supporting name) to the `input` components that were missing it to support `remix`
- Fixed `DateTimeWidget` to properly use `BaseInputTemplate` rather than `TextWidget`
- Fixed `CheckboxesWidget` and `RadioWidget` to have unique `id`s for each radio element by appending the `option.value`, removing unnecessary casts and protecting against non-arrays, fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/2138)
- Fixed `RadioWidget` so that it supports read-only and disabled states

## @rjsf/material-ui

- Convert `WrapIfAdditional` to `WrapIfAdditionalTemplate`
- Added `name` to the `input` components that were missing it to support `remix`
- Fixed `CheckboxesWidget` and `RadioWidget` to have unique `id`s for each radio element by appending the `option.value`, removing unnecessary casts to `any` and protecting against non-arrays

## @rjsf/mui

- Convert `WrapIfAdditional` to `WrapIfAdditionalTemplate`
- Added `name` to the `input` components that were missing it to support `remix`
- Fixed `CheckboxesWidget` and `RadioWidget` to have unique `id`s for each radio element by appending the `option.value`, removing unnecessary casts to `any` and protecting against non-arrays

## @rjsf/semantic-ui

- Convert `WrapIfAdditional` to `WrapIfAdditionalTemplate`
- Fixed `ArrayFieldTemplate` and `ObjectFieldTemplate`'s `AddButton` to show the non-labeled version. (https://github.com/rjsf-team/react-jsonschema-form/pull/3142)
- Added `name` to the `input` components that were missing it to support `remix`, including fixing incorrect `name`s as `id`s in some situations
- Fixed `CheckboxesWidget` and `RadioWidget` to have unique `id`s for each radio element by appending the `option.value`, protecting against non-arrays
- Converted `semantic-ui` to Typescript

## @rjsf/utils

- Added `WrapIfAdditionalTemplate` and `WrapIfAdditionalTemplateProps` to simplify theming and make it easier to override Field behavior for schemas with `additionalProperties`.

# 5.0.0-beta.9

## @rjsf/antd

- Pass `uiSchema` appropriately to all of the `IconButton`s, `ArrayFieldItemTemplate` and `WrapIfAdditional` components, fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/3130)

## @rjsf/bootstrap

- Updated the `FieldErrorTemplate` to remove the explicit typing of the `error` to string to support the two options
- Updated `Theme` to use the renamed `ThemeProps` from `@rjsf/core`
- Pass `uiSchema` appropriately to all of the `IconButton`s, `ArrayFieldItemTemplate` and `WrapIfAdditional` components, fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/3130)

## @rjsf/chakra-ui

- Updated `Theme` to use the renamed `ThemeProps` from `@rjsf/core`
- Pass `uiSchema` appropriately to all of the `IconButton`s, `ArrayFieldItemTemplate` and `WrapIfAdditional` components, fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/3130)

## @rjsf/core

- Updated the `FieldErrorTemplate` to remove the explicit typing of the `error` to string to support the two options
- Implemented programmatic validation via new `validateForm()` method on `Form`, fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/2755, https://github.com/rjsf-team/react-jsonschema-form/issues/2552, https://github.com/rjsf-team/react-jsonschema-form/issues/2381, https://github.com/rjsf-team/react-jsonschema-form/issues/2343, https://github.com/rjsf-team/react-jsonschema-form/issues/1006, https://github.com/rjsf-team/react-jsonschema-form/issues/246)
- Renamed `WithThemeProps` to `ThemeProps` to prevent another breaking-change by returning the type back to the name it had in version 4
- Pass `uiSchema` appropriately to all of the `IconButton`s, `ArrayFieldItemTemplate` and `WrapIfAdditional` components, fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/3130)
- Updated `ArrayField` to fall back to `SchemaField` if `ArraySchemaField` is not defined, fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/3131)

## @rjsf/fluent-ui

- Updated `Theme` to use the renamed `ThemeProps` from `@rjsf/core`
- Pass `uiSchema` appropriately to all of the `IconButton`s and `ArrayFieldItemTemplate` components, fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/3130)

## @rjsf/material-ui

- Updated `Theme` to use the renamed `ThemeProps` from `@rjsf/core`
- Pass `uiSchema` appropriately to all of the `IconButton`s, `ArrayFieldItemTemplate` and `WrapIfAdditional` components, fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/3130)

## @rjsf/mui

- Updated `Theme` to use the renamed `ThemeProps` from `@rjsf/core`
- Pass `uiSchema` appropriately to all of the `IconButton`s, `ArrayFieldItemTemplate` and `WrapIfAdditional` components, fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/3130)

## @rjsf/semantic-ui

- Updated the `FieldErrorTemplate` to use the `children` variation of the `List.Item` that supports ReactElement
- Pass `uiSchema` appropriately to all of the `IconButton`s, `ArrayFieldItemTemplate` and `WrapIfAdditional` components, fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/3130)

## @rjsf/utils

- Updated the `FieldErrorProps` type to make it support an array of string and ReactElement
- Updated the `IconButtonProps` type to add `uiSchema`, adding the `<T = any, F = any>` generics to it and the associated `ButtonTemplates` in `TemplatesType` AND added `uiSchema` to `ArrayFieldTemplateItemType` as well, fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/3130)

## Dev / docs / playground

- Updated the `custom-templates.md` file to add the missing asterisk to the new `FieldErrorTemplate` and `FieldHelpTemplate`
- Updated the playground to add a new button for programmatically validating a form
- Also updated the `validation.md` documentation to describe how to programmatically validate a form
- Fixed the `chakra-ui` custom `uiSchema` documentation to make it clear they work on a per-field basis, fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/2865)
- Added `formElement` breaking-change documentation to the `5.x upgrade guide.md`
- Replace Webpack with Vite
- Updated documentation for `ArraySchemaField` to better represent the updated implementation, fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/3131)

# 5.0.0-beta.8

## @rjsf/core

- When rendering additional properties with title, use the key of the property instead of the title.

# v5.0.0-beta.7

## @rjsf/antd

- Only show description when there really IS a description, fixes (https://github.com/rjsf-team/react-jsonschema-form/issues/2779)
- Refactored the `FieldErrorTemplate` from inside of `FieldTemplate`; fixes (https://github.com/rjsf-team/react-jsonschema-form/issues/3104)

## @rjsf/bootstrap-4

- Refactored the `FieldErrorTemplate` and `FieldHelpTemplate` from inside of `FieldTemplate`; fixes (https://github.com/rjsf-team/react-jsonschema-form/issues/3104)

## @rjsf/chakra-ui

- Refactored the `FieldErrorTemplate` and `FieldHelpTemplate` from inside of `FieldTemplate`; fixes (https://github.com/rjsf-team/react-jsonschema-form/issues/3104)

## @rjsf/core

- Added new field `ArraySchemaField`, assigned to `SchemaField` by default, that is used by the `ArrayField` to render the `children` for each array field element
- Refactored the internal `ErrorList` and `Help` components from inside of `SchemaField` to new templates: `FieldErrorTemplate` and `FieldHelpTemplate`; fixes (https://github.com/rjsf-team/react-jsonschema-form/issues/3104)

## @rjsf/material-ui

- Refactored the `FieldErrorTemplate` and `FieldHelpTemplate` from inside of `FieldTemplate`; fixes (https://github.com/rjsf-team/react-jsonschema-form/issues/3104)

## @rjsf/mui

- Refactored the `FieldErrorTemplate` and `FieldHelpTemplate` from inside of `FieldTemplate`; fixes (https://github.com/rjsf-team/react-jsonschema-form/issues/3104)

## @rjsf/semantic-ui

- Converted `RawErrors` and `HelpField` into `FieldErrorTemplate` and `FieldHelpTemplate`, removing their explicit calls from `FieldTemplate`; fixes (https://github.com/rjsf-team/react-jsonschema-form/issues/3104)

## @rjsf/utils

- Added new `FieldErrorProps` and `FieldHelpProps` types
- Added new `FieldErrorTemplate` and `FieldHelpTemplate` to the `TemplatesType`

## Dev / docs / playground

- Updated the `custom-templates.md` file to add documentation for the new `FieldErrorTemplate` and `FieldHelpTemplate`
- Updated the `custom-widgets-fields.md` file to add documentation for the new `ArraySchemaField` field.

# v5.0.0-beta.6

## @rjsf/bootstrap-4

- Change custom attribute to bsPrefix by @WillowP, fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/2648)

## @rjsf/core

- Added tests for the new `@rjsf/validator-ajv8` to the `validate_test.js` file to ensure the validation works with both validator implementations

## @rjsf/mui

- Fixed the `README.md` to correct the package name in several places to match the actual package

## @rjsf/utils

- Fixed the `README.md` to remove references to ajv6 validator, adding link to the `utility-functions.md` in the docs
- Fixed the `README.md` to correct the package name in several places to match the actual package
- Updated `getDefaultFormState()` so that oneOf and anyOf default values do not always use the first option when formData contains a better option, fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/2183)

## @rjsf/validator-ajv6

- Fixed the `README.md` to correct the package name in several places to match the actual package

## @rjsf/validator-ajv8

- Support for localization (L10n) on a customized validator using a `Localizer` function passed as a second parameter to `customizeValidator()`, fixing (https://github.com/rjsf-team/react-jsonschema-form/pull/846, and https://github.com/rjsf-team/react-jsonschema-form/issues/1195)
- Fixed the `README.md` to correct the package name in several places to match the actual package

## Dev / docs / playground

- Added two new validator selections, `AJV8` and `AJV8_es` to the list of available validators for the playground; Using the second one will translate error messages to spanish.
- Updated the validation documentation to clarify the case of empty strings being stored as `null` in certain cases.

# v5.0.0-beta.5

## @rjsf/validator-ajv8

- Added the new Ajv 8 based validator so that it can get published on npm

# v5.0.0-beta.4

## @rjsf/semantic-ui

- Switched `devDependencies` for React to 17.x and use `dts` to build and test the library (rather than `tsdx`)

# v5.0.0-beta.3

## @rjsf/core

- Added a `requestSubmit()` call to the `Form.submit()` function, fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/2104, https://github.com/rjsf-team/react-jsonschema-form/issues/3023)
- Added missing `children` property on the `FormProps` type for `Form`
- Throw an error when the required `validator` prop has not been provided to the `Form`

## @rjsf/antd

- Do not show errors if `extraErrors` has `[]` (https://github.com/rjsf-team/react-jsonschema-form/pull/2576).
- Added support for `schema.examples` in the material ui theme fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/2368, https://github.com/rjsf-team/react-jsonschema-form/issues/2557)

## @rjsf/fluent-ui

- Added support for `schema.examples` in the material ui theme fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/2368, https://github.com/rjsf-team/react-jsonschema-form/issues/2557)

## @rjsf/material-ui

- Added support for `schema.examples` in the material ui theme fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/2368, https://github.com/rjsf-team/react-jsonschema-form/issues/2557)

## @rjsf/material-ui

- Added support for `schema.examples` in the material ui theme fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/2368, https://github.com/rjsf-team/react-jsonschema-form/issues/2557)

## @rjsf/semantic-ui

- Upgraded from the `1.x` to `2.x` version of `semantic-ui-react`
- Added support for `schema.examples` in the material ui theme fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/2368, https://github.com/rjsf-team/react-jsonschema-form/issues/2557)

## @rjsf/bootstrap-4

- Avoid importing the whole of `react-icons` (https://github.com/rjsf-team/react-jsonschema-form/pull/3046, https://github.com/react-icons/react-icons/issues/154)

## Dev / docs / playground

- Fixed missing `playground` import error by adding `source-map-loader`
- Fixed up the incorrectly formatted `5.x Migration Guide`
- Added a `Programmatic Submit` button on the playground form to allow users to test the ability to programmatically submit a form
- Regenerated the `package-lock.json` files using clean `node_modules` directories
- Fixed issue with playground controls in top right corner not functioning properly due to missing validator

# v5.0.0-beta.2

- Added peer dependencies to new `@rjsf/utils` library now that it is published on npm

# v5.0.0-beta.1

## Global changes across all themes:

- Node 16 is now the default node engine for all packages, fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/2687)
- Refactored all themes to use the new `@rjsf/utils` library functions and types
- Refactored the individual theme forms to consolidate `templates` as part of the fix for https://github.com/rjsf-team/react-jsonschema-form/issues/2526
  - All the work implementing the `BaseInputTemplate` should fix (https://github.com/rjsf-team/react-jsonschema-form/issues/2926, https://github.com/rjsf-team/react-jsonschema-form/issues/2889, https://github.com/rjsf-team/react-jsonschema-form/issues/2875, https://github.com/rjsf-team/react-jsonschema-form/issues/2223)
  - Also made the display of `title` and `description` consistent across themes, fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/2481, https://github.com/rjsf-team/react-jsonschema-form/issues/2363, https://github.com/rjsf-team/react-jsonschema-form/issues/2219)
  - This change also ensures that all templates are properly exported, resolving (https://github.com/rjsf-team/react-jsonschema-form/issues/2365)
- Bumped most devDependencies to the latest versions where possible
- Switched all repos `package.json` and `package-lock.json` files to be built and maintained by Node 16.
- Adding button templates help to change text for buttons (https://github.com/rjsf-team/react-jsonschema-form/issues/2082, https://github.com/rjsf-team/react-jsonschema-form/issues/2357)

## @rjsf/utils

- New package created by refactoring and converting to Typescript the `utils.js` file from `core` into independent functions.
  - Resolves (https://github.com/rjsf-team/react-jsonschema-form/issues/1655, https://github.com/rjsf-team/react-jsonschema-form/issues/2480, https://github.com/rjsf-team/react-jsonschema-form/issues/2341)
- Updated `types` from `core` in `utils` to better match the implementation across all themes
  - Included adding a bunch of new types for existing and new features
  - The type updates should fix (https://github.com/rjsf-team/react-jsonschema-form/issues/2871, https://github.com/rjsf-team/react-jsonschema-form/issues/2673, https://github.com/rjsf-team/react-jsonschema-form/issues/2347, https://github.com/rjsf-team/react-jsonschema-form/issues/2186)
- Clear errors on `formData` change when `liveOmit=true` when "additionalProperties: false" [issue 1507](https://github.com/rjsf-team/react-jsonschema-form/issues/1507) (https://github.com/rjsf-team/react-jsonschema-form/pull/2631)

## @rjsf/validator-ajv6

- New package created by refactoring and converting to Typescript the `validator.js` file from `core` into independent functions as well as a class that implements the new `ValidatorType` interface.
  - [#2693](https://github.com/rjsf-team/react-jsonschema-form/issues/2693).
- Added support for customizing the options passed to the creation of the `ajv` instance.
- A **BREAKING CHANGE** to `toErrorList()` was made so that it takes `fieldPath: string[]` rather than `fieldName='root'` as part of the fix to (https://github.com/rjsf-team/react-jsonschema-form/issues/1596)
  - The returned `errors` also now adds `property` from the `fieldPath` along with the proper path from the `property` to the `stack` message, making it consistent with the AJV errors.
    - Previously the `stack` attribute would say `root: error message`; now it says `. error message`
  - In addition, the extra information provided by AJV is no longer lost from the `errors` when merged with custom validation, fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/1596).

## @rjsf/core

- Converted core to Typescript (https://github.com/rjsf-team/react-jsonschema-form/issues/583)
- `ui:emptyValue` now works with selects (https://github.com/rjsf-team/react-jsonschema-form/issues/1041)
- Refactoring `utils.js` into the new `@rjsf/utils` fixes (https://github.com/rjsf-team/react-jsonschema-form/issues/2719)
- **BREAKING CHANGE** Fix overriding core submit button className (https://github.com/rjsf-team/react-jsonschema-form/issues/2979)
- Fix `ui:field` with anyOf or oneOf no longer rendered twice (#2890)
- **BREAKING CHANGE** Fixed `anyOf` and `oneOf` getting incorrect, potentially duplicate ids when combined with array (https://github.com/rjsf-team/react-jsonschema-form/issues/2197)
- `formContext` is now passed properly to `SchemaField`, fixes (https://github.com/rjsf-team/react-jsonschema-form/issues/2394, https://github.com/rjsf-team/react-jsonschema-form/issues/2274)
- Added `ui:duplicateKeySuffixSeparator` to customize how duplicate object keys are renamed when using `additionalProperties`.
- The `extraErrors` are now consistently appended onto the end of the schema validation-based `errors` information that is returned via the `onErrors()` callback when submit fails.
  - In addition, the extra information provided by AJV is no longer stripped from the `errors` during the merge process, fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/1596).
- Fixed id generation for `RadioWidget` to no longer use random numbers fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/2461)
- Correctly call the `onChange` handler in the new set of props if it changed, fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/1708).
- Fixed race condition for `onChange` when `formData` is controlled prop, fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/513),

## @rjsf/antd

- Fix esm build to use `@rollup/plugin-replace` to replace `antd/lib` and `rc-picker/lib` with `antd/es` and `rc-picker/es` respectively, fixing (https://github.com/rjsf-team/react-jsonschema-form/issues/2962)

## @rjsf/bootstrap-4

- Bootstrap-4 `withTheme` customizations should work properly now (https://github.com/rjsf-team/react-jsonschema-form/issues/2058)
- `ArrayFieldTemplate` refactor seems to have fixed https://github.com/rjsf-team/react-jsonschema-form/issues/2775
- Fix issues with `SelectField` (https://github.com/rjsf-team/react-jsonschema-form/issues/2616, https://github.com/rjsf-team/react-jsonschema-form/issues/2875)

## @rjsf/chakra-ui

- Properly handle the hidden field in this theme (https://github.com/rjsf-team/react-jsonschema-form/issues/2571)

## @rjsf/material-ui

- The theme for Material UI version 5 (i.e. `@rjsf/mui`) was split out of the theme for version 4 (i.e. `@rjsf/material-ui`) to resolve the following issues:
  - [#2762](https://github.com/rjsf-team/react-jsonschema-form/issues/2762)
  - [#2858](https://github.com/rjsf-team/react-jsonschema-form/issues/2858)
  - [#2905](https://github.com/rjsf-team/react-jsonschema-form/issues/2905)
  - [#2945](https://github.com/rjsf-team/react-jsonschema-form/issues/2945)
  - [#2774](https://github.com/rjsf-team/react-jsonschema-form/issues/2774)
- Material-UI TextWidget now respects `inputType` in uiSchema (https://github.com/rjsf-team/react-jsonschema-form/issues/2057)
  - Also respects `step` for `number` type (https://github.com/rjsf-team/react-jsonschema-form/issues/2488)
- Material-UI UpDownWidget now support min/max/step (https://github.com/rjsf-team/react-jsonschema-form/issues/2022)
- Properly handle the hidden field in this theme (https://github.com/rjsf-team/react-jsonschema-form/issues/2571)
- Select properly accepts true or false (https://github.com/rjsf-team/react-jsonschema-form/issues/2326)

## @rjsf/mui

- The theme for Material UI version 5 (i.e. `@rjsf/mui`) was split out of the theme for version 4 (i.e. `@rjsf/material-ui`) to resolve the following issues:
  - [#2762](https://github.com/rjsf-team/react-jsonschema-form/issues/2762)
  - [#2858](https://github.com/rjsf-team/react-jsonschema-form/issues/2858)
  - [#2905](https://github.com/rjsf-team/react-jsonschema-form/issues/2905)
  - [#2945](https://github.com/rjsf-team/react-jsonschema-form/issues/2945)
  - [#2774](https://github.com/rjsf-team/react-jsonschema-form/issues/2774)
- Material-UI TextWidget now respects `inputType` in uiSchema (https://github.com/rjsf-team/react-jsonschema-form/issues/2057)
  - Also respects `step` for `number` type (https://github.com/rjsf-team/react-jsonschema-form/issues/2488)
- Material-UI UpDownWidget now support min/max/step (https://github.com/rjsf-team/react-jsonschema-form/issues/2022)
- Properly handle the hidden field in this theme (https://github.com/rjsf-team/react-jsonschema-form/issues/2571)

## @rjsf/semantic-ui

- Fix missing error class on fields (https://github.com/rjsf-team/react-jsonschema-form/issues/2666)
- Fixed the `main` definition in `semantic-ui` to fix (https://github.com/withastro/astro/issues/4357)
- Properly handle the hidden field in this theme (https://github.com/rjsf-team/react-jsonschema-form/issues/2571)

## Dev / docs / playground

- Demonstrate use of `ui:field` with `anyOf` (#2890)
- Playground now uses webpack 5
- Corrected number field default (https://github.com/rjsf-team/react-jsonschema-form/issues/2358)

# 4.2.1

- fix typo by @epicfaace in https://github.com/rjsf-team/react-jsonschema-form/pull/2854
- Build all packages with TypeScript, including core by @nickgros in https://github.com/rjsf-team/react-jsonschema-form/pull/2799
- fix(@rjsf/chakra-ui): append SubmitButton by @terrierscript in https://github.com/rjsf-team/react-jsonschema-form/pull/2860
- fix: Pass uiSchema to custom ArrayField by @bakajvo in https://github.com/rjsf-team/react-jsonschema-form/pull/2769
- fix(@rjsf-antd): Submit button type bug (#2867) by @sarpere in https://github.com/rjsf-team/react-jsonschema-form/pull/2869
- Docs: Clarify registry object structure and that it's passed down to custom widgets by @epicfaace in https://github.com/rjsf-team/react-jsonschema-form/pull/2886
- fix: allow UISchemaSubmitButtonOptions properties to be undefined by @maxpou in https://github.com/rjsf-team/react-jsonschema-form/pull/2876
- Create FUNDING.yml by @epicfaace in https://github.com/rjsf-team/react-jsonschema-form/pull/2866
- docs: fix schema dependencies link by @epicfaace in https://github.com/rjsf-team/react-jsonschema-form/pull/2885
- chore(deps): bump core-js-pure from 3.21.1 to 3.23.3 by @dependabot in https://github.com/rjsf-team/react-jsonschema-form/pull/2902
- chore(deps): bump minimist from 1.2.5 to 1.2.6 in /packages/fluent-ui by @dependabot in https://github.com/rjsf-team/react-jsonschema-form/pull/2805
- fix(@rjsf/bootstrap-4): Change custom attribute to bsPrefix by @WillowP in https://github.com/rjsf-team/react-jsonschema-form/pull/3049

# 4.2.0

## @rjsf/core

- Feature for ui:submitButtonOptions on the submit button for forms (https://github.com/rjsf-team/react-jsonschema-form/pull/2640)
- Fix `ui:orderable` and `ui:removable` in arrays (#2797)
- Fix for nested allOf blocks with multiple if/then/else statements failing to render correctly (https://github.com/rjsf-team/react-jsonschema-form/pull/2839)

## Dev / docs / playground

- Enable ui options in playground, to demonstrate submit button options (https://github.com/rjsf-team/react-jsonschema-form/pull/2640)
- Document the `material-ui` context and hook (#2757)

## @rjsf/material-ui

- SubmitButton widget to use new ui:submitButtonOptions on the submit button for forms (https://github.com/rjsf-team/react-jsonschema-form/pull/2833)
- Fixed bundler warning issue (#2762) by exporting a `@rjsf/material-ui/v4` and `@rjsf/material-ui/v5` sub-package
  - NOTE: `@rjsf/material-ui` was retained to avoid a breaking change, but using it will continue to cause bundler warnings
  - See the `README.md` for the `@rjsf/material-ui` package for updated usage information
- Fixed (#2831) for `material-ui` by removing the `DefaultChildren` passed into the themes

## @rjsf/bootstrap-4

- SubmitButton widget to use new ui:submitButtonOptions on the submit button for forms (https://github.com/rjsf-team/react-jsonschema-form/pull/2640)

## @rjsf/semantic-ui

- SubmitButton widget to use new ui:submitButtonOptions on the submit button for forms (https://github.com/rjsf-team/react-jsonschema-form/pull/2640)

## @rjsf/antd

- SubmitButton widget to use new ui:submitButtonOptions on the submit button for forms (https://github.com/rjsf-team/react-jsonschema-form/pull/2640)

## @rjsf/fluent-ui

- SubmitButton widget to use new ui:submitButtonOptions on the submit button for forms (https://github.com/rjsf-team/react-jsonschema-form/pull/2640)

# v4.1.1

## @rjsf/material-ui

- Fix bloated bundle size by individually requiring all MUI components (#2754)
- Add new `useMuiComponent()` hook as a shortcut for `useContext(MuiComponentContext)`

## @rjsf/semantic-ui

- Added support for additionalProperties schema property (#2817)

# v4.1.0

## @rjsf/core

- To improve performance, skip validating subschemas in oneOf / anyOf if formData is undefined (#2676)
- Fixed the `toIdSchema()` typescript definition to add new `idSeparator` prop along with the spelling of `idPrefix`
  - Also passed the new `idSeparator` prop through to the `AnyOfField` and `OneOfField` inside of `SchemaField`
  - Updated `ArrayField` in `@rjsf/core` to pass `idSeparator` and `idPrefix` through to `SchemaField`, fixing a small bug
- Added support for the new `ui:hideError` feature, which allows you to hide errors at a field level

## @rjsf/material-ui

- Remove `console.log()` of the import error in `MaterialUIContext` and `Mui5Context`
- Export the `MaterialComponentContext` (#2724)

## Dev / docs / playground

- Added documentation for the new `ui:hideError` feature

# v4.0.1

- Bumped the peer dependencies of `@rjsf/core` to `^4.0.0` for all of themes in `package.json`
- Also, added tests to all themes to verify that the `tagName` prop works as expected

## @rjsf/core

- Updated `Form` to support the `semantic-ui` and `material-ui` themes to allow them work when `tagName` is provided
- Support if/then/else (#2700)

## @rjsf/material-ui

- Fixed up the `Theme` and `Theme5` implementations to deal with a regression in which adding `tagName` caused the 2 themes to not work
- Only `console.log()` the import error in `MaterialUIContext` and `Mui5Context` when not in `production` to eliminate tons of warnings for released code

## @rjsf/semantic-ui

- Fixed up the `Theme` implementation to deal with a regression in which adding `tagName` caused the theme to not work

# v4.0.0

## @rjsf/core

- Add React 17 as a supported peer-dependency
- Introduce `idSeparator` prop to change the path separator used to generate field names (https://github.com/rjsf-team/react-jsonschema-form/pull/2628)
- Array fields support custom widgets (previously, only multiple-choice arrays with `enums` or `uniqueItems` support it) (https://github.com/rjsf-team/react-jsonschema-form/pull/2697)

## @rjsf/material-ui

- Added React 17 as an optional peer dependency
- Minimum version of React required to use package is now React 16.3
- Bumped required minimum versions of `@material-ui/core` and `@material-ui/icons` to the latest (`4.12.0` and `4.11.1`)
  - New exports: `MuiForm4` and `Theme4` are aliases to the material-ui version 4 `MuiForm` and `Theme`
  - The Material-UI 4 theme will fallback to a form with a message indicating `@material-ui` is not available when one (or both) of the libraries are not installed
- Added support for material-ui version 5 on top of React 17
  - Requires React 17 so will need to upgrade project
  - Added `@mui/material`, `@mui/icons-material`, `@emotion/react` and `@emotion/styled` as optional peer dependencies
  - New exports: `MuiForm5` and `Theme5` support using the Material UI 5 libraries instead of version 4
  - The Material-UI 5 theme will fallback to a form with a message indicating `@mui` is not available when one (or both) of the libraries are not installed

## @rjsf/chakra-ui

- Added support for this new theme

## Dev / docs / playground

- Upgraded playground to use React 17
- Differentiated the material-ui 4 and 5 themes
- Added chakra-ui theme

# v3.3.0

## @rjsf/semantic-ui

- "semantic-ui-react" dependency updated to v1.3.1 (https://github.com/rjsf-team/react-jsonschema-form/pull/2590)
- fixed an issue where all semantic props overwritten when a single [semantic theme-specific prop](https://rjsf-team.github.io/react-jsonschema-form/docs/api-reference/themes/semantic-ui/uiSchema/) is passed in ([issue 2619](https://github.com/rjsf-team/react-jsonschema-form/issues/2619)) (https://github.com/rjsf-team/react-jsonschema-form/pull/2590)

# v3.2.1

## @rjsf/core

- Don't crash when non-object formData is passed in to a schema item with additionalProperties (https://github.com/rjsf-team/react-jsonschema-form/pull/2595)
- Upgrade jsonpointer to 5.0.0 to address security vulnerability (https://github.com/rjsf-team/react-jsonschema-form/pull/2599)
- Feature for ui:submitButtonOptions on the submit button for forms (https://github.com/rjsf-team/react-jsonschema-form/pull/2640)

# v3.2.0

## @rjsf/core

- Fix for clearing errors after updating and submitting form (https://github.com/rjsf-team/react-jsonschema-form/pull/2536)
- bootstrap-4 TextWidget wrappers now pull from registry, add rootSchema to Registry, fix FieldProps.onFocus type to match WidgetProps (https://github.com/rjsf-team/react-jsonschema-form/pull/2519)
- Added global `readonly` flag to the `Form` (https://github.com/rjsf-team/react-jsonschema-form/pull/2554)
- Fix to allow changing `additionalProperties` to falsy values (https://github.com/rjsf-team/react-jsonschema-form/pull/2540)
- Pass uiSchema to custom Boolean widget (https://github.com/rjsf-team/react-jsonschema-form/pull/2587

## @rjsf/bootstrap-4

- bootstrap-4 TextWidget wrappers now pull from registry, add rootSchema to Registry, fix FieldProps.onFocus type to match WidgetProps (https://github.com/rjsf-team/react-jsonschema-form/pull/2519)

## @rjsf/fluent-ui

- fluent-ui: Allow value of 0 in TextWidget (https://github.com/rjsf-team/react-jsonschema-form/pull/2497)

## Dev / docs / playground

- Several dependency updates
- Added global `readonly` flag to the `Form` (https://github.com/rjsf-team/react-jsonschema-form/pull/2554)
- Enable source maps in playground, for development (https://github.com/rjsf-team/react-jsonschema-form/pull/2568)

# v3.1.0

## @rjsf/core

- Properly assign label prop for MultiSelect ArrayField (https://github.com/rjsf-team/react-jsonschema-form/pull/2459)
- Take into account implicitly defined types when rendering labels for fields (https://github.com/rjsf-team/react-jsonschema-form/pull/2502)

## @rjsf/antd

- Add default Form export to @rjsf/antd (https://github.com/rjsf-team/react-jsonschema-form/pull/2514)

## @rjsf/fluent-ui

- Make material-ui and fluent-ui pull TextWidget from the registry; remove registry prop from <div> in TextWidget (https://github.com/rjsf-team/react-jsonschema-form/pull/2515)

## @rjsf/material-ui

- Make material-ui and fluent-ui pull TextWidget from the registry; remove registry prop from <div> in TextWidget (https://github.com/rjsf-team/react-jsonschema-form/pull/2515)

## @rjsf/semantic-ui

- Use getDisplayLabel to properly show labels for widgets (https://github.com/rjsf-team/react-jsonschema-form/pull/2225)
- Add submit button, email, url, date widgets (https://github.com/rjsf-team/react-jsonschema-form/pull/2224)

## Dev / docs / playground

- Several dependency updates
