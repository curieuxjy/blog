---
toc: true
layout: post
description: custom module을 불러오는 방법
categories: [python]
title: An Example Markdown Post
---

Python: custom module을 불러오는 방법

## Structure

![folder_img](./imgs/img4.JPG)
![xmind_img](./imgs/img5.JPG)

`gym_foo` folder에 반드시 `__init__.py`를 만들어야 한다.

## Code
* `utils_foo.py`
```python
def utils_test():
    print("utils_foo")

print("HERE: utils_foo")
```

* `env_foo.py`
```python
from gym_foo import utils_foo

utils_foo.utils_test()

print("HERE: env_foo")

def env_test():
    print("env_foo") 
```

* `main_foo.py`
```python
from gym_foo import utils_foo
from gym_foo import env_foo

utils_foo.utils_test()
env_foo.env_test()
```

## Goal
* 실행 파일: `main_foo.py`
* import하는 파일: `env_foo.py`
* **import하는 파일 내에서(=env_foo.py)** import하는 파일: `utils_foo.py`

## How
* `main_foo.py`에서 `env_foo.py`를 import한다.
* `env_foo.py`에서 `utils_foo.py`를 import 한다.
* 이때 `env_foo.py`에서 `import utils_foo`로 utils_foo를 불러오면,
    * `python env_foo.py` 실행시 잘 작동되지만(같은 위치)
    * `python main_foo.py` 실행에서는 `from gym_foo import *`코드를 읽을 때 `env_foo.py`내의 `from gym_foo import utils_foo`를 불러올 수 없다고 error가 난다.(상위 위치)

```cmd
$ python main_foo.py 
Traceback (most recent call last):
File "main_foo.py", line 4, in <module>
    env_foo.env_test()
NameError: name 'env_foo' is not defined
``` 

* env_foo.py에서 utils_foo module을 불러올 때, `from gym_foo import utils_foo`로 불러온다. 상위 위치인 `gym_foo`를 거쳐서 import해야한다는 뜻이다. 그러면 `python main_foo.py` 실행시 잘 작동한다.

```cmd
$ python main_foo.py 
HERE: utils_foo
utils_foo
HERE: env_foo
utils_foo
env_foo
```

* 한 가지 더 주의해야할 점이 있다. `main_foo.py`에서 `utils_foo`와 `env_foo`를 import 할 때이다.

    `from gym_foo import *` 코드로 utils_foo와 env_foo가 모두 불러와질 것이라고 생각했으나, `main_foo.py`를 실행했을 때 import 하지 못한다. 따라서 위에 `main_foo.py`에서 볼 수 있듯이 `from gym_foo import utils_foo`, `from gym_foo import env_foo`각각 따로 import 해줘야 한다.


