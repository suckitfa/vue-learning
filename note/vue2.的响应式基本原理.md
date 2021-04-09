```js
function obse
function defineReactive(data,key,value) {
    Object.defineProperty(data,key,{
        observe(value);//递归的劫持
        get() {
            return this.value
        },
        set(newValue) {
            if (this.value !== newValue) {
                this.value = newValue;
            }
        }
    });
}
```