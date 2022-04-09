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
