# AngularCordova

1. Cordova create NAME
2. cd NAME
3. Create `build.json` in the cordova app folder with:
  {
  "ios": {
      "developmentTeam": "NAME",
      "debug": {
          "buildFlag": ["-UseModernBuildSystem=0"]
      },
      "release": {
          "buildFlag": ["-UseModernBuildSystem=0"]
      }
  }
}

4. Build the angular project and move output into NAME/www
 - ng build --prod --base-href . --output-path ../NAME/www
5. open `index.html` inside the www folder
6. Add `<script type=”text/javascript” src=”cordova.js”></script>`
7. `cordova platform add ios`
8. `cordova run ios  --target="iPhone-8”`
