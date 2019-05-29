# sync-json-firestore

A Node.js script that help you **sync** your json with Firestore database.

## **IMPORTANT!** 
Dont forget to add `firebaseConfig.js` and `serviceAccount.json` to your .gitignore

## 1. JSON File 

**Note:** JSON file must be object with **'key'** because Firebase Cloud Firestore must have a **'collection'** in the root of the project of yout database.

```json
{
  "collection_name_required": {
    "document_name_optional": {
      "hello": "world"
    }
  }
}
```

## 2. Get firebaseConfig

1. From your [Firebase Console ](https://console.firebase.google.com), select your project, then click `Project Overview` -> `</>`
2. Copy and paste the `firebaseConfig` in `firebaseConfig.js`

```js
// Firebase Config
const firebaseConfig = {
  apiKey: "API_KEY_HERE",
  authDomain: "AUTH_DOMAIN_HERE",
  databaseURL: "DATABASE_URL_HERE",
  projectId: "PROJECT_ID_HERE",
  storageBucket: "STORAGE_BUCKET_HERE",
  messagingSenderId: "MESSAGING_ID_HERE"
}
// Exports
module.exports = firebaseConfig;
```

## 3. Firebase Service Account

1. From your [Firebase Console ](https://console.firebase.google.com), select your project, then click `Settings (gear icon)` -> `Users and Permissions` -> `Service accounts`
2. Choose `Node.js` in Admin SDK configuration snippet and click `Generate a new private key`
3. Copy the downloaded file in this project root directory and rename it as `serviceAccount.json`


## 4. Build Setup
``` bash
# install dependencies
$ npm install
```

## 5. Sync it your Firestore
```bash
$ npm start
```