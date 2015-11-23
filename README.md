# Uploading Images as Base 64 via File Reader

* Using the Javascript FileReader API, we can upload images as Base64 strings.
* We log out the base64 string via the `event` in `line:67` of `index.html`.
* All FileReader related elements and code are contained in the `index.html` file.
* This project contains the MUI CSS framework and corresponding libraries.

## Code Behind This

```javascript
var reader = new FileReader();
reader.onload = function (event) {
  // try to read whatever file has been 'readAsDataURL'
  try {
    // event target result is our base64 encoded type
    // this is whatever file has been reader during 'readAsDataURL'
    console.log("File as base 64:");
    console.log(event.target.result);
    // catch an error if one occurs...
  } catch (ex) {
    // output a warning in the DevTools console
    throw new Error("Couldn't convert file: " + ex);
  }
}
// read the file argument
reader.readAsDataURL(binaryData);
```
