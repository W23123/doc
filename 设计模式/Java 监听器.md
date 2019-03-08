# Java 监听器

#### 模型
监听器涉及3个对象
- 事件：用户对组件的一个操作，称为事件
- 事件源：发生事件的组件
- 事件监听器：监听并负责处理事件的方法

事件源注册到监听器，组件被外部事件触发，产生一个相应的事件对象，并把对象传递给与之关联的事件处理器，事件处理器启动，并执行相关的代码来处理事件

#### 实现

具体实现UML类图
	

事件

```java
public interface IEvent {
    void setEventListener(IEventListener listener);
}
```
事件监听

```java
public interface IEventListener {
    void doEvent(IEvent event);
}
```

事件源

```java
public class ButtonEventSource implements IEvent {

    private IEventListener listener;

    @Override
    public void setEventListener(IEventListener listener) {
        this.listener = listener;
    }

    public void buttonEventHappened() {
        listener.doEvent(this);
    }
}

public class MouseEventSource implements IEvent {

    private IEventListener listener;

    @Override
    public void setEventListener(IEventListener listener) {
        this.listener = listener;
    }

    public void mouseEventHappened() {
        listener.doEvent(this);
    }
}
```

测试

```java
public static void main(String[] args) {

        IEventListener listener = event -> {
            if(event instanceof ButtonEventSource){
                System.out.println("您点击了button！");
            }else if (event instanceof MouseEventSource){
                System.out.println("您移动了鼠标！");
            }

        };

        ButtonEventSource buttonEventSource = new ButtonEventSource();
        buttonEventSource.setEventListener(listener);
        buttonEventSource.buttonEventHappened();

        MouseEventSource mouseEventSource = new MouseEventSource();
        mouseEventSource.setEventListener(listener);
        mouseEventSource.mouseEventHappened();
}
```


后面可以对listenter进行管理，方便操作。（第2个实现，以及类图）

![listener2.png](quiver-image-url/63006272670B392DB29DECB708C88DF4.png)


```java
public class ListenerManager {

    private Collection listeners;

    public void addListener(DEventListener listener) {
        if (listeners == null) {
            listeners = new HashSet();
        }
        listeners.add(listener);
    }

    public void removeListener(IEventListener listener) {
        if (listeners == null) return;
        listeners.remove(listener);
    }

    

    public void doEvent(String event) {
        if (listeners==null) return;
        DEvent dEvent = new DEvent(this,event);
        notifyListeners(dEvent);
    }

    public void notifyListeners(DEvent event) {
        Iterator iterator = listeners.iterator();
        while (iterator.hasNext()){
            DEventListener eventListener = (DEventListener) iterator.next();
            eventListener.doEvent(event);
        }
    }


}
```

github地址：[https://github.com/dongbinmu/design-pattern-demo](https://github.com/dongbinmu/design-pattern-demo)

参考  [https://blog.csdn.net/tfygg/article/details/51638933](https://blog.csdn.net/tfygg/article/details/51638933)