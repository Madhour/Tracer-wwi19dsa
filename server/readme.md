Backend w/ Deno
====== 

to run the server use: __deno run --allow-net --allow-read --allow-write --allow-env --unstable ./server/src/backendServer.ts__
→ server runs on __localhost:3000__

Note: You need to have a (local) mySQL DB running: __mysql -u root -p__

Dependencies 
------

1. Opine
2. Jsonfile
3. cuid
4. [Localbase](https://github.com/dannyconnell/localbase)
5. Jquery

1_Log_New_Scan
------

- [x] set locID & timestamp
- [x] store locID & timestamp in ~~./databases/LocalBuffer.json~~ [indexedDB](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API) database
- [x] send locID & timestamp via url (get)
- [x] generate cuid
- [x] store locID, cuid & timestamp in ./databases/GlobalDatabase.json
- [x] return cuid to client
- [x] store data in indexedDB database first and clear entry after response from server (offline functionality)

<img src="./ressources/TracerDB_demo.gif" width="750"/>


____