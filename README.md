From version 5.1.5 I get errors building my typescript project due to multiple versions of @types/react.  I'm not sure if this is a problem with html-react-parser or with @types/react.

See https://github.com/remarkablemark/html-react-parser/commit/78b7a8e8a52b23676a5d86ef60ee9c57683839e3 and https://github.com/remarkablemark/html-react-parser/issues/1320

```
git clone git@github.com:captain-igloo/html-react-parser-bug.git
cd html-react-parser-bug
npm ci
npm run build
```

Error:

```
node_modules/@types/react/index.d.ts:4127:14 - error TS2300: Duplicate identifier 'ElementType'.

4127         type ElementType = string | React.JSXElementConstructor<any>;
                  ~~~~~~~~~~~

  node_modules/html-react-parser/node_modules/@types/react/index.d.ts:4127:14
    4127         type ElementType = string | React.JSXElementConstructor<any>;
                      ~~~~~~~~~~~
    'ElementType' was also declared here.

node_modules/@types/react/index.d.ts:4141:14 - error TS2300: Duplicate identifier 'LibraryManagedAttributes'.

4141         type LibraryManagedAttributes<C, P> = C extends
                  ~~~~~~~~~~~~~~~~~~~~~~~~

  node_modules/html-react-parser/node_modules/@types/react/index.d.ts:4141:14
    4141         type LibraryManagedAttributes<C, P> = C extends
                      ~~~~~~~~~~~~~~~~~~~~~~~~
    'LibraryManagedAttributes' was also declared here.

node_modules/html-react-parser/node_modules/@types/react/index.d.ts:4127:14 - error TS2300: Duplicate identifier 'ElementType'.

4127         type ElementType = string | React.JSXElementConstructor<any>;
                  ~~~~~~~~~~~

  node_modules/@types/react/index.d.ts:4127:14
    4127         type ElementType = string | React.JSXElementConstructor<any>;
                      ~~~~~~~~~~~
    'ElementType' was also declared here.

node_modules/html-react-parser/node_modules/@types/react/index.d.ts:4141:14 - error TS2300: Duplicate identifier 'LibraryManagedAttributes'.

4141         type LibraryManagedAttributes<C, P> = C extends
                  ~~~~~~~~~~~~~~~~~~~~~~~~

  node_modules/@types/react/index.d.ts:4141:14
    4141         type LibraryManagedAttributes<C, P> = C extends
                      ~~~~~~~~~~~~~~~~~~~~~~~~
    'LibraryManagedAttributes' was also declared here.
```
