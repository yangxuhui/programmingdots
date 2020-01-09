# Programming Dots
## 消息/任务队列
### [beanstalkd](https://github.com/beanstalkd/beanstalkd)
#### Tube
> The "ignore" command will reply "NOT_IGNORED\r\n" if the client attempts to ignore the only tube in its watch list.
#### [Client Libraries](https://github.com/beanstalkd/beanstalkd/wiki/Client-Libraries)
## 监控
### [Metrics](https://metrics.dropwizard.io/3.1.0/getting-started/)
#### Client Libraries
* java
    * [metrics](https://github.com/dropwizard/metrics)
* python
    * [pyformance](https://github.com/omergertel/pyformance)
## Docker
## Signal Handle
### python
* Add signal handler:`signal.signal(signal.SIGALRM, handler)`
* Stop threads using [Event](https://docs.python.org/3/library/threading.html#event-objects)
```python
class App:
    def __init__(self):
        self._stop = threading.Event()
    
    def worker(self):
        while not self._stop.is_set():
            ...
    
    def stop(self):
        self._stop.set()
```
## Code Complexity Analysis Tool
### python
#### [wily](https://github.com/tonybaloney/wily)
## Design Patterns
### Creational Patterns
#### Singleton
* 应用场景
    * 显式确保某个类的对象有且仅有一个
* 实现方式
    * 将构造函数声明为私有成员函数，创建一个静态方法来进行对象的创建
    * [How to implement a configurable singleton?](https://stackoverflow.com/questions/34642170/how-to-implement-a-configurable-singleton)
## Programming Languages
### golang
#### [`init`](https://golang.org/doc/effective_go.html#init)
### python
* `@staticmethod` vs `@classmethod`
## Caches
### In Memory Caches
[guava caches](https://github.com/google/guava/wiki/CachesExplained)给出了in-memory cache的典型应用方式 
* From a CacheLoader
* From a Callable
* Inserted Directly
#### Libraries
* java
    * [guava caches](https://github.com/google/guava/wiki/CachesExplained)
* golang
    * [Mango Cache](https://github.com/goburrow/cache)
## 包管理
### python
* [Packaging and distributing projects](https://packaging.python.org/guides/distributing-packages-using-setuptools/)
## CLIs
* python
    * [python-fire](https://github.com/google/python-fire)
## OOP
### Object References
* Reference Variables are not boxes, it's better to think of them as labels attached to objects.
* Identity, Equality, Aliases
    * python
        * `==` means equality
        * `is` means identity
* Copies Are Shallow by Default
### Access Privileges
> “In Python, there is no way to create private variables like there is with the private modifier in Java.”
### Static Member
### Interfaces
> “An interface seen as a set of methods to fulfill a role is what Smalltalkers called a procotol”

> “Protocols are interfaces, but because they are **informal—defined** only by documentation and conventions—protocols cannot be enforced like formal interfaces can”

> “A protocol may be partially implemented in a particular class, and that’s OK”
