# Altering the Bare Pattern Lab Front End

## Developing Locally

The best way to make changes to this repo and test them is through your existing edition.

``` sh
cd uikit-bare
npm link
cd path/to/your/edition
npm link uikit-bare
```

Add the uikit as another entry within `patternlab-config.json`. The name of your package must match the name of the key.

``` diff
  "uikits": [
    {
      "name": "uikit-workshop",
-      "outputDir": "",
+      "outputDir": "workshop",
      "enabled": true,
      "excludedPatternStates": [],
      "excludedTags": []
-    }
+    },
+    {
+      "name": "uikit-bare",
+      "outputDir": "bare",
+      "enabled": true,
+      "excludedPatternStates": [],
+      "excludedTags": []
+    }
  ]
```

## Running and Making Changes

`npm start` will compile and watch the SCSS files within `./source`

All other templates (in `./views`) and Javascript (in `./dist`) can be edited directly. `./dist/index.html` contains the entry point of the UIKit's HTML, gluing it all together.

