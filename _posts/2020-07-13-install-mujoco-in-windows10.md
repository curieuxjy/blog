---
toc: true
layout: post
description: Window10에서 mujoco 설치하기
categories: [mujoco]
title: Install Mujoco in Window10
---

Reinforcement learning에서 많이 쓰이는 시뮬레이션 Mujoco Window10에 설치하기

# Mujoco 
1. [Mujoco](http://www.mujoco.org/index.html)에서 [License](https://www.roboti.us/license.html) tab으로 들어가서 Personal Student Software License를 받는다.

2. 이메일로 Account number를 받는다.(spam도 확인하자)

3. 다시 [License](https://www.roboti.us/license.html)로 가서 Account number와 Computer Id를 입력한다.

    ![license_img](imgs/img2.JPG)

4. 다시 이메일로 MuJoCo Pro Personal Activation Key(mjkey.txt)를 받는다.

5. `.mujoco`라는 파일을 `C:\Users\사용자명\`에 만든다.

6. [Products](https://www.roboti.us/index.html)에서 `mjpro150 win64`을 다운받아 `.mujoco`에 압축을 풀어준다.(`C:\Users\사용자명\.mujoco\mjpro150`)

    ![product_img](imgs/img3.JPG)

6. 다운받은 mjkey.txt 파일을 `C:\Users\사용자명\.mujoco`와 `C:\Users\사용자명\.mujoco\mjpro150\bin` 에 옮긴다.

7. cmd창을 열어서 cd 명령어로 `C:\Users\사용자명\.mujoco\mjpro150\bin` 경로로 이동한 다음 `simulate ../model/humanoid.xml`명령어를 입력한다.

8. Humanoid Simulation 창이 나오면 성공이다.

    ![humanoid_gif](imgs/gif2.gif)

# Mujoco-py

1. `SET PATH=C:\Users\사용자명\.mujoco\mjpro150\bin;%PATH%;`으로 경로설정을 해준다.

2. [mujoco-py-1.50.1.0](https://github.com/openai/mujoco-py/archive/1.50.1.0.zip) 파일을 다운받아 `C:\Users\사용자명\.mujoco`에 압축을 풀어준다.(`C:\Users\사용자명\.mujoco\mujoco-py-1.50.1.0`)

3. cmd 창에서 `python setup.py install`를 입력하여 설치한다.

    `C:\Users\사용자명\.mujoco\mujoco-py-1.50.1.0> python setup.py install`
    
    혹시 여기서 error가 난다면 전에 mujoco-py를 설치해서 버젼이 안 맞아 나는 것일 수도 있다. `pip list`로 `mujoco-py`의 버젼을 확인해보고 다른 버젼이라면 `pip uninstall mujoco-py`를 해준후 다시 설치한다.
    
4. cmd 창에서 `python examples\body_interaction.py`를 입력하여 잘 실행되는지 확인한다.

    `C:\Users\사용자명\.mujoco\mujoco-py-1.50.1.0> python examples\body_interaction.py`
    
    처음에 실행화면이 뜨는 시간이 오래걸리지만 이후에는 실행창이 빨리 나왔다.
    
    ![body_gif](imgs/gif1.gif)


### Reference
* [MuJoCo 설치 (윈도우 10 version)](https://seunghyun-lee.tistory.com/2)

