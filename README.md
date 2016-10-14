To avoid error add:

edit:
`commonjs()` line 40 of node_modules/@ionic/app-scripts/config/rollup.config.js
to
`commonjs({
  namedExports: {
    'node_modules/angular2-progressbar/dist/index.js':['CircleProgressComponent', 'ProgressBarModule']
  }
}),`

When running `ionic build ios` i get the error:
`ngc: Error: Unexpected value 'ProgressBarModule' imported by the module 'AppModule'`
