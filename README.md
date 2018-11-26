```js
//index.js
 
Page({
    data: {
        my:{
            name:"xuyang",
            age:21
        }
    },
    onLoad(){
        getApp().setWatcher(this.data, this.watch);
        this.data.my.name = 'lxm';
        this.data.my.age = 2;
        this.setData({
            my: this.data.my
        })
    },
    watch:{
        'my.name':function(newValue){
            console.log(newValue);
        },
        'my.age':function(newValue){
            console.log(newValue);
        }
    }
})

```
