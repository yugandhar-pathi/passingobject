### Send Data Across Tabs

`Pre-requisite :- Both sender and receiver should be on the same domain.`

### `window.open` method

`window.open` method returns an reference to the receiver object.

```js
function sendData() {
  let windowReference = window.open('./receiver.html');
  windowReference.dataSent = { author: 'pathi' };
}
```

Whatever we add to the `windowReference` can be accessed in the receiver html.

```js
let data = window.dataSent;
document.getElementById('para').innerHTML = data.author;
```
