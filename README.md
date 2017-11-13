# firebase_image_upload

Simple example of how to upload files to firebase storage


## Use
Change the config object in index.html to your own firebase project to use. 

Authentication has NOT been added so this requires your firebase rules to be set as follows in order to work

```
service firebase.storage {
  match /b/{bucket}/o {
    match /{allPaths=**} {
      allow read, write: if true;
    }
  }
}
```

That's it.