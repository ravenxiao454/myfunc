# myfunc

## 1.js_stream_load_sqlite
### description
#### rewrite in javascript from the python version of "stream_sqlite" 
#### it can scan rows while request pending,but the output rows isn't ordered
#### usage
```
  const r = await fetch('/test.db')
  var reqit = await iter_request(r.body.getReader(),65536)
  var dbit = await iter_dbchunks(reqit,null)   //the second param could be a callback function
  var dbnext = await dbit.next()
  while (!dbnext.done){
      console.log(dbva.value)
      dbval = await dbit.next()
  }
```
