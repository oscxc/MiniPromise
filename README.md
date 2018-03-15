#  MiniPromise


## Source code

```
function MiniPromise(fn) {
    this.then = function (cb) {
        fn(cb)
    }
}
```

## Usage

```
function wait(){
    return new MiniPromise(function(cb){
        setTimeout(function(){
            cb('value1','value2')
        },1000)
    })
}
```
```
wait().then(function(value1,value2){
    console.log(value1)
    console.log(value2)
})
```