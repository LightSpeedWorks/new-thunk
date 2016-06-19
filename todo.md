### Thunk.all(iterable or array)

wait for all promises.

```js
thunk = Thunk.all([thunk, ...]);
```

### Thunk.race(iterable or array)

get value or error of first finished thunk.

```js
thunk = Thunk.race([thunk, ...]);
```

### Thunk.resolve(value or thunk)

get resolved thunk.

```js
thunk = Thunk.resolve(value or thunk);
```

### Thunk.reject(error)

get rejected thunk.

```js
thunk = Thunk.reject(error);
```

### Thunk.accept(value)

get resolved (accepted) thunk.

```js
thunk = Thunk.accept(value);
```

# LICENSE:

  MIT
