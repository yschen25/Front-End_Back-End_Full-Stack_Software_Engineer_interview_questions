## Web Interview Questions

      This document is provided to who wants to prepare front-end interview
      so it doesn't explain the concepts deeply, if you need more details please google it. 
<br/>

1. What Is The Difference Between Session, Cookie, Sessionstorage, Localstorage?

| Type |  Session |  Cookie |  Sessionstorage |  Localstorage | 
|---|---|---|---|---|
| Expired Time  | It can set the expire time | Its expiration varies based on the type and the expiration duration can be set from either server-side or client-side  | The data clear automatically when the browser is closed | The data **WILL NOT** be deleted when the browser is closed until user clear through JavaScript, browser cache / locally stored data |
| Storage  | 1024KB |  4KB | 5MB | 5MB  |
| Storing Location | storing on server-side   | storing on client-side and server-side | storing on client-side | storing on client-side |
| Request |   | The data is sent back to the server for every HTTP request | The data is **NOT** sent back to the server for every HTTP request | The data is **NOT** sent back to the server for every HTTP request |
<br/>
