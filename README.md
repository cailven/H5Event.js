# H5Event.js

## 介绍

在HTML5项目中，我们追求精简极致的文件尺寸，因此我做了一个极简事件处理组件。建议把该组件初始化在window下或者某单例等全局环境内。


## 使用方法：

```javascript

//在全局的地方创建管理器
    var h5Event = new H5Event();

//在需要更新的地方加上监听
    h5Event.on("test", function () {
            console.log(e);
            console.log(e.data);
            //收数据

           alert("this is a test")
       })

//在其他地方发出事件
    h5Event.trigger({
            type: "test",
            data: ["test1", "test2", "test3"]
            //发数据
        });

//在不需要的时候卸载掉
     h5Event.off("test", function () {
           alert("this is a test")
       })

```

## API:
- on(event,function);
监听事件

- trigger({type:event});
发送事件

- off(event,function);
删除监听





