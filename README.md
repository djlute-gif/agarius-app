{
  "name": "agarius-app",
  "version": "3.0.0",
  "description": "AGARIUS — Resonancia Total",
  "main": "index.js",
  "scripts": {
    "build": "echo 'Static app, no build needed'",
    "cap:add": "npx cap add android",
    "cap:sync": "npx cap sync android",
    "cap:open": "npx cap open android",
    "apk": "cd android && ./gradlew assembleDebug"
  },
  "dependencies": {
    "@capacitor/android": "^5.7.0",
    "@capacitor/core": "^5.7.0"
  },
  "devDependencies": {
    "@capacitor/cli": "^5.7.0"
  }
}
