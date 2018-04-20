# Graph Panel

Webpack copy of [Grafana default panel](http://docs.grafana.org/features/panels/graph/). 
Now you can make your plugins based on graph panel and hack it easier.
Work only on Grafana versions >= V5.0.1

# Build

```
npm install
npm run build
```

# After you fork

Sorry, but it's common for Grafana plugins make directives which collides with each other. It comes from AngularJS.
Use `ctrl+f` to find params ic source code.

* Change in `plugin.json` id from `graph-panel-template-panel` to `something-else-graph-panel`
* Change in `src/graph.ts` directive name from `grafanaTemplateGraph` to `somethingElseGraph`
* Change in `src/legend.ts` directive name from `graphTemplateLegend` to `somethingElseLegend`
* Change in `src/axes_editor` param `templateUrl` param from `public/plugins/graph-panel-template-panel/partials/axes_editor.html` to `public/plugins/something-else-graph-panel/partials/axes_editor.html`
* Change in `template.ts` param `grafana-template-graph` to `something-else-graph` and `graph-template-legend` to `something-else-legend`
* in case you debug with VSCode, change in `.vscode/launch.json` param `/public/plugins/graph-panel-template-panel` to `/public/plugins/something-else-graph-panel`

# Credits

Based on 

* [grafana-plugin-template-webpack-typescript](https://github.com/CorpGlory/grafana-plugin-template-webpack-typescript) 
* [@types/grafana](https://github.com/CorpGlory/types-grafana)
