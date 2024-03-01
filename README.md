## Neptune Mutual ESLint Packages
Currently, the packages are hosted with the prefix of `eslint-config-neptunemutual-`, which will later be changed to `eslint-config-neptune-`

## ESLint Config Core

```
yarn add -D eslint eslint-config-neptunemutual-core
```

Now create a `.eslintrc.json` file in the root of the project with the following content.

```
{
  "extends": "neptunemutual-core"
}
```

## ESLint Config Next

```
yarn add -D eslint eslint-config-neptunemutual-next
```

Now create a `.eslintrc.json` file in the root of the project with the following content.

```
{
  "extends": "neptunemutual-next"
}
```

## ESLint Config Typescript

Make sure you have `typescript` as the devDependency of the project.

### For Node/Typescipt:

```
yarn add -D eslint eslint-config-neptunemutual-core eslint-config-neptunemutual-typescript
```

And `.eslintrc.json` will be:

```
{
  "extends": ["neptunemutual-core", "neptunemutual-typescript"]
}
```

### For Next/Typescipt:

```
yarn add -D eslint eslint-config-neptunemutual-next eslint-config-neptunemutual-typescript
```

And `.eslintrc.json` will be:

```
{
  "extends": ["neptunemutual-next", "neptunemutual-typescript"]
}
```

## VS Code Auto Format On Save

Make sure you have `ESLint` Extension added to your VS Code

In `settings.json`:

```
{
  "editor.formatOnSave": true,
  "[javascript]": {
    "editor.formatOnSave": false
  },
  "editor.codeActionsOnSave": {
      "source.fixAll.eslint": true
  },
  "eslint.workingDirectories": [
    "./folder-1",
    "./folder-2",
    "./folder-3"
  ]
}
```

Note: `eslint.workingDirectories` is only required for mono-repo style projects where multiple eslint configurations confuse the ESLint VS Code Extension

## Publishing Steps

Change the version in the corresponding `package.json` file of the package you'd like to publish.

```
cd [package_folder_name]
npm publish
```
