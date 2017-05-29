# jsonawk

- awk style json line processor(use js code)
- support awk style: $ BEGIN END
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
cat file.json | jsonawk 'console.log($.name)'
torvalds
tj
```


use lodash
```sh
cat file.json | jsonawk 'console.log(_.join([$.name, "making the world better"], " "))'
torvalds making the world better
tj making the world better
```

use BEGIN,END
```sh
cat file.json | jsonawk 'BEGIN{var n=0;}{n++;console.log(_.join([$.name, "making the world better"], " "))  }END{console.log(n)}' 
torvalds making the world better
tj making the world better
2
```
# todo
- contact al@xfruit.cn

