# H5Event.js

## 介绍

在HTML5项目中，我们追求精简极致的文件尺寸，因此我做了一个极简事件处理组件。


## 使用方法：

```javascript

//在全局的地方创建管理器
    var h5Event = new H5Event();

//在需要更新的地方加上监听
    h5Event.addEvent("test", function () {
           alert("this is a test")
       })

//在其他地方发出事件
    h5Event.fireEvent({
            type: "test"
        });

//在不需要的时候卸载掉
     h5Event.removeEvent("test", function () {
           alert("this is a test")
       })

```

## API:
- addEvent(event,function);
监听事件

- fireEvent({type:event});
发送事件

- removeEvent(event,function);
删除监听





