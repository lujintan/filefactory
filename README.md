# filefactory
generate files by the sample files

###Installation

```base
npm install -g filefactory
```

###Example：

Goto the test folder and execute

```base
ffy -c config.json
```

###Usage

```base
ffy --help
```

```console
Usage: ffy ffy -s <sample> -d <delimiter> -t <target> -c <config>

Options:

    -h, --help              output usage information
    -V, --version           output the version number
    -s, --sample [type]     The sample file
    -d, --delimiter [type]  the template delimiter(optional), default is %
    -t, --target [type]     generate to this target path
    -c, --config [type]     the template's datasource, must be a .js or .json file
```

###Config Options

```javascript
module.exports = {
    //sample file or folder
    "sample": "./sample/",
    //Character to use with angle brackets for open/close
    "delimiter": "./delimiter",
    //File or folder name to generate files
    "dest": "./filefactory_dest",
    //filter could be a Function or RegeExp string
    //if filter return true filefactory will render file by ejs(a template engine) and data(configed in this file)
    "filter": "\\.(js|css|coffee|json|tpl|txt)",
    //the data file 
    "data": {
        "a": 1,
        "b": 2
    }
}
```

###Related projects

* The usage of ejs: [https://github.com/mde/ejs](https://github.com/mde/ejs)