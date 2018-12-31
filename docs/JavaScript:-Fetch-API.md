## Using JavaScript fetch() to make GET and POST requests:

**Get Request:**

* Fetch API is a replacement for XMLHttpRequest
* It is a web API that can be used to create requests.
* Once fetch is called, it will return promises.
* To handle promises returned by fetch(), we chain .then() methods
* The .json() method converts a returned promise to a JSON object.

```javascript
fetch('https://api-url-goes-here.com/endpoint').then(response => {
  if(response.ok){
    return response.json();
  }
  throw new Error('Request failed!');
}, networkError => {
  console.log(networkError.message);
}).then(jsonResponse => {
  return jsonResponse;
});
```

**Post Request:**

Fetch POST call takes two arguments
1. An endpoint of the API
2. An object that contains information needed for the POST request

```javascript
fetch('https://api-url-goes-here.com/endpoint', {
  method: 'POST',
  body: JSON.stringify({id: '200'})
}).then(response => {
  if(response.ok){
    return response.json();
  }
  throw new Error('Request failed!');
}, networkError => {
  console.log(networkError.message);
}).then(jsonResponse => {
  return jsonResponse;
});
```

**async/await Get Request:**

```javascript
const getData = async () => {
   try {
     const response = await fetch('https://api-url-goes-here.com/endpoint');
     if(response.ok){
     const jsonResponse = await response.json();
       return jsonResponse;
    }
     throw new Error('Request failed!');
  } catch (error){
    console.log(error);
  }
}
```

**async/await Post Request:**

```javascript
const getData = async () => {
  try{
    const response = await fetch('https://api-url-goes-here.com/endpoint', {
      method: 'POST',
      body: JSON.stringify({id: 200}) 
    });
    if (response.ok){
      const jsonResponse = await response.json();
      return jsonResponse;
    }
    throw new Error('Request failed!');
  } catch (error){
    console.log(error);
  }
}
```
