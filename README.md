# jsonawk

- awk style json line processor
- use js code
- support loadash: _

# installation
```sh
npm install -g jsonawk
```

# usage
file.json
```
{"userid":"001","name":"torvalds"}
{"userid":"002","name":"tj"}
```

```sh
cat file.json | ./jsonawk 'console.log(data.name))'
torvalds
tj
```


use lodash
```sh
cat file.json | ./jsonawk 'console.log(_.join([data.name, "making the world better"], " "))'
torvalds making the world better
tj making the world better
```

# todo
- awk style BEGIN
- awk style END