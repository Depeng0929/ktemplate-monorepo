1. replace name in packages.json
2. config tsconfig

```ts
"paths": {
  "@slidev/client/*": ["./packages/client/*"],
  "@slidev/types": ["./packages/types/src/index.ts"],
  "@slidev/parser": ["./packages/parser/src/index.ts"],
  "@slidev/parser/fs": ["./packages/parser/src/fs.ts"],
}
```

3. config sub package.json, add devDependencies

```ts
"@slidev/cli": "workspace:*",
```


4. config types sub
```json
  "main": "dist/index.js",
  "module": "dist/index.mjs",
  "types": "index.d.ts",
  "files": [
    "dist",
    "index.d.ts"
  ],
  "scripts": {
    "build": "tsup src/index.ts",
    "dev": "nr build --watch",
    "prepublishOnly": "npm run build"
  }
```

5. delete sub .eslintrc and package.json eslint dependencies

