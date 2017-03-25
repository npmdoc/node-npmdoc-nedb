# api documentation for  [nedb (v1.8.0)](https://github.com/louischatriot/nedb)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-nedb.svg)](https://travis-ci.org/npmdoc/node-npmdoc-nedb)
#### File-based embedded data store for node.js

[![NPM](https://nodei.co/npm/nedb.png?downloads=true)](https://www.npmjs.com/package/nedb)

[![apidoc](https://npmdoc.github.io/node-npmdoc-nedb/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-nedb_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-nedb/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-nedb/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "Louis Chatriot",
        "email": "louis.chatriot@gmail.com"
    },
    "browser": {
        "./lib/customUtils.js": "./browser-version/browser-specific/lib/customUtils.js",
        "./lib/storage.js": "./browser-version/browser-specific/lib/storage.js"
    },
    "bugs": {
        "url": "https://github.com/louischatriot/nedb/issues"
    },
    "contributors": [
        {
            "name": "Louis Chatriot"
        }
    ],
    "dependencies": {
        "async": "0.2.10",
        "binary-search-tree": "0.2.5",
        "localforage": "^1.3.0",
        "mkdirp": "~0.5.1",
        "underscore": "~1.4.4"
    },
    "description": "File-based embedded data store for node.js",
    "devDependencies": {
        "chai": "^3.2.0",
        "commander": "1.1.1",
        "exec-time": "0.0.2",
        "mocha": "1.4.x",
        "request": "2.9.x",
        "sinon": "1.3.x"
    },
    "directories": {},
    "dist": {
        "shasum": "0e3502cd82c004d5355a43c9e55577bd7bd91d88",
        "tarball": "https://registry.npmjs.org/nedb/-/nedb-1.8.0.tgz"
    },
    "gitHead": "1695426cd93e4639d4a379efd039b5bf9a7ba789",
    "homepage": "https://github.com/louischatriot/nedb",
    "keywords": [
        "database",
        "datastore",
        "embedded"
    ],
    "license": "SEE LICENSE IN LICENSE",
    "main": "index",
    "maintainers": [
        {
            "name": "louischatriot",
            "email": "louis.chatriot@gmail.com"
        }
    ],
    "name": "nedb",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/louischatriot/nedb.git"
    },
    "scripts": {
        "test": "mocha --reporter spec --timeout 10000"
    },
    "version": "1.8.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module nedb](#apidoc.module.nedb)
1.  [function <span class="apidocSignatureSpan">nedb.</span>cursor (db, query, execFn)](#apidoc.element.nedb.cursor)
1.  [function <span class="apidocSignatureSpan">nedb.</span>executor ()](#apidoc.element.nedb.executor)
1.  [function <span class="apidocSignatureSpan">nedb.</span>indexes (options)](#apidoc.element.nedb.indexes)
1.  [function <span class="apidocSignatureSpan">nedb.</span>persistence (options)](#apidoc.element.nedb.persistence)
1.  [function <span class="apidocSignatureSpan">nedb.</span>super_ ()](#apidoc.element.nedb.super_)
1.  object <span class="apidocSignatureSpan">nedb.</span>cursor.prototype
1.  object <span class="apidocSignatureSpan">nedb.</span>customUtils
1.  object <span class="apidocSignatureSpan">nedb.</span>executor.prototype
1.  object <span class="apidocSignatureSpan">nedb.</span>indexes.prototype
1.  object <span class="apidocSignatureSpan">nedb.</span>model
1.  object <span class="apidocSignatureSpan">nedb.</span>persistence.prototype
1.  object <span class="apidocSignatureSpan">nedb.</span>storage

#### [module nedb.cursor](#apidoc.module.nedb.cursor)
1.  [function <span class="apidocSignatureSpan">nedb.</span>cursor (db, query, execFn)](#apidoc.element.nedb.cursor.cursor)

#### [module nedb.cursor.prototype](#apidoc.module.nedb.cursor.prototype)
1.  [function <span class="apidocSignatureSpan">nedb.cursor.prototype.</span>_exec (_callback)](#apidoc.element.nedb.cursor.prototype._exec)
1.  [function <span class="apidocSignatureSpan">nedb.cursor.prototype.</span>exec ()](#apidoc.element.nedb.cursor.prototype.exec)
1.  [function <span class="apidocSignatureSpan">nedb.cursor.prototype.</span>limit (limit)](#apidoc.element.nedb.cursor.prototype.limit)
1.  [function <span class="apidocSignatureSpan">nedb.cursor.prototype.</span>project (candidates)](#apidoc.element.nedb.cursor.prototype.project)
1.  [function <span class="apidocSignatureSpan">nedb.cursor.prototype.</span>projection (projection)](#apidoc.element.nedb.cursor.prototype.projection)
1.  [function <span class="apidocSignatureSpan">nedb.cursor.prototype.</span>skip (skip)](#apidoc.element.nedb.cursor.prototype.skip)
1.  [function <span class="apidocSignatureSpan">nedb.cursor.prototype.</span>sort (sortQuery)](#apidoc.element.nedb.cursor.prototype.sort)

#### [module nedb.customUtils](#apidoc.module.nedb.customUtils)
1.  [function <span class="apidocSignatureSpan">nedb.customUtils.</span>uid (len)](#apidoc.element.nedb.customUtils.uid)

#### [module nedb.executor](#apidoc.module.nedb.executor)
1.  [function <span class="apidocSignatureSpan">nedb.</span>executor ()](#apidoc.element.nedb.executor.executor)

#### [module nedb.executor.prototype](#apidoc.module.nedb.executor.prototype)
1.  [function <span class="apidocSignatureSpan">nedb.executor.prototype.</span>processBuffer ()](#apidoc.element.nedb.executor.prototype.processBuffer)
1.  [function <span class="apidocSignatureSpan">nedb.executor.prototype.</span>push (task, forceQueuing)](#apidoc.element.nedb.executor.prototype.push)

#### [module nedb.indexes](#apidoc.module.nedb.indexes)
1.  [function <span class="apidocSignatureSpan">nedb.</span>indexes (options)](#apidoc.element.nedb.indexes.indexes)

#### [module nedb.indexes.prototype](#apidoc.module.nedb.indexes.prototype)
1.  [function <span class="apidocSignatureSpan">nedb.indexes.prototype.</span>getAll ()](#apidoc.element.nedb.indexes.prototype.getAll)
1.  [function <span class="apidocSignatureSpan">nedb.indexes.prototype.</span>getBetweenBounds (query)](#apidoc.element.nedb.indexes.prototype.getBetweenBounds)
1.  [function <span class="apidocSignatureSpan">nedb.indexes.prototype.</span>getMatching (value)](#apidoc.element.nedb.indexes.prototype.getMatching)
1.  [function <span class="apidocSignatureSpan">nedb.indexes.prototype.</span>insert (doc)](#apidoc.element.nedb.indexes.prototype.insert)
1.  [function <span class="apidocSignatureSpan">nedb.indexes.prototype.</span>insertMultipleDocs (docs)](#apidoc.element.nedb.indexes.prototype.insertMultipleDocs)
1.  [function <span class="apidocSignatureSpan">nedb.indexes.prototype.</span>remove (doc)](#apidoc.element.nedb.indexes.prototype.remove)
1.  [function <span class="apidocSignatureSpan">nedb.indexes.prototype.</span>reset (newData)](#apidoc.element.nedb.indexes.prototype.reset)
1.  [function <span class="apidocSignatureSpan">nedb.indexes.prototype.</span>revertUpdate (oldDoc, newDoc)](#apidoc.element.nedb.indexes.prototype.revertUpdate)
1.  [function <span class="apidocSignatureSpan">nedb.indexes.prototype.</span>update (oldDoc, newDoc)](#apidoc.element.nedb.indexes.prototype.update)
1.  [function <span class="apidocSignatureSpan">nedb.indexes.prototype.</span>updateMultipleDocs (pairs)](#apidoc.element.nedb.indexes.prototype.updateMultipleDocs)

#### [module nedb.model](#apidoc.module.nedb.model)
1.  [function <span class="apidocSignatureSpan">nedb.model.</span>areThingsEqual (a, b)](#apidoc.element.nedb.model.areThingsEqual)
1.  [function <span class="apidocSignatureSpan">nedb.model.</span>checkObject (obj)](#apidoc.element.nedb.model.checkObject)
1.  [function <span class="apidocSignatureSpan">nedb.model.</span>compareThings (a, b, _compareStrings)](#apidoc.element.nedb.model.compareThings)
1.  [function <span class="apidocSignatureSpan">nedb.model.</span>deepCopy (obj, strictKeys)](#apidoc.element.nedb.model.deepCopy)
1.  [function <span class="apidocSignatureSpan">nedb.model.</span>deserialize (rawData)](#apidoc.element.nedb.model.deserialize)
1.  [function <span class="apidocSignatureSpan">nedb.model.</span>getDotValue (obj, field)](#apidoc.element.nedb.model.getDotValue)
1.  [function <span class="apidocSignatureSpan">nedb.model.</span>isPrimitiveType (obj)](#apidoc.element.nedb.model.isPrimitiveType)
1.  [function <span class="apidocSignatureSpan">nedb.model.</span>match (obj, query)](#apidoc.element.nedb.model.match)
1.  [function <span class="apidocSignatureSpan">nedb.model.</span>modify (obj, updateQuery)](#apidoc.element.nedb.model.modify)
1.  [function <span class="apidocSignatureSpan">nedb.model.</span>serialize (obj)](#apidoc.element.nedb.model.serialize)

#### [module nedb.persistence](#apidoc.module.nedb.persistence)
1.  [function <span class="apidocSignatureSpan">nedb.</span>persistence (options)](#apidoc.element.nedb.persistence.persistence)
1.  [function <span class="apidocSignatureSpan">nedb.persistence.</span>ensureDirectoryExists (dir, cb)](#apidoc.element.nedb.persistence.ensureDirectoryExists)
1.  [function <span class="apidocSignatureSpan">nedb.persistence.</span>getNWAppFilename (appName, relativeFilename)](#apidoc.element.nedb.persistence.getNWAppFilename)

#### [module nedb.persistence.prototype](#apidoc.module.nedb.persistence.prototype)
1.  [function <span class="apidocSignatureSpan">nedb.persistence.prototype.</span>compactDatafile ()](#apidoc.element.nedb.persistence.prototype.compactDatafile)
1.  [function <span class="apidocSignatureSpan">nedb.persistence.prototype.</span>loadDatabase (cb)](#apidoc.element.nedb.persistence.prototype.loadDatabase)
1.  [function <span class="apidocSignatureSpan">nedb.persistence.prototype.</span>persistCachedDatabase (cb)](#apidoc.element.nedb.persistence.prototype.persistCachedDatabase)
1.  [function <span class="apidocSignatureSpan">nedb.persistence.prototype.</span>persistNewState (newDocs, cb)](#apidoc.element.nedb.persistence.prototype.persistNewState)
1.  [function <span class="apidocSignatureSpan">nedb.persistence.prototype.</span>setAutocompactionInterval (interval)](#apidoc.element.nedb.persistence.prototype.setAutocompactionInterval)
1.  [function <span class="apidocSignatureSpan">nedb.persistence.prototype.</span>stopAutocompaction ()](#apidoc.element.nedb.persistence.prototype.stopAutocompaction)
1.  [function <span class="apidocSignatureSpan">nedb.persistence.prototype.</span>treatRawData (rawData)](#apidoc.element.nedb.persistence.prototype.treatRawData)

#### [module nedb.storage](#apidoc.module.nedb.storage)
1.  [function <span class="apidocSignatureSpan">nedb.storage.</span>appendFile (path, data, options, callback_)](#apidoc.element.nedb.storage.appendFile)
1.  [function <span class="apidocSignatureSpan">nedb.storage.</span>crashSafeWriteFile (filename, data, cb)](#apidoc.element.nedb.storage.crashSafeWriteFile)
1.  [function <span class="apidocSignatureSpan">nedb.storage.</span>ensureDatafileIntegrity (filename, callback)](#apidoc.element.nedb.storage.ensureDatafileIntegrity)
1.  [function <span class="apidocSignatureSpan">nedb.storage.</span>ensureFileDoesntExist (file, callback)](#apidoc.element.nedb.storage.ensureFileDoesntExist)
1.  [function <span class="apidocSignatureSpan">nedb.storage.</span>exists (path, callback)](#apidoc.element.nedb.storage.exists)
1.  [function <span class="apidocSignatureSpan">nedb.storage.</span>flushToStorage (options, callback)](#apidoc.element.nedb.storage.flushToStorage)
1.  [function <span class="apidocSignatureSpan">nedb.storage.</span>mkdirp (p, opts, f, made)](#apidoc.element.nedb.storage.mkdirp)
1.  [function <span class="apidocSignatureSpan">nedb.storage.</span>readFile (path, options, callback_)](#apidoc.element.nedb.storage.readFile)
1.  [function <span class="apidocSignatureSpan">nedb.storage.</span>rename (oldPath, newPath, callback)](#apidoc.element.nedb.storage.rename)
1.  [function <span class="apidocSignatureSpan">nedb.storage.</span>unlink (path, callback)](#apidoc.element.nedb.storage.unlink)
1.  [function <span class="apidocSignatureSpan">nedb.storage.</span>writeFile (path, data, options, callback_)](#apidoc.element.nedb.storage.writeFile)



# <a name="apidoc.module.nedb"></a>[module nedb](#apidoc.module.nedb)

#### <a name="apidoc.element.nedb.cursor"></a>[function <span class="apidocSignatureSpan">nedb.</span>cursor (db, query, execFn)](#apidoc.element.nedb.cursor)
- description and source-code
```javascript
function Cursor(db, query, execFn) {
  this.db = db;
  this.query = query || {};
  if (execFn) { this.execFn = execFn; }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nedb.executor"></a>[function <span class="apidocSignatureSpan">nedb.</span>executor ()](#apidoc.element.nedb.executor)
- description and source-code
```javascript
function Executor() {
  this.buffer = [];
  this.ready = false;

  // This queue will execute all commands, one-by-one in order
  this.queue = async.queue(function (task, cb) {
    var newArguments = [];

    // task.arguments is an array-like object on which adding a new field doesn't work, so we transform it into a real array
    for (var i = 0; i < task.arguments.length; i += 1) { newArguments.push(task.arguments[i]); }
    var lastArg = task.arguments[task.arguments.length - 1];

    // Always tell the queue task is complete. Execute callback if any was given.
    if (typeof lastArg === 'function') {
      // Callback was supplied
      newArguments[newArguments.length - 1] = function () {
        if (typeof setImmediate === 'function') {
           setImmediate(cb);
        } else {
          process.nextTick(cb);
        }
        lastArg.apply(null, arguments);
      };
    } else if (!lastArg && task.arguments.length !== 0) {
      // false/undefined/null supplied as callbback
      newArguments[newArguments.length - 1] = function () { cb(); };
    } else {
      // Nothing supplied as callback
      newArguments.push(function () { cb(); });
    }


    task.fn.apply(task.this, newArguments);
  }, 1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nedb.indexes"></a>[function <span class="apidocSignatureSpan">nedb.</span>indexes (options)](#apidoc.element.nedb.indexes)
- description and source-code
```javascript
function Index(options) {
  this.fieldName = options.fieldName;
  this.unique = options.unique || false;
  this.sparse = options.sparse || false;

  this.treeOptions = { unique: this.unique, compareKeys: model.compareThings, checkValueEquality: checkValueEquality };

  this.reset();   // No data in the beginning
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nedb.persistence"></a>[function <span class="apidocSignatureSpan">nedb.</span>persistence (options)](#apidoc.element.nedb.persistence)
- description and source-code
```javascript
function Persistence(options) {
  var i, j, randomString;

  this.db = options.db;
  this.inMemoryOnly = this.db.inMemoryOnly;
  this.filename = this.db.filename;
  this.corruptAlertThreshold = options.corruptAlertThreshold !== undefined ? options.corruptAlertThreshold : 0.1;

  if (!this.inMemoryOnly && this.filename && this.filename.charAt(this.filename.length - 1) === '~') {
    throw new Error("The datafile name can't end with a ~, which is reserved for crash safe backup files");
  }

  // After serialization and before deserialization hooks with some basic sanity checks
  if (options.afterSerialization && !options.beforeDeserialization) {
    throw new Error("Serialization hook defined but deserialization hook undefined, cautiously refusing to start NeDB to prevent
 dataloss");
  }
  if (!options.afterSerialization && options.beforeDeserialization) {
    throw new Error("Serialization hook undefined but deserialization hook defined, cautiously refusing to start NeDB to prevent
 dataloss");
  }
  this.afterSerialization = options.afterSerialization || function (s) { return s; };
  this.beforeDeserialization = options.beforeDeserialization || function (s) { return s; };
  for (i = 1; i < 30; i += 1) {
    for (j = 0; j < 10; j += 1) {
      randomString = customUtils.uid(i);
      if (this.beforeDeserialization(this.afterSerialization(randomString)) !== randomString) {
        throw new Error("beforeDeserialization is not the reverse of afterSerialization, cautiously refusing to start NeDB to prevent
 dataloss");
      }
    }
  }

  // For NW apps, store data in the same directory where NW stores application data
  if (this.filename && options.nodeWebkitAppName) {
    console.log("==================================================================");
    console.log("WARNING: The nodeWebkitAppName option is deprecated");
    console.log("To get the path to the directory where Node Webkit stores the data");
    console.log("for your app, use the internal nw.gui module like this");
    console.log("require('nw.gui').App.dataPath");
    console.log("See https://github.com/rogerwang/node-webkit/issues/500");
    console.log("==================================================================");
    this.filename = Persistence.getNWAppFilename(options.nodeWebkitAppName, this.filename);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nedb.super_"></a>[function <span class="apidocSignatureSpan">nedb.</span>super_ ()](#apidoc.element.nedb.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.nedb.cursor"></a>[module nedb.cursor](#apidoc.module.nedb.cursor)

#### <a name="apidoc.element.nedb.cursor.cursor"></a>[function <span class="apidocSignatureSpan">nedb.</span>cursor (db, query, execFn)](#apidoc.element.nedb.cursor.cursor)
- description and source-code
```javascript
function Cursor(db, query, execFn) {
  this.db = db;
  this.query = query || {};
  if (execFn) { this.execFn = execFn; }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.nedb.cursor.prototype"></a>[module nedb.cursor.prototype](#apidoc.module.nedb.cursor.prototype)

#### <a name="apidoc.element.nedb.cursor.prototype._exec"></a>[function <span class="apidocSignatureSpan">nedb.cursor.prototype.</span>_exec (_callback)](#apidoc.element.nedb.cursor.prototype._exec)
- description and source-code
```javascript
_exec = function (_callback) {
  var res = [], added = 0, skipped = 0, self = this
    , error = null
    , i, keys, key
    ;

  function callback (error, res) {
    if (self.execFn) {
      return self.execFn(error, res, _callback);
    } else {
      return _callback(error, res);
    }
  }

  this.db.getCandidates(this.query, function (err, candidates) {
    if (err) { return callback(err); }

    try {
      for (i = 0; i < candidates.length; i += 1) {
        if (model.match(candidates[i], self.query)) {
          // If a sort is defined, wait for the results to be sorted before applying limit and skip
          if (!self._sort) {
            if (self._skip && self._skip > skipped) {
              skipped += 1;
            } else {
              res.push(candidates[i]);
              added += 1;
              if (self._limit && self._limit <= added) { break; }
            }
          } else {
            res.push(candidates[i]);
          }
        }
      }
    } catch (err) {
      return callback(err);
    }

    // Apply all sorts
    if (self._sort) {
      keys = Object.keys(self._sort);

      // Sorting
      var criteria = [];
      for (i = 0; i < keys.length; i++) {
        key = keys[i];
        criteria.push({ key: key, direction: self._sort[key] });
      }
      res.sort(function(a, b) {
        var criterion, compare, i;
        for (i = 0; i < criteria.length; i++) {
          criterion = criteria[i];
          compare = criterion.direction * model.compareThings(model.getDotValue(a, criterion.key), model.getDotValue(b, criterion
.key), self.db.compareStrings);
          if (compare !== 0) {
            return compare;
          }
        }
        return 0;
      });

      // Applying limit and skip
      var limit = self._limit || res.length
        , skip = self._skip || 0;

      res = res.slice(skip, skip + limit);
    }

    // Apply projection
    try {
      res = self.project(res);
    } catch (e) {
      error = e;
      res = undefined;
    }

    return callback(error, res);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nedb.cursor.prototype.exec"></a>[function <span class="apidocSignatureSpan">nedb.cursor.prototype.</span>exec ()](#apidoc.element.nedb.cursor.prototype.exec)
- description and source-code
```javascript
exec = function () {
  this.db.executor.push({ this: this, fn: this._exec, arguments: arguments });
}
```
- example usage
```shell
...
// Let's say the database contains these 4 documents
// doc1 = { _id: 'id1', planet: 'Mars', system: 'solar', inhabited: false, satellites: ['Phobos', 'Deimos'] }
// doc2 = { _id: 'id2', planet: 'Earth', system: 'solar', inhabited: true, humans: { genders: 2, eyes: true } }
// doc3 = { _id: 'id3', planet: 'Jupiter', system: 'solar', inhabited: false }
// doc4 = { _id: 'id4', planet: 'Omicron Persei 8', system: 'futurama', inhabited: true, humans: { genders: 7 } }

// No query used means all results are returned (before the Cursor modifiers)
db.find({}).sort({ planet: 1 }).skip(1).limit(2).exec(function (err, docs) {
  // docs is [doc3, doc1]
});

// You can sort in reverse order like this
db.find({ system: 'solar' }).sort({ planet: -1 }).exec(function (err, docs) {
  // docs is [doc1, doc3, doc2]
});
...
```

#### <a name="apidoc.element.nedb.cursor.prototype.limit"></a>[function <span class="apidocSignatureSpan">nedb.cursor.prototype.</span>limit (limit)](#apidoc.element.nedb.cursor.prototype.limit)
- description and source-code
```javascript
limit = function (limit) {
  this._limit = limit;
  return this;
}
```
- example usage
```shell
...
// Let's say the database contains these 4 documents
// doc1 = { _id: 'id1', planet: 'Mars', system: 'solar', inhabited: false, satellites: ['Phobos', 'Deimos'] }
// doc2 = { _id: 'id2', planet: 'Earth', system: 'solar', inhabited: true, humans: { genders: 2, eyes: true } }
// doc3 = { _id: 'id3', planet: 'Jupiter', system: 'solar', inhabited: false }
// doc4 = { _id: 'id4', planet: 'Omicron Persei 8', system: 'futurama', inhabited: true, humans: { genders: 7 } }

// No query used means all results are returned (before the Cursor modifiers)
db.find({}).sort({ planet: 1 }).skip(1).limit(2).exec(function (err, docs) {
  // docs is [doc3, doc1]
});

// You can sort in reverse order like this
db.find({ system: 'solar' }).sort({ planet: -1 }).exec(function (err, docs) {
  // docs is [doc1, doc3, doc2]
});
...
```

#### <a name="apidoc.element.nedb.cursor.prototype.project"></a>[function <span class="apidocSignatureSpan">nedb.cursor.prototype.</span>project (candidates)](#apidoc.element.nedb.cursor.prototype.project)
- description and source-code
```javascript
project = function (candidates) {
  var res = [], self = this
    , keepId, action, keys
    ;

  if (this._projection === undefined || Object.keys(this._projection).length === 0) {
    return candidates;
  }

  keepId = this._projection._id === 0 ? false : true;
  this._projection = _.omit(this._projection, '_id');

  // Check for consistency
  keys = Object.keys(this._projection);
  keys.forEach(function (k) {
    if (action !== undefined && self._projection[k] !== action) { throw new Error("Can't both keep and omit fields except for _id
"); }
    action = self._projection[k];
  });

  // Do the actual projection
  candidates.forEach(function (candidate) {
    var toPush;
    if (action === 1) {   // pick-type projection
      toPush = { $set: {} };
      keys.forEach(function (k) {
        toPush.$set[k] = model.getDotValue(candidate, k);
        if (toPush.$set[k] === undefined) { delete toPush.$set[k]; }
      });
      toPush = model.modify({}, toPush);
    } else {   // omit-type projection
      toPush = { $unset: {} };
      keys.forEach(function (k) { toPush.$unset[k] = true });
      toPush = model.modify(candidate, toPush);
    }
    if (keepId) {
      toPush._id = candidate._id;
    } else {
      delete toPush._id;
    }
    res.push(toPush);
  });

  return res;
}
```
- example usage
```shell
...
      , skip = self._skip || 0;

    res = res.slice(skip, skip + limit);
  }

  // Apply projection
  try {
    res = self.project(res);
  } catch (e) {
    error = e;
    res = undefined;
  }

  return callback(error, res);
});
...
```

#### <a name="apidoc.element.nedb.cursor.prototype.projection"></a>[function <span class="apidocSignatureSpan">nedb.cursor.prototype.</span>projection (projection)](#apidoc.element.nedb.cursor.prototype.projection)
- description and source-code
```javascript
projection = function (projection) {
  this._projection = projection;
  return this;
}
```
- example usage
```shell
...

// Failure: using both modes at the same time
db.find({ planet: 'Mars' }, { planet: 0, system: 1 }, function (err, docs) {
  // err is the error message, docs is undefined
});

// You can also use it in a Cursor way but this syntax is not compatible with MongoDB
db.find({ planet: 'Mars' }).projection({ planet: 1, system: 1 }).exec(function (err, docs) {
  // docs is [{ planet: 'Mars', system: 'solar', _id: 'id1' }]
});

// Project on a nested document
db.findOne({ planet: 'Earth' }).projection({ planet: 1, 'humans.genders': 1 }).exec(function (err, doc) {
  // doc is { planet: 'Earth', _id: 'id2', humans: { genders: 2 } }
});
...
```

#### <a name="apidoc.element.nedb.cursor.prototype.skip"></a>[function <span class="apidocSignatureSpan">nedb.cursor.prototype.</span>skip (skip)](#apidoc.element.nedb.cursor.prototype.skip)
- description and source-code
```javascript
skip = function (skip) {
  this._skip = skip;
  return this;
}
```
- example usage
```shell
...
// Let's say the database contains these 4 documents
// doc1 = { _id: 'id1', planet: 'Mars', system: 'solar', inhabited: false, satellites: ['Phobos', 'Deimos'] }
// doc2 = { _id: 'id2', planet: 'Earth', system: 'solar', inhabited: true, humans: { genders: 2, eyes: true } }
// doc3 = { _id: 'id3', planet: 'Jupiter', system: 'solar', inhabited: false }
// doc4 = { _id: 'id4', planet: 'Omicron Persei 8', system: 'futurama', inhabited: true, humans: { genders: 7 } }

// No query used means all results are returned (before the Cursor modifiers)
db.find({}).sort({ planet: 1 }).skip(1).limit(2).exec(function (err, docs) {
  // docs is [doc3, doc1]
});

// You can sort in reverse order like this
db.find({ system: 'solar' }).sort({ planet: -1 }).exec(function (err, docs) {
  // docs is [doc1, doc3, doc2]
});
...
```

#### <a name="apidoc.element.nedb.cursor.prototype.sort"></a>[function <span class="apidocSignatureSpan">nedb.cursor.prototype.</span>sort (sortQuery)](#apidoc.element.nedb.cursor.prototype.sort)
- description and source-code
```javascript
sort = function (sortQuery) {
  this._sort = sortQuery;
  return this;
}
```
- example usage
```shell
...
// Let's say the database contains these 4 documents
// doc1 = { _id: 'id1', planet: 'Mars', system: 'solar', inhabited: false, satellites: ['Phobos', 'Deimos'] }
// doc2 = { _id: 'id2', planet: 'Earth', system: 'solar', inhabited: true, humans: { genders: 2, eyes: true } }
// doc3 = { _id: 'id3', planet: 'Jupiter', system: 'solar', inhabited: false }
// doc4 = { _id: 'id4', planet: 'Omicron Persei 8', system: 'futurama', inhabited: true, humans: { genders: 7 } }

// No query used means all results are returned (before the Cursor modifiers)
db.find({}).sort({ planet: 1 }).skip(1).limit(2).exec(function (err, docs) {
  // docs is [doc3, doc1]
});

// You can sort in reverse order like this
db.find({ system: 'solar' }).sort({ planet: -1 }).exec(function (err, docs) {
  // docs is [doc1, doc3, doc2]
});
...
```



# <a name="apidoc.module.nedb.customUtils"></a>[module nedb.customUtils](#apidoc.module.nedb.customUtils)

#### <a name="apidoc.element.nedb.customUtils.uid"></a>[function <span class="apidocSignatureSpan">nedb.customUtils.</span>uid (len)](#apidoc.element.nedb.customUtils.uid)
- description and source-code
```javascript
function uid(len) {
  return crypto.randomBytes(Math.ceil(Math.max(8, len * 2)))
    .toString('base64')
    .replace(/[+\/]/g, '')
    .slice(0, len);
}
```
- example usage
```shell
...
if (!options.afterSerialization && options.beforeDeserialization) {
  throw new Error("Serialization hook undefined but deserialization hook defined, cautiously refusing to start NeDB to prevent dataloss
");
}
this.afterSerialization = options.afterSerialization || function (s) { return s; };
this.beforeDeserialization = options.beforeDeserialization || function (s) { return s; };
for (i = 1; i < 30; i += 1) {
  for (j = 0; j < 10; j += 1) {
    randomString = customUtils.uid(i);
    if (this.beforeDeserialization(this.afterSerialization(randomString)) !== randomString) {
      throw new Error("beforeDeserialization is not the reverse of afterSerialization, cautiously refusing to start NeDB to prevent
 dataloss");
    }
  }
}

// For NW apps, store data in the same directory where NW stores application data
...
```



# <a name="apidoc.module.nedb.executor"></a>[module nedb.executor](#apidoc.module.nedb.executor)

#### <a name="apidoc.element.nedb.executor.executor"></a>[function <span class="apidocSignatureSpan">nedb.</span>executor ()](#apidoc.element.nedb.executor.executor)
- description and source-code
```javascript
function Executor() {
  this.buffer = [];
  this.ready = false;

  // This queue will execute all commands, one-by-one in order
  this.queue = async.queue(function (task, cb) {
    var newArguments = [];

    // task.arguments is an array-like object on which adding a new field doesn't work, so we transform it into a real array
    for (var i = 0; i < task.arguments.length; i += 1) { newArguments.push(task.arguments[i]); }
    var lastArg = task.arguments[task.arguments.length - 1];

    // Always tell the queue task is complete. Execute callback if any was given.
    if (typeof lastArg === 'function') {
      // Callback was supplied
      newArguments[newArguments.length - 1] = function () {
        if (typeof setImmediate === 'function') {
           setImmediate(cb);
        } else {
          process.nextTick(cb);
        }
        lastArg.apply(null, arguments);
      };
    } else if (!lastArg && task.arguments.length !== 0) {
      // false/undefined/null supplied as callbback
      newArguments[newArguments.length - 1] = function () { cb(); };
    } else {
      // Nothing supplied as callback
      newArguments.push(function () { cb(); });
    }


    task.fn.apply(task.this, newArguments);
  }, 1);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.nedb.executor.prototype"></a>[module nedb.executor.prototype](#apidoc.module.nedb.executor.prototype)

#### <a name="apidoc.element.nedb.executor.prototype.processBuffer"></a>[function <span class="apidocSignatureSpan">nedb.executor.prototype.</span>processBuffer ()](#apidoc.element.nedb.executor.prototype.processBuffer)
- description and source-code
```javascript
processBuffer = function () {
  var i;
  this.ready = true;
  for (i = 0; i < this.buffer.length; i += 1) { this.queue.push(this.buffer[i]); }
  this.buffer = [];
}
```
- example usage
```shell
...
          });
        });
      });
    }
  ], function (err) {
       if (err) { return callback(err); }

       self.db.executor.processBuffer();
       return callback(null);
     });
};


// Interface
module.exports = Persistence;
...
```

#### <a name="apidoc.element.nedb.executor.prototype.push"></a>[function <span class="apidocSignatureSpan">nedb.executor.prototype.</span>push (task, forceQueuing)](#apidoc.element.nedb.executor.prototype.push)
- description and source-code
```javascript
push = function (task, forceQueuing) {
  if (this.ready || forceQueuing) {
    this.queue.push(task);
  } else {
    this.buffer.push(task);
  }
}
```
- example usage
```shell
...
      toPush = model.modify(candidate, toPush);
    }
    if (keepId) {
      toPush._id = candidate._id;
    } else {
      delete toPush._id;
    }
    res.push(toPush);
  });

  return res;
};


/**
...
```



# <a name="apidoc.module.nedb.indexes"></a>[module nedb.indexes](#apidoc.module.nedb.indexes)

#### <a name="apidoc.element.nedb.indexes.indexes"></a>[function <span class="apidocSignatureSpan">nedb.</span>indexes (options)](#apidoc.element.nedb.indexes.indexes)
- description and source-code
```javascript
function Index(options) {
  this.fieldName = options.fieldName;
  this.unique = options.unique || false;
  this.sparse = options.sparse || false;

  this.treeOptions = { unique: this.unique, compareKeys: model.compareThings, checkValueEquality: checkValueEquality };

  this.reset();   // No data in the beginning
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.nedb.indexes.prototype"></a>[module nedb.indexes.prototype](#apidoc.module.nedb.indexes.prototype)

#### <a name="apidoc.element.nedb.indexes.prototype.getAll"></a>[function <span class="apidocSignatureSpan">nedb.indexes.prototype.</span>getAll ()](#apidoc.element.nedb.indexes.prototype.getAll)
- description and source-code
```javascript
getAll = function () {
  var res = [];

  this.tree.executeOnEveryNode(function (node) {
    var i;

    for (i = 0; i < node.data.length; i += 1) {
      res.push(node.data[i]);
    }
  });

  return res;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nedb.indexes.prototype.getBetweenBounds"></a>[function <span class="apidocSignatureSpan">nedb.indexes.prototype.</span>getBetweenBounds (query)](#apidoc.element.nedb.indexes.prototype.getBetweenBounds)
- description and source-code
```javascript
getBetweenBounds = function (query) {
  return this.tree.betweenBounds(query);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nedb.indexes.prototype.getMatching"></a>[function <span class="apidocSignatureSpan">nedb.indexes.prototype.</span>getMatching (value)](#apidoc.element.nedb.indexes.prototype.getMatching)
- description and source-code
```javascript
getMatching = function (value) {
  var self = this;

  if (!util.isArray(value)) {
    return self.tree.search(value);
  } else {
    var _res = {}, res = [];

    value.forEach(function (v) {
      self.getMatching(v).forEach(function (doc) {
        _res[doc._id] = doc;
      });
    });

    Object.keys(_res).forEach(function (_id) {
      res.push(_res[_id]);
    });

    return res;
  }
}
```
- example usage
```shell
...

  if (!util.isArray(value)) {
return self.tree.search(value);
  } else {
var _res = {}, res = [];

value.forEach(function (v) {
  self.getMatching(v).forEach(function (doc) {
    _res[doc._id] = doc;
  });
});

Object.keys(_res).forEach(function (_id) {
  res.push(_res[_id]);
});
...
```

#### <a name="apidoc.element.nedb.indexes.prototype.insert"></a>[function <span class="apidocSignatureSpan">nedb.indexes.prototype.</span>insert (doc)](#apidoc.element.nedb.indexes.prototype.insert)
- description and source-code
```javascript
insert = function (doc) {
  var key, self = this
    , keys, i, failingI, error
    ;

  if (util.isArray(doc)) { this.insertMultipleDocs(doc); return; }

  key = model.getDotValue(doc, this.fieldName);

  // We don't index documents that don't contain the field if the index is sparse
  if (key === undefined && this.sparse) { return; }

  if (!util.isArray(key)) {
    this.tree.insert(key, doc);
  } else {
    // If an insert fails due to a unique constraint, roll back all inserts before it
    keys = _.uniq(key, projectForUnique);

    for (i = 0; i < keys.length; i += 1) {
      try {
        this.tree.insert(keys[i], doc);
      } catch (e) {
        error = e;
        failingI = i;
        break;
      }
    }

    if (error) {
      for (i = 0; i < failingI; i += 1) {
        this.tree.delete(keys[i], doc);
      }

      throw error;
    }
  }
}
```
- example usage
```shell
...
               , nedbIsAwesome: true
               , notthere: null
               , notToBeSaved: undefined  // Will not be saved
               , fruits: [ 'apple', 'orange', 'pear' ]
               , infos: { name: 'nedb' }
               };

db.insert(doc, function (err, newDoc) {   // Callback is optional
  // newDoc is the newly inserted document, including its _id
  // newDoc has no key called notToBeSaved since its value was undefined
});
'''

You can also bulk-insert an array of documents. This operation is atomic, meaning that if one insert fails due to a unique constraint
 being violated, all changes are rolled back.
...
```

#### <a name="apidoc.element.nedb.indexes.prototype.insertMultipleDocs"></a>[function <span class="apidocSignatureSpan">nedb.indexes.prototype.</span>insertMultipleDocs (docs)](#apidoc.element.nedb.indexes.prototype.insertMultipleDocs)
- description and source-code
```javascript
insertMultipleDocs = function (docs) {
  var i, error, failingI;

  for (i = 0; i < docs.length; i += 1) {
    try {
      this.insert(docs[i]);
    } catch (e) {
      error = e;
      failingI = i;
      break;
    }
  }

  if (error) {
    for (i = 0; i < failingI; i += 1) {
      this.remove(docs[i]);
    }

    throw error;
  }
}
```
- example usage
```shell
...
 * O(log(n))
 */
Index.prototype.insert = function (doc) {
var key, self = this
  , keys, i, failingI, error
  ;

if (util.isArray(doc)) { this.insertMultipleDocs(doc); return; }

key = model.getDotValue(doc, this.fieldName);

// We don't index documents that don't contain the field if the index is sparse
if (key === undefined && this.sparse) { return; }

if (!util.isArray(key)) {
...
```

#### <a name="apidoc.element.nedb.indexes.prototype.remove"></a>[function <span class="apidocSignatureSpan">nedb.indexes.prototype.</span>remove (doc)](#apidoc.element.nedb.indexes.prototype.remove)
- description and source-code
```javascript
remove = function (doc) {
  var key, self = this;

  if (util.isArray(doc)) { doc.forEach(function (d) { self.remove(d); }); return; }

  key = model.getDotValue(doc, this.fieldName);

  if (key === undefined && this.sparse) { return; }

  if (!util.isArray(key)) {
    this.tree.delete(key, doc);
  } else {
    _.uniq(key, projectForUnique).forEach(function (_key) {
      self.tree.delete(_key, doc);
    });
  }
}
```
- example usage
```shell
...

db.update({ _id: 'id1' }, { $min: { value: 8 } }, {}, function () {
  // The document will not be modified
});
'''

### Removing documents
'db.remove(query, options, callback)' will remove all documents matching 'query' according to 'options'
* 'query' is the same as the ones used for finding and updating
* 'options' only one option for now: 'multi' which allows the removal of multiple documents if set to true. Default is false
* 'callback' is optional, signature: err, numRemoved

'''javascript
// Let's use the same example collection as in the "finding document" part
// { _id: 'id1', planet: 'Mars', system: 'solar', inhabited: false }
...
```

#### <a name="apidoc.element.nedb.indexes.prototype.reset"></a>[function <span class="apidocSignatureSpan">nedb.indexes.prototype.</span>reset (newData)](#apidoc.element.nedb.indexes.prototype.reset)
- description and source-code
```javascript
reset = function (newData) {
  this.tree = new BinarySearchTree(this.treeOptions);

  if (newData) { this.insert(newData); }
}
```
- example usage
```shell
...
function Index (options) {
 this.fieldName = options.fieldName;
 this.unique = options.unique || false;
 this.sparse = options.sparse || false;

 this.treeOptions = { unique: this.unique, compareKeys: model.compareThings, checkValueEquality: checkValueEquality };

 this.reset();   // No data in the beginning
}


/**
* Reset an index
* @param {Document or Array of documents} newData Optional, data to initialize the index with
*                                                 If an error is thrown during insertion, the index is not modified
...
```

#### <a name="apidoc.element.nedb.indexes.prototype.revertUpdate"></a>[function <span class="apidocSignatureSpan">nedb.indexes.prototype.</span>revertUpdate (oldDoc, newDoc)](#apidoc.element.nedb.indexes.prototype.revertUpdate)
- description and source-code
```javascript
revertUpdate = function (oldDoc, newDoc) {
  var revert = [];

  if (!util.isArray(oldDoc)) {
    this.update(newDoc, oldDoc);
  } else {
    oldDoc.forEach(function (pair) {
      revert.push({ oldDoc: pair.newDoc, newDoc: pair.oldDoc });
    });
    this.update(revert);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nedb.indexes.prototype.update"></a>[function <span class="apidocSignatureSpan">nedb.indexes.prototype.</span>update (oldDoc, newDoc)](#apidoc.element.nedb.indexes.prototype.update)
- description and source-code
```javascript
update = function (oldDoc, newDoc) {
  if (util.isArray(oldDoc)) { this.updateMultipleDocs(oldDoc); return; }

  this.remove(oldDoc);

  try {
    this.insert(newDoc);
  } catch (e) {
    this.insert(oldDoc);
    throw e;
  }
}
```
- example usage
```shell
...
db.count({}, function (err, count) {
// count equals to 4
});
'''


### Updating documents
'db.update(query, update, options, callback)' will update all documents matching 'query' according to the 'update' rules:
* 'query' is the same kind of finding query you use with 'find' and 'findOne'
* 'update' specifies how the documents should be modified. It is either a new document or a set of modifiers (you cannot use both
 together, it doesn't make sense!)
* A new document will replace the matched docs
* The modifiers create the fields they need to modify if they don't exist, and you can apply them to subdocs. Available field modifiers
 are '$set' to change a field's value, '$unset' to delete a field, '$inc' to increment a field's value and '$min'/'$max' to change
 field's value, only if provided value is less/greater than current value. To work on arrays, you have '$push', '$pop', '$addToSet
', '$pull', and the special '$each' and '$slice'. See examples below for the syntax.
* 'options' is an object with two possible parameters
* 'multi' (defaults to 'false') which allows the modification of several documents if set to true
* 'upsert' (defaults to 'false') if you want to insert a new document corresponding to the 'update' rules if your 'query' doesn'
t match anything. If your 'update' is a simple object with no modifiers, it is the inserted document. In the other case, the 'query
' is stripped from all operator recursively, and the 'update' is applied to it.
...
```

#### <a name="apidoc.element.nedb.indexes.prototype.updateMultipleDocs"></a>[function <span class="apidocSignatureSpan">nedb.indexes.prototype.</span>updateMultipleDocs (pairs)](#apidoc.element.nedb.indexes.prototype.updateMultipleDocs)
- description and source-code
```javascript
updateMultipleDocs = function (pairs) {
  var i, failingI, error;

  for (i = 0; i < pairs.length; i += 1) {
    this.remove(pairs[i].oldDoc);
  }

  for (i = 0; i < pairs.length; i += 1) {
    try {
      this.insert(pairs[i].newDoc);
    } catch (e) {
      error = e;
      failingI = i;
      break;
    }
  }

  // If an error was raised, roll back changes in the inverse order
  if (error) {
    for (i = 0; i < failingI; i += 1) {
      this.remove(pairs[i].newDoc);
    }

    for (i = 0; i < pairs.length; i += 1) {
      this.insert(pairs[i].oldDoc);
    }

    throw error;
  }
}
```
- example usage
```shell
...

/**
 * Update a document in the index
 * If a constraint is violated, changes are rolled back and an error thrown
 * Naive implementation, still in O(log(n))
 */
Index.prototype.update = function (oldDoc, newDoc) {
if (util.isArray(oldDoc)) { this.updateMultipleDocs(oldDoc); return; }

this.remove(oldDoc);

try {
  this.insert(newDoc);
} catch (e) {
  this.insert(oldDoc);
...
```



# <a name="apidoc.module.nedb.model"></a>[module nedb.model](#apidoc.module.nedb.model)

#### <a name="apidoc.element.nedb.model.areThingsEqual"></a>[function <span class="apidocSignatureSpan">nedb.model.</span>areThingsEqual (a, b)](#apidoc.element.nedb.model.areThingsEqual)
- description and source-code
```javascript
function areThingsEqual(a, b) {
  var aKeys , bKeys , i;

  // Strings, booleans, numbers, null
  if (a === null || typeof a === 'string' || typeof a === 'boolean' || typeof a === 'number' ||
      b === null || typeof b === 'string' || typeof b === 'boolean' || typeof b === 'number') { return a === b; }

  // Dates
  if (util.isDate(a) || util.isDate(b)) { return util.isDate(a) && util.isDate(b) && a.getTime() === b.getTime(); }

  // Arrays (no match since arrays are used as a $in)
  // undefined (no match since they mean field doesn't exist and can't be serialized)
  if ((!(util.isArray(a) && util.isArray(b)) && (util.isArray(a) || util.isArray(b))) || a === undefined || b === undefined) { return
 false; }

  // General objects (check for deep equality)
  // a and b should be objects at this point
  try {
    aKeys = Object.keys(a);
    bKeys = Object.keys(b);
  } catch (e) {
    return false;
  }

  if (aKeys.length !== bKeys.length) { return false; }
  for (i = 0; i < aKeys.length; i += 1) {
    if (bKeys.indexOf(aKeys[i]) === -1) { return false; }
    if (!areThingsEqual(a[aKeys[i]], b[aKeys[i]])) { return false; }
  }
  return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nedb.model.checkObject"></a>[function <span class="apidocSignatureSpan">nedb.model.</span>checkObject (obj)](#apidoc.element.nedb.model.checkObject)
- description and source-code
```javascript
function checkObject(obj) {
  if (util.isArray(obj)) {
    obj.forEach(function (o) {
      checkObject(o);
    });
  }

  if (typeof obj === 'object' && obj !== null) {
    Object.keys(obj).forEach(function (k) {
      checkKey(k, obj[k]);
      checkObject(obj[k]);
    });
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nedb.model.compareThings"></a>[function <span class="apidocSignatureSpan">nedb.model.</span>compareThings (a, b, _compareStrings)](#apidoc.element.nedb.model.compareThings)
- description and source-code
```javascript
function compareThings(a, b, _compareStrings) {
  var aKeys, bKeys, comp, i
    , compareStrings = _compareStrings || compareNSB;

  // undefined
  if (a === undefined) { return b === undefined ? 0 : -1; }
  if (b === undefined) { return a === undefined ? 0 : 1; }

  // null
  if (a === null) { return b === null ? 0 : -1; }
  if (b === null) { return a === null ? 0 : 1; }

  // Numbers
  if (typeof a === 'number') { return typeof b === 'number' ? compareNSB(a, b) : -1; }
  if (typeof b === 'number') { return typeof a === 'number' ? compareNSB(a, b) : 1; }

  // Strings
  if (typeof a === 'string') { return typeof b === 'string' ? compareStrings(a, b) : -1; }
  if (typeof b === 'string') { return typeof a === 'string' ? compareStrings(a, b) : 1; }

  // Booleans
  if (typeof a === 'boolean') { return typeof b === 'boolean' ? compareNSB(a, b) : -1; }
  if (typeof b === 'boolean') { return typeof a === 'boolean' ? compareNSB(a, b) : 1; }

  // Dates
  if (util.isDate(a)) { return util.isDate(b) ? compareNSB(a.getTime(), b.getTime()) : -1; }
  if (util.isDate(b)) { return util.isDate(a) ? compareNSB(a.getTime(), b.getTime()) : 1; }

  // Arrays (first element is most significant and so on)
  if (util.isArray(a)) { return util.isArray(b) ? compareArrays(a, b) : -1; }
  if (util.isArray(b)) { return util.isArray(a) ? compareArrays(a, b) : 1; }

  // Objects
  aKeys = Object.keys(a).sort();
  bKeys = Object.keys(b).sort();

  for (i = 0; i < Math.min(aKeys.length, bKeys.length); i += 1) {
    comp = compareThings(a[aKeys[i]], b[bKeys[i]]);

    if (comp !== 0) { return comp; }
  }

  return compareNSB(aKeys.length, bKeys.length);
}
```
- example usage
```shell
...
  key = keys[i];
  criteria.push({ key: key, direction: self._sort[key] });
}
res.sort(function(a, b) {
  var criterion, compare, i;
  for (i = 0; i < criteria.length; i++) {
    criterion = criteria[i];
    compare = criterion.direction * model.compareThings(model.getDotValue(a, criterion.key), model.getDotValue(b, criterion.key),
self.db.compareStrings);
    if (compare !== 0) {
      return compare;
    }
  }
  return 0;
});
...
```

#### <a name="apidoc.element.nedb.model.deepCopy"></a>[function <span class="apidocSignatureSpan">nedb.model.</span>deepCopy (obj, strictKeys)](#apidoc.element.nedb.model.deepCopy)
- description and source-code
```javascript
function deepCopy(obj, strictKeys) {
  var res;

  if ( typeof obj === 'boolean' ||
       typeof obj === 'number' ||
       typeof obj === 'string' ||
       obj === null ||
       (util.isDate(obj)) ) {
    return obj;
  }

  if (util.isArray(obj)) {
    res = [];
    obj.forEach(function (o) { res.push(deepCopy(o, strictKeys)); });
    return res;
  }

  if (typeof obj === 'object') {
    res = {};
    Object.keys(obj).forEach(function (k) {
      if (!strictKeys || (k[0] !== '$' && k.indexOf('.') === -1)) {
        res[k] = deepCopy(obj[k], strictKeys);
      }
    });
    return res;
  }

  return undefined;   // For now everything else is undefined. We should probably throw an error instead
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nedb.model.deserialize"></a>[function <span class="apidocSignatureSpan">nedb.model.</span>deserialize (rawData)](#apidoc.element.nedb.model.deserialize)
- description and source-code
```javascript
function deserialize(rawData) {
  return JSON.parse(rawData, function (k, v) {
    if (k === '$$date') { return new Date(v); }
    if (typeof v === 'string' || typeof v === 'number' || typeof v === 'boolean' || v === null) { return v; }
    if (v && v.$$date) { return v.$$date; }

    return v;
  });
}
```
- example usage
```shell
...
, corruptItems = -1   // Last line of every data file is usually blank so not really corrupt
;

  for (i = 0; i < data.length; i += 1) {
var doc;

try {
  doc = model.deserialize(this.beforeDeserialization(data[i]));
  if (doc._id) {
    if (doc.$$deleted === true) {
      delete dataById[doc._id];
    } else {
      dataById[doc._id] = doc;
    }
  } else if (doc.$$indexCreated && doc.$$indexCreated.fieldName != undefined) {
...
```

#### <a name="apidoc.element.nedb.model.getDotValue"></a>[function <span class="apidocSignatureSpan">nedb.model.</span>getDotValue (obj, field)](#apidoc.element.nedb.model.getDotValue)
- description and source-code
```javascript
function getDotValue(obj, field) {
  var fieldParts = typeof field === 'string' ? field.split('.') : field
    , i, objs;

  if (!obj) { return undefined; }   // field cannot be empty so that means we should return undefined so that nothing can match

  if (fieldParts.length === 0) { return obj; }

  if (fieldParts.length === 1) { return obj[fieldParts[0]]; }

  if (util.isArray(obj[fieldParts[0]])) {
    // If the next field is an integer, return only this item of the array
    i = parseInt(fieldParts[1], 10);
    if (typeof i === 'number' && !isNaN(i)) {
      return getDotValue(obj[fieldParts[0]][i], fieldParts.slice(2))
    }

    // Return the array of values
    objs = new Array();
    for (i = 0; i < obj[fieldParts[0]].length; i += 1) {
       objs.push(getDotValue(obj[fieldParts[0]][i], fieldParts.slice(1)));
    }
    return objs;
  } else {
    return getDotValue(obj[fieldParts[0]], fieldParts.slice(1));
  }
}
```
- example usage
```shell
...

// Do the actual projection
candidates.forEach(function (candidate) {
  var toPush;
  if (action === 1) {   // pick-type projection
    toPush = { $set: {} };
    keys.forEach(function (k) {
      toPush.$set[k] = model.getDotValue(candidate, k);
      if (toPush.$set[k] === undefined) { delete toPush.$set[k]; }
    });
    toPush = model.modify({}, toPush);
  } else {   // omit-type projection
    toPush = { $unset: {} };
    keys.forEach(function (k) { toPush.$unset[k] = true });
    toPush = model.modify(candidate, toPush);
...
```

#### <a name="apidoc.element.nedb.model.isPrimitiveType"></a>[function <span class="apidocSignatureSpan">nedb.model.</span>isPrimitiveType (obj)](#apidoc.element.nedb.model.isPrimitiveType)
- description and source-code
```javascript
function isPrimitiveType(obj) {
  return ( typeof obj === 'boolean' ||
       typeof obj === 'number' ||
       typeof obj === 'string' ||
       obj === null ||
       util.isDate(obj) ||
       util.isArray(obj));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nedb.model.match"></a>[function <span class="apidocSignatureSpan">nedb.model.</span>match (obj, query)](#apidoc.element.nedb.model.match)
- description and source-code
```javascript
function match(obj, query) {
  var queryKeys, queryKey, queryValue, i;

  // Primitive query against a primitive type
  // This is a bit of a hack since we construct an object with an arbitrary key only to dereference it later
  // But I don't have time for a cleaner implementation now
  if (isPrimitiveType(obj) || isPrimitiveType(query)) {
    return matchQueryPart({ needAKey: obj }, 'needAKey', query);
  }

  // Normal query
  queryKeys = Object.keys(query);
  for (i = 0; i < queryKeys.length; i += 1) {
    queryKey = queryKeys[i];
    queryValue = query[queryKey];

    if (queryKey[0] === '$') {
      if (!logicalOperators[queryKey]) { throw new Error("Unknown logical operator " + queryKey); }
      if (!logicalOperators[queryKey](obj, queryValue)) { return false; }
    } else {
      if (!matchQueryPart(obj, queryKey, queryValue)) { return false; }
    }
  }

  return true;
}
```
- example usage
```shell
...
  }

  this.db.getCandidates(this.query, function (err, candidates) {
if (err) { return callback(err); }

try {
  for (i = 0; i < candidates.length; i += 1) {
    if (model.match(candidates[i], self.query)) {
      // If a sort is defined, wait for the results to be sorted before applying limit and skip
      if (!self._sort) {
        if (self._skip && self._skip > skipped) {
          skipped += 1;
        } else {
          res.push(candidates[i]);
          added += 1;
...
```

#### <a name="apidoc.element.nedb.model.modify"></a>[function <span class="apidocSignatureSpan">nedb.model.</span>modify (obj, updateQuery)](#apidoc.element.nedb.model.modify)
- description and source-code
```javascript
function modify(obj, updateQuery) {
  var keys = Object.keys(updateQuery)
    , firstChars = _.map(keys, function (item) { return item[0]; })
    , dollarFirstChars = _.filter(firstChars, function (c) { return c === '$'; })
    , newDoc, modifiers
    ;

  if (keys.indexOf('_id') !== -1 && updateQuery._id !== obj._id) { throw new Error("You cannot change a document's _id"); }

  if (dollarFirstChars.length !== 0 && dollarFirstChars.length !== firstChars.length) {
    throw new Error("You cannot mix modifiers and normal fields");
  }

  if (dollarFirstChars.length === 0) {
    // Simply replace the object with the update query contents
    newDoc = deepCopy(updateQuery);
    newDoc._id = obj._id;
  } else {
    // Apply modifiers
    modifiers = _.uniq(keys);
    newDoc = deepCopy(obj);
    modifiers.forEach(function (m) {
      var keys;

      if (!modifierFunctions[m]) { throw new Error("Unknown modifier " + m); }

      // Can't rely on Object.keys throwing on non objects since ES6
      // Not 100% satisfying as non objects can be interpreted as objects but no false negatives so we can live with it
      if (typeof updateQuery[m] !== 'object') {
        throw new Error("Modifier " + m + "'s argument must be an object");
      }

      keys = Object.keys(updateQuery[m]);
      keys.forEach(function (k) {
        modifierFunctions[m](newDoc, k, updateQuery[m][k]);
      });
    });
  }

  // Check result is valid and return it
  checkObject(newDoc);

  if (obj._id !== newDoc._id) { throw new Error("You can't change a document's _id"); }
  return newDoc;
}
```
- example usage
```shell
...
var toPush;
if (action === 1) {   // pick-type projection
  toPush = { $set: {} };
  keys.forEach(function (k) {
    toPush.$set[k] = model.getDotValue(candidate, k);
    if (toPush.$set[k] === undefined) { delete toPush.$set[k]; }
  });
  toPush = model.modify({}, toPush);
} else {   // omit-type projection
  toPush = { $unset: {} };
  keys.forEach(function (k) { toPush.$unset[k] = true });
  toPush = model.modify(candidate, toPush);
}
if (keepId) {
  toPush._id = candidate._id;
...
```

#### <a name="apidoc.element.nedb.model.serialize"></a>[function <span class="apidocSignatureSpan">nedb.model.</span>serialize (obj)](#apidoc.element.nedb.model.serialize)
- description and source-code
```javascript
function serialize(obj) {
  var res;

  res = JSON.stringify(obj, function (k, v) {
    checkKey(k, v);

    if (v === undefined) { return undefined; }
    if (v === null) { return null; }

    // Hackish way of checking if object is Date (this way it works between execution contexts in node-webkit).
    // We can't use value directly because for dates it is already string in this function (date.toJSON was already called), so
we use this
    if (typeof this[k].getTime === 'function') { return { $$date: this[k].getTime() }; }

    return v;
  });

  return res;
}
```
- example usage
```shell
...
  , toPersist = ''
  , self = this
  ;

if (this.inMemoryOnly) { return callback(null); }

this.db.getAllData().forEach(function (doc) {
  toPersist += self.afterSerialization(model.serialize(doc)) + '\n';
});
Object.keys(this.db.indexes).forEach(function (fieldName) {
  if (fieldName != "_id") {   // The special _id index is managed by datastore.js, the others need to be persisted
    toPersist += self.afterSerialization(model.serialize({ $$indexCreated: { fieldName: fieldName, unique: self.db.indexes[fieldName
].unique, sparse: self.db.indexes[fieldName].sparse }})) + '\n';
  }
});
...
```



# <a name="apidoc.module.nedb.persistence"></a>[module nedb.persistence](#apidoc.module.nedb.persistence)

#### <a name="apidoc.element.nedb.persistence.persistence"></a>[function <span class="apidocSignatureSpan">nedb.</span>persistence (options)](#apidoc.element.nedb.persistence.persistence)
- description and source-code
```javascript
function Persistence(options) {
  var i, j, randomString;

  this.db = options.db;
  this.inMemoryOnly = this.db.inMemoryOnly;
  this.filename = this.db.filename;
  this.corruptAlertThreshold = options.corruptAlertThreshold !== undefined ? options.corruptAlertThreshold : 0.1;

  if (!this.inMemoryOnly && this.filename && this.filename.charAt(this.filename.length - 1) === '~') {
    throw new Error("The datafile name can't end with a ~, which is reserved for crash safe backup files");
  }

  // After serialization and before deserialization hooks with some basic sanity checks
  if (options.afterSerialization && !options.beforeDeserialization) {
    throw new Error("Serialization hook defined but deserialization hook undefined, cautiously refusing to start NeDB to prevent
 dataloss");
  }
  if (!options.afterSerialization && options.beforeDeserialization) {
    throw new Error("Serialization hook undefined but deserialization hook defined, cautiously refusing to start NeDB to prevent
 dataloss");
  }
  this.afterSerialization = options.afterSerialization || function (s) { return s; };
  this.beforeDeserialization = options.beforeDeserialization || function (s) { return s; };
  for (i = 1; i < 30; i += 1) {
    for (j = 0; j < 10; j += 1) {
      randomString = customUtils.uid(i);
      if (this.beforeDeserialization(this.afterSerialization(randomString)) !== randomString) {
        throw new Error("beforeDeserialization is not the reverse of afterSerialization, cautiously refusing to start NeDB to prevent
 dataloss");
      }
    }
  }

  // For NW apps, store data in the same directory where NW stores application data
  if (this.filename && options.nodeWebkitAppName) {
    console.log("==================================================================");
    console.log("WARNING: The nodeWebkitAppName option is deprecated");
    console.log("To get the path to the directory where Node Webkit stores the data");
    console.log("for your app, use the internal nw.gui module like this");
    console.log("require('nw.gui').App.dataPath");
    console.log("See https://github.com/rogerwang/node-webkit/issues/500");
    console.log("==================================================================");
    this.filename = Persistence.getNWAppFilename(options.nodeWebkitAppName, this.filename);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nedb.persistence.ensureDirectoryExists"></a>[function <span class="apidocSignatureSpan">nedb.persistence.</span>ensureDirectoryExists (dir, cb)](#apidoc.element.nedb.persistence.ensureDirectoryExists)
- description and source-code
```javascript
ensureDirectoryExists = function (dir, cb) {
  var callback = cb || function () {}
    ;

  storage.mkdirp(dir, function (err) { return callback(err); });
}
```
- example usage
```shell
...
  self.db.resetIndexes();

  // In-memory only datastore
  if (self.inMemoryOnly) { return callback(null); }

  async.waterfall([
    function (cb) {
      Persistence.ensureDirectoryExists(path.dirname(self.filename), function (err) {
        storage.ensureDatafileIntegrity(self.filename, function (err) {
          storage.readFile(self.filename, 'utf8', function (err, rawData) {
if (err) { return cb(err); }

try {
  var treatedData = self.treatRawData(rawData);
} catch (e) {
...
```

#### <a name="apidoc.element.nedb.persistence.getNWAppFilename"></a>[function <span class="apidocSignatureSpan">nedb.persistence.</span>getNWAppFilename (appName, relativeFilename)](#apidoc.element.nedb.persistence.getNWAppFilename)
- description and source-code
```javascript
getNWAppFilename = function (appName, relativeFilename) {
  var home;

  switch (process.platform) {
    case 'win32':
    case 'win64':
      home = process.env.LOCALAPPDATA || process.env.APPDATA;
      if (!home) { throw new Error("Couldn't find the base application data folder"); }
      home = path.join(home, appName);
      break;
    case 'darwin':
      home = process.env.HOME;
      if (!home) { throw new Error("Couldn't find the base application data directory"); }
      home = path.join(home, 'Library', 'Application Support', appName);
      break;
    case 'linux':
      home = process.env.HOME;
      if (!home) { throw new Error("Couldn't find the base application data directory"); }
      home = path.join(home, '.config', appName);
      break;
    default:
      throw new Error("Can't use the Node Webkit relative path for platform " + process.platform);
      break;
  }

  return path.join(home, 'nedb-data', relativeFilename);
}
```
- example usage
```shell
...
   console.log("==================================================================");
   console.log("WARNING: The nodeWebkitAppName option is deprecated");
   console.log("To get the path to the directory where Node Webkit stores the data");
   console.log("for your app, use the internal nw.gui module like this");
   console.log("require('nw.gui').App.dataPath");
   console.log("See https://github.com/rogerwang/node-webkit/issues/500");
   console.log("==================================================================");
   this.filename = Persistence.getNWAppFilename(options.nodeWebkitAppName, this.filename);
 }
};


/**
* Check if a directory exists and create it on the fly if it is not the case
* cb is optional, signature: err
...
```



# <a name="apidoc.module.nedb.persistence.prototype"></a>[module nedb.persistence.prototype](#apidoc.module.nedb.persistence.prototype)

#### <a name="apidoc.element.nedb.persistence.prototype.compactDatafile"></a>[function <span class="apidocSignatureSpan">nedb.persistence.prototype.</span>compactDatafile ()](#apidoc.element.nedb.persistence.prototype.compactDatafile)
- description and source-code
```javascript
compactDatafile = function () {
  this.db.executor.push({ this: this, fn: this.persistCachedDatabase, arguments: [] });
}
```
- example usage
```shell
...
   , minInterval = 5000
   , realInterval = Math.max(interval || 0, minInterval)
   ;

 this.stopAutocompaction();

 this.autocompactionIntervalId = setInterval(function () {
   self.compactDatafile();
 }, realInterval);
};


/**
* Stop autocompaction (do nothing if autocompaction was not running)
*/
...
```

#### <a name="apidoc.element.nedb.persistence.prototype.loadDatabase"></a>[function <span class="apidocSignatureSpan">nedb.persistence.prototype.</span>loadDatabase (cb)](#apidoc.element.nedb.persistence.prototype.loadDatabase)
- description and source-code
```javascript
loadDatabase = function (cb) {
  var callback = cb || function () {}
    , self = this
    ;

  self.db.resetIndexes();

  // In-memory only datastore
  if (self.inMemoryOnly) { return callback(null); }

  async.waterfall([
    function (cb) {
      Persistence.ensureDirectoryExists(path.dirname(self.filename), function (err) {
        storage.ensureDatafileIntegrity(self.filename, function (err) {
          storage.readFile(self.filename, 'utf8', function (err, rawData) {
            if (err) { return cb(err); }

            try {
              var treatedData = self.treatRawData(rawData);
            } catch (e) {
              return cb(e);
            }

            // Recreate all indexes in the datafile
            Object.keys(treatedData.indexes).forEach(function (key) {
              self.db.indexes[key] = new Index(treatedData.indexes[key]);
            });

            // Fill cached database (i.e. all indexes) with data
            try {
              self.db.resetIndexes(treatedData.data);
            } catch (e) {
              self.db.resetIndexes();   // Rollback any index which didn't fail
              return cb(e);
            }

            self.db.persistence.persistCachedDatabase(cb);
          });
        });
      });
    }
  ], function (err) {
       if (err) { return callback(err); }

       self.db.executor.processBuffer();
       return callback(null);
     });
}
```
- example usage
```shell
...
var Datastore = require('nedb')
, db = new Datastore();


// Type 2: Persistent datastore with manual loading
var Datastore = require('nedb')
, db = new Datastore({ filename: 'path/to/datafile' });
db.loadDatabase(function (err) {    // Callback is optional
// Now commands will be executed
});


// Type 3: Persistent datastore with automatic loading
var Datastore = require('nedb')
, db = new Datastore({ filename: 'path/to/datafile', autoload: true });
...
```

#### <a name="apidoc.element.nedb.persistence.prototype.persistCachedDatabase"></a>[function <span class="apidocSignatureSpan">nedb.persistence.prototype.</span>persistCachedDatabase (cb)](#apidoc.element.nedb.persistence.prototype.persistCachedDatabase)
- description and source-code
```javascript
persistCachedDatabase = function (cb) {
  var callback = cb || function () {}
    , toPersist = ''
    , self = this
    ;

  if (this.inMemoryOnly) { return callback(null); }

  this.db.getAllData().forEach(function (doc) {
    toPersist += self.afterSerialization(model.serialize(doc)) + '\n';
  });
  Object.keys(this.db.indexes).forEach(function (fieldName) {
    if (fieldName != "_id") {   // The special _id index is managed by datastore.js, the others need to be persisted
      toPersist += self.afterSerialization(model.serialize({ $$indexCreated: { fieldName: fieldName, unique: self.db.indexes[fieldName
].unique, sparse: self.db.indexes[fieldName].sparse }})) + '\n';
    }
  });

  storage.crashSafeWriteFile(this.filename, toPersist, function (err) {
    if (err) { return callback(err); }
    self.db.emit('compaction.done');
    return callback(null);
  });
}
```
- example usage
```shell
...
          try {
            self.db.resetIndexes(treatedData.data);
          } catch (e) {
            self.db.resetIndexes();   // Rollback any index which didn't fail
            return cb(e);
          }

          self.db.persistence.persistCachedDatabase(cb);
        });
      });
    });
  }
], function (err) {
     if (err) { return callback(err); }
...
```

#### <a name="apidoc.element.nedb.persistence.prototype.persistNewState"></a>[function <span class="apidocSignatureSpan">nedb.persistence.prototype.</span>persistNewState (newDocs, cb)](#apidoc.element.nedb.persistence.prototype.persistNewState)
- description and source-code
```javascript
persistNewState = function (newDocs, cb) {
  var self = this
    , toPersist = ''
    , callback = cb || function () {}
    ;

  // In-memory only datastore
  if (self.inMemoryOnly) { return callback(null); }

  newDocs.forEach(function (doc) {
    toPersist += self.afterSerialization(model.serialize(doc)) + '\n';
  });

  if (toPersist.length === 0) { return callback(null); }

  storage.appendFile(self.filename, toPersist, 'utf8', function (err) {
    return callback(err);
  });
}
```
- example usage
```shell
...



/**
 * Handle every persistence-related task
 * The interface Datastore expects to be implemented is
 * * Persistence.loadDatabase(callback) and callback has signature err
 * * Persistence.persistNewState(newDocs, callback) where newDocs is an array of documents and callback has signature err
 */

var storage = require('./storage')
, path = require('path')
, model = require('./model')
, async = require('async')
, customUtils = require('./customUtils')
...
```

#### <a name="apidoc.element.nedb.persistence.prototype.setAutocompactionInterval"></a>[function <span class="apidocSignatureSpan">nedb.persistence.prototype.</span>setAutocompactionInterval (interval)](#apidoc.element.nedb.persistence.prototype.setAutocompactionInterval)
- description and source-code
```javascript
setAutocompactionInterval = function (interval) {
  var self = this
    , minInterval = 5000
    , realInterval = Math.max(interval || 0, minInterval)
    ;

  this.stopAutocompaction();

  this.autocompactionIntervalId = setInterval(function () {
    self.compactDatafile();
  }, realInterval);
}
```
- example usage
```shell
...
'''

### Persistence
Under the hood, NeDB's persistence uses an append-only format, meaning that all updates and deletes actually result in lines added
 at the end of the datafile, for performance reasons. The database is automatically compacted (i.e. put back in the one-line-per
-document format) every time you load each database within your application.

You can manually call the compaction function with 'yourDatabase.persistence.compactDatafile' which takes no argument. It queues
 a compaction of the datafile in the executor, to be executed sequentially after all pending operations. The datastore will fire
 a 'compaction.done' event once compaction is finished.

You can also set automatic compaction at regular intervals with 'yourDatabase.persistence.setAutocompactionInterval(interval)', '
interval' in milliseconds (a minimum of 5s is enforced), and stop automatic compaction with 'yourDatabase.persistence.stopAutocompaction
()'.

Keep in mind that compaction takes a bit of time (not too much: 130ms for 50k records on a typical development machine) and no other
 operation can happen when it does, so most projects actually don't need to use it.

Compaction will also immediately remove any documents whose data line has become corrupted, assuming that the total percentage of
 all corrupted documents in that database still falls below the specified 'corruptAlertThreshold' option's value.

Durability works similarly to major databases: compaction forces the OS to physically flush data to disk, while appends to the data
 file do not (the OS is responsible for flushing the data). That guarantees that a server crash can never cause complete data loss
, while preserving performance. The worst that can happen is a crash between two syncs, causing a loss of all data between the two
 syncs. Usually syncs are 30 seconds appart so that's at most 30 seconds of data. <a href="http://oldblog.antirez.com/post/redis
-persistence-demystified.html" target="_blank">This post by Antirez on Redis persistence</a> explains this in more details, NeDB
 being very close to Redis AOF persistence with 'appendfsync' option set to 'no'.
...
```

#### <a name="apidoc.element.nedb.persistence.prototype.stopAutocompaction"></a>[function <span class="apidocSignatureSpan">nedb.persistence.prototype.</span>stopAutocompaction ()](#apidoc.element.nedb.persistence.prototype.stopAutocompaction)
- description and source-code
```javascript
stopAutocompaction = function () {
  if (this.autocompactionIntervalId) { clearInterval(this.autocompactionIntervalId); }
}
```
- example usage
```shell
...
'''

### Persistence
Under the hood, NeDB's persistence uses an append-only format, meaning that all updates and deletes actually result in lines added
 at the end of the datafile, for performance reasons. The database is automatically compacted (i.e. put back in the one-line-per
-document format) every time you load each database within your application.

You can manually call the compaction function with 'yourDatabase.persistence.compactDatafile' which takes no argument. It queues
 a compaction of the datafile in the executor, to be executed sequentially after all pending operations. The datastore will fire
 a 'compaction.done' event once compaction is finished.

You can also set automatic compaction at regular intervals with 'yourDatabase.persistence.setAutocompactionInterval(interval)', '
interval' in milliseconds (a minimum of 5s is enforced), and stop automatic compaction with 'yourDatabase.persistence.stopAutocompaction
()'.

Keep in mind that compaction takes a bit of time (not too much: 130ms for 50k records on a typical development machine) and no other
 operation can happen when it does, so most projects actually don't need to use it.

Compaction will also immediately remove any documents whose data line has become corrupted, assuming that the total percentage of
 all corrupted documents in that database still falls below the specified 'corruptAlertThreshold' option's value.

Durability works similarly to major databases: compaction forces the OS to physically flush data to disk, while appends to the data
 file do not (the OS is responsible for flushing the data). That guarantees that a server crash can never cause complete data loss
, while preserving performance. The worst that can happen is a crash between two syncs, causing a loss of all data between the two
 syncs. Usually syncs are 30 seconds appart so that's at most 30 seconds of data. <a href="http://oldblog.antirez.com/post/redis
-persistence-demystified.html" target="_blank">This post by Antirez on Redis persistence</a> explains this in more details, NeDB
 being very close to Redis AOF persistence with 'appendfsync' option set to 'no'.
...
```

#### <a name="apidoc.element.nedb.persistence.prototype.treatRawData"></a>[function <span class="apidocSignatureSpan">nedb.persistence.prototype.</span>treatRawData (rawData)](#apidoc.element.nedb.persistence.prototype.treatRawData)
- description and source-code
```javascript
treatRawData = function (rawData) {
  var data = rawData.split('\n')
    , dataById = {}
    , tdata = []
    , i
    , indexes = {}
    , corruptItems = -1   // Last line of every data file is usually blank so not really corrupt
    ;

  for (i = 0; i < data.length; i += 1) {
    var doc;

    try {
      doc = model.deserialize(this.beforeDeserialization(data[i]));
      if (doc._id) {
        if (doc.$$deleted === true) {
          delete dataById[doc._id];
        } else {
          dataById[doc._id] = doc;
        }
      } else if (doc.$$indexCreated && doc.$$indexCreated.fieldName != undefined) {
        indexes[doc.$$indexCreated.fieldName] = doc.$$indexCreated;
      } else if (typeof doc.$$indexRemoved === "string") {
        delete indexes[doc.$$indexRemoved];
      }
    } catch (e) {
      corruptItems += 1;
    }
  }

  // A bit lenient on corruption
  if (data.length > 0 && corruptItems / data.length > this.corruptAlertThreshold) {
    throw new Error("More than " + Math.floor(100 * this.corruptAlertThreshold) + "% of the data file is corrupt, the wrong beforeDeserialization
 hook may be used. Cautiously refusing to start NeDB to prevent dataloss");
  }

  Object.keys(dataById).forEach(function (k) {
    tdata.push(dataById[k]);
  });

  return { data: tdata, indexes: indexes };
}
```
- example usage
```shell
...
    function (cb) {
      Persistence.ensureDirectoryExists(path.dirname(self.filename), function (err) {
        storage.ensureDatafileIntegrity(self.filename, function (err) {
          storage.readFile(self.filename, 'utf8', function (err, rawData) {
if (err) { return cb(err); }

try {
  var treatedData = self.treatRawData(rawData);
} catch (e) {
  return cb(e);
}

// Recreate all indexes in the datafile
Object.keys(treatedData.indexes).forEach(function (key) {
  self.db.indexes[key] = new Index(treatedData.indexes[key]);
...
```



# <a name="apidoc.module.nedb.storage"></a>[module nedb.storage](#apidoc.module.nedb.storage)

#### <a name="apidoc.element.nedb.storage.appendFile"></a>[function <span class="apidocSignatureSpan">nedb.storage.</span>appendFile (path, data, options, callback_)](#apidoc.element.nedb.storage.appendFile)
- description and source-code
```javascript
appendFile = function (path, data, options, callback_) {
  var callback = maybeCallback(arguments[arguments.length - 1]);

  if (!options || typeof options === 'function') {
    options = { encoding: 'utf8', mode: 0o666, flag: 'a' };
  } else if (typeof options === 'string') {
    options = { encoding: options, mode: 0o666, flag: 'a' };
  } else if (typeof options !== 'object') {
    throwOptionsError(options);
  }

  if (!options.flag)
    options = util._extend({ flag: 'a' }, options);

  // force append behavior when using a supplied file descriptor
  if (isFd(path))
    options.flag = 'a';

  fs.writeFile(path, data, options, callback);
}
```
- example usage
```shell
...

 newDocs.forEach(function (doc) {
   toPersist += self.afterSerialization(model.serialize(doc)) + '\n';
 });

 if (toPersist.length === 0) { return callback(null); }

 storage.appendFile(self.filename, toPersist, 'utf8', function (err) {
   return callback(err);
 });
};


/**
* From a database's raw data, return the corresponding
...
```

#### <a name="apidoc.element.nedb.storage.crashSafeWriteFile"></a>[function <span class="apidocSignatureSpan">nedb.storage.</span>crashSafeWriteFile (filename, data, cb)](#apidoc.element.nedb.storage.crashSafeWriteFile)
- description and source-code
```javascript
crashSafeWriteFile = function (filename, data, cb) {
  var callback = cb || function () {}
    , tempFilename = filename + '~';

  async.waterfall([
    async.apply(storage.flushToStorage, { filename: path.dirname(filename), isDir: true })
  , function (cb) {
      storage.exists(filename, function (exists) {
        if (exists) {
          storage.flushToStorage(filename, function (err) { return cb(err); });
        } else {
          return cb();
        }
      });
    }
  , function (cb) {
      storage.writeFile(tempFilename, data, function (err) { return cb(err); });
    }
  , async.apply(storage.flushToStorage, tempFilename)
  , function (cb) {
      storage.rename(tempFilename, filename, function (err) { return cb(err); });
    }
  , async.apply(storage.flushToStorage, { filename: path.dirname(filename), isDir: true })
  ], function (err) { return callback(err); })
}
```
- example usage
```shell
...
  });
  Object.keys(this.db.indexes).forEach(function (fieldName) {
    if (fieldName != "_id") {   // The special _id index is managed by datastore.js, the others need to be persisted
      toPersist += self.afterSerialization(model.serialize({ $$indexCreated: { fieldName: fieldName, unique: self.db.indexes[fieldName
].unique, sparse: self.db.indexes[fieldName].sparse }})) + '\n';
    }
  });

  storage.crashSafeWriteFile(this.filename, toPersist, function (err) {
    if (err) { return callback(err); }
    self.db.emit('compaction.done');
    return callback(null);
  });
};
...
```

#### <a name="apidoc.element.nedb.storage.ensureDatafileIntegrity"></a>[function <span class="apidocSignatureSpan">nedb.storage.</span>ensureDatafileIntegrity (filename, callback)](#apidoc.element.nedb.storage.ensureDatafileIntegrity)
- description and source-code
```javascript
ensureDatafileIntegrity = function (filename, callback) {
  var tempFilename = filename + '~';

  storage.exists(filename, function (filenameExists) {
    // Write was successful
    if (filenameExists) { return callback(null); }

    storage.exists(tempFilename, function (oldFilenameExists) {
      // New database
      if (!oldFilenameExists) {
        return storage.writeFile(filename, '', 'utf8', function (err) { callback(err); });
      }

      // Write failed, use old version
      storage.rename(tempFilename, filename, function (err) { return callback(err); });
    });
  });
}
```
- example usage
```shell
...

  // In-memory only datastore
  if (self.inMemoryOnly) { return callback(null); }

  async.waterfall([
    function (cb) {
      Persistence.ensureDirectoryExists(path.dirname(self.filename), function (err) {
        storage.ensureDatafileIntegrity(self.filename, function (err) {
          storage.readFile(self.filename, 'utf8', function (err, rawData) {
if (err) { return cb(err); }

try {
  var treatedData = self.treatRawData(rawData);
} catch (e) {
  return cb(e);
...
```

#### <a name="apidoc.element.nedb.storage.ensureFileDoesntExist"></a>[function <span class="apidocSignatureSpan">nedb.storage.</span>ensureFileDoesntExist (file, callback)](#apidoc.element.nedb.storage.ensureFileDoesntExist)
- description and source-code
```javascript
ensureFileDoesntExist = function (file, callback) {
  storage.exists(file, function (exists) {
    if (!exists) { return callback(null); }

    storage.unlink(file, function (err) { return callback(err); });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nedb.storage.exists"></a>[function <span class="apidocSignatureSpan">nedb.storage.</span>exists (path, callback)](#apidoc.element.nedb.storage.exists)
- description and source-code
```javascript
exists = function (path, callback) {
  if (!nullCheck(path, cb)) return;
  var req = new FSReqWrap();
  req.oncomplete = cb;
  binding.stat(pathModule._makeLong(path), req);
  function cb(err, stats) {
    if (callback) callback(err ? false : true);
  }
}
```
- example usage
```shell
...
storage.mkdirp = mkdirp;


/**
 * Explicit name ...
 */
storage.ensureFileDoesntExist = function (file, callback) {
  storage.exists(file, function (exists) {
    if (!exists) { return callback(null); }

    storage.unlink(file, function (err) { return callback(err); });
  });
};
...
```

#### <a name="apidoc.element.nedb.storage.flushToStorage"></a>[function <span class="apidocSignatureSpan">nedb.storage.</span>flushToStorage (options, callback)](#apidoc.element.nedb.storage.flushToStorage)
- description and source-code
```javascript
flushToStorage = function (options, callback) {
  var filename, flags;
  if (typeof options === 'string') {
    filename = options;
    flags = 'r+';
  } else {
    filename = options.filename;
    flags = options.isDir ? 'r' : 'r+';
  }

  // Windows can't fsync (FlushFileBuffers) directories. We can live with this as it cannot cause 100% dataloss
  // except in the very rare event of the first time database is loaded and a crash happens
  if (flags === 'r' && (process.platform === 'win32' || process.platform === 'win64')) { return callback(null); }

  fs.open(filename, flags, function (err, fd) {
    if (err) { return callback(err); }
    fs.fsync(fd, function (errFS) {
      fs.close(fd, function (errC) {
        if (errFS || errC) {
          var e = new Error('Failed to flush to storage');
          e.errorOnFsync = errFS;
          e.errorOnClose = errC;
          return callback(e);
        } else {
          return callback(null);
        }
      });
    });
  });
}
```
- example usage
```shell
...
  , tempFilename = filename + '~';

async.waterfall([
  async.apply(storage.flushToStorage, { filename: path.dirname(filename), isDir: true })
, function (cb) {
    storage.exists(filename, function (exists) {
      if (exists) {
        storage.flushToStorage(filename, function (err) { return cb(err); });
      } else {
        return cb();
      }
    });
  }
, function (cb) {
    storage.writeFile(tempFilename, data, function (err) { return cb(err); });
...
```

#### <a name="apidoc.element.nedb.storage.mkdirp"></a>[function <span class="apidocSignatureSpan">nedb.storage.</span>mkdirp (p, opts, f, made)](#apidoc.element.nedb.storage.mkdirp)
- description and source-code
```javascript
function mkdirP(p, opts, f, made) {
    if (typeof opts === 'function') {
        f = opts;
        opts = {};
    }
    else if (!opts || typeof opts !== 'object') {
        opts = { mode: opts };
    }

    var mode = opts.mode;
    var xfs = opts.fs || fs;

    if (mode === undefined) {
        mode = _0777 & (~process.umask());
    }
    if (!made) made = null;

    var cb = f || function () {};
    p = path.resolve(p);

    xfs.mkdir(p, mode, function (er) {
        if (!er) {
            made = made || p;
            return cb(null, made);
        }
        switch (er.code) {
            case 'ENOENT':
                mkdirP(path.dirname(p), opts, function (er, made) {
                    if (er) cb(er, made);
                    else mkdirP(p, opts, cb, made);
                });
                break;

            // In the case of any other error, just see if there's a dir
            // there already.  If so, then hooray!  If not, then something
            // is borked.
            default:
                xfs.stat(p, function (er2, stat) {
                    // if the stat fails, then that's super weird.
                    // let the original error be the failure reason.
                    if (er2 || !stat.isDirectory()) cb(er, made)
                    else cb(null, made);
                });
                break;
        }
    });
}
```
- example usage
```shell
...
* Check if a directory exists and create it on the fly if it is not the case
* cb is optional, signature: err
*/
Persistence.ensureDirectoryExists = function (dir, cb) {
 var callback = cb || function () {}
   ;

 storage.mkdirp(dir, function (err) { return callback(err); });
};




/**
* Return the path the datafile if the given filename is relative to the directory where Node Webkit stores
...
```

#### <a name="apidoc.element.nedb.storage.readFile"></a>[function <span class="apidocSignatureSpan">nedb.storage.</span>readFile (path, options, callback_)](#apidoc.element.nedb.storage.readFile)
- description and source-code
```javascript
readFile = function (path, options, callback_) {
  var callback = maybeCallback(arguments[arguments.length - 1]);

  if (!options || typeof options === 'function') {
    options = { encoding: null, flag: 'r' };
  } else if (typeof options === 'string') {
    options = { encoding: options, flag: 'r' };
  } else if (typeof options !== 'object') {
    throwOptionsError(options);
  }

  var encoding = options.encoding;
  assertEncoding(encoding);

  var flag = options.flag || 'r';

  if (!nullCheck(path, callback))
    return;

  var context = new ReadFileContext(callback, encoding);
  context.isUserFd = isFd(path); // file descriptor ownership
  var req = new FSReqWrap();
  req.context = context;
  req.oncomplete = readFileAfterOpen;

  if (context.isUserFd) {
    process.nextTick(function() {
      req.oncomplete(null, path);
    });
    return;
  }

  binding.open(pathModule._makeLong(path),
               stringToFlags(flag),
               0o666,
               req);
}
```
- example usage
```shell
...
  // In-memory only datastore
  if (self.inMemoryOnly) { return callback(null); }

  async.waterfall([
    function (cb) {
      Persistence.ensureDirectoryExists(path.dirname(self.filename), function (err) {
        storage.ensureDatafileIntegrity(self.filename, function (err) {
          storage.readFile(self.filename, 'utf8', function (err, rawData) {
if (err) { return cb(err); }

try {
  var treatedData = self.treatRawData(rawData);
} catch (e) {
  return cb(e);
}
...
```

#### <a name="apidoc.element.nedb.storage.rename"></a>[function <span class="apidocSignatureSpan">nedb.storage.</span>rename (oldPath, newPath, callback)](#apidoc.element.nedb.storage.rename)
- description and source-code
```javascript
rename = function (oldPath, newPath, callback) {
  callback = makeCallback(callback);
  if (!nullCheck(oldPath, callback)) return;
  if (!nullCheck(newPath, callback)) return;
  var req = new FSReqWrap();
  req.oncomplete = callback;
  binding.rename(pathModule._makeLong(oldPath),
                 pathModule._makeLong(newPath),
                 req);
}
```
- example usage
```shell
...
      });
    }
  , function (cb) {
      storage.writeFile(tempFilename, data, function (err) { return cb(err); });
    }
  , async.apply(storage.flushToStorage, tempFilename)
  , function (cb) {
      storage.rename(tempFilename, filename, function (err) { return cb(err); });
    }
  , async.apply(storage.flushToStorage, { filename: path.dirname(filename), isDir: true })
  ], function (err) { return callback(err); })
};


/**
...
```

#### <a name="apidoc.element.nedb.storage.unlink"></a>[function <span class="apidocSignatureSpan">nedb.storage.</span>unlink (path, callback)](#apidoc.element.nedb.storage.unlink)
- description and source-code
```javascript
unlink = function (path, callback) {
  callback = makeCallback(callback);
  if (!nullCheck(path, callback)) return;
  var req = new FSReqWrap();
  req.oncomplete = callback;
  binding.unlink(pathModule._makeLong(path), req);
}
```
- example usage
```shell
...
/**
* Explicit name ...
*/
storage.ensureFileDoesntExist = function (file, callback) {
 storage.exists(file, function (exists) {
   if (!exists) { return callback(null); }

   storage.unlink(file, function (err) { return callback(err); });
 });
};


/**
* Flush data in OS buffer to storage if corresponding option is set
* @param {String} options.filename
...
```

#### <a name="apidoc.element.nedb.storage.writeFile"></a>[function <span class="apidocSignatureSpan">nedb.storage.</span>writeFile (path, data, options, callback_)](#apidoc.element.nedb.storage.writeFile)
- description and source-code
```javascript
writeFile = function (path, data, options, callback_) {
  var callback = maybeCallback(arguments[arguments.length - 1]);

  if (!options || typeof options === 'function') {
    options = { encoding: 'utf8', mode: 0o666, flag: 'w' };
  } else if (typeof options === 'string') {
    options = { encoding: options, mode: 0o666, flag: 'w' };
  } else if (typeof options !== 'object') {
    throwOptionsError(options);
  }

  assertEncoding(options.encoding);

  var flag = options.flag || 'w';

  if (isFd(path)) {
    writeFd(path, true);
    return;
  }

  fs.open(path, flag, options.mode, function(openErr, fd) {
    if (openErr) {
      callback(openErr);
    } else {
      writeFd(fd, false);
    }
  });

  function writeFd(fd, isUserFd) {
    var buffer = (data instanceof Buffer) ?
        data : Buffer.from('' + data, options.encoding || 'utf8');
    var position = /a/.test(flag) ? null : 0;

    writeAll(fd, isUserFd, buffer, 0, buffer.length, position, callback);
  }
}
```
- example usage
```shell
...
        storage.flushToStorage(filename, function (err) { return cb(err); });
      } else {
        return cb();
      }
    });
  }
, function (cb) {
    storage.writeFile(tempFilename, data, function (err) { return cb(err); });
  }
, async.apply(storage.flushToStorage, tempFilename)
, function (cb) {
    storage.rename(tempFilename, filename, function (err) { return cb(err); });
  }
, async.apply(storage.flushToStorage, { filename: path.dirname(filename), isDir: true })
], function (err) { return callback(err); })
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
