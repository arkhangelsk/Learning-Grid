## How to dynamically access object property using a variable?

```
    const serviceName = 'GeoLoc';
    const _baseURI = `baseURI${serviceName}`;
    const _path =  `path${serviceName}`;
    const _header = `header${serviceName}`;
    
    const baseURI = apidata[_baseURI];              
    const path = apidata[_path];
    const header = apidata[_header];    //here we want to get data apidata.headerGeoLoc
    
    let postParam = {
    header: header,
    endpoint: baseURI + path 
    }
```