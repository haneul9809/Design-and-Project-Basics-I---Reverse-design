# Design-and-Project-Basics-I---Reverse-design
똑똑한 우리집(Smart Home)
## 발표 영상 링크
https://youtu.be/TYO0KbbRAI8
## 역설계 최종 보고서
https://konyang-my.sharepoint.com/:t:/g/personal/19615050_konyang_ac_kr/EYdGnu11bsVPl6TjVZjY47UBGzq_GhAsjecAof3DAxOPPg?e=k4m1D6

## 🗓️ 개발 기간

2020/3/14 ~ 2020/4/13
## 📜서비스 내용

- 문제 제기
    - 사물인터넷(IoT : Internet of Things)는 사물간 통신을 통해 수집되는 방대한 데이터를 기반으로 새로운 형태의 서비스를 창출할 수 있다.
        - 국내외의 IoT 시장 추세는 점점 더 증가하고 있고 가정, 교통, 의료 등 다양한 분야에 활용되고 있다.
        - 스마트홈(Smart Home)은 집과 IoT를 융합하여 사용자가 집안의 다양한 장치를 제어할 수 있는 서비스이다.
        - IoT 기술을 이용하여 사용자 중심의 스마트홈 플랫폼을 구축하고자 이 작품을 설계하였다
        
        ![Untitled1](https://user-images.githubusercontent.com/67767912/204736299-9b912b34-a16d-475b-a78d-9351ebc7b481.png)

        
    
    ![Untitled2](https://user-images.githubusercontent.com/67767912/204736353-d4e7dc10-ea46-420c-84ef-56a958ec8e33.png)

    
- 문제 해결(기능과 기대효과)
    - 다양한 홈 IoT 기기를 설계할 수 있다.
    - IoT 장치를 개별 제어를 할 수 있다
    - 외부서버를 통한 원격 제어를 할 수 있다.
    - 가정에서 사용하는 상용전원을 이해하고 통제할 수 있다.
    - 실제 블라인드 구현을 통해 모터의 종류와 특성을 이해할 수 있다.
    - 와이파이 모듈을 통해 센서 값을 전송하고 웹에 표시할 수 있다.

## ⚙️ 기술 스택

- 스마트홈 홈페이지
    - SW
        - HTML
- 스마트 멀티탭
    - HW
        - Raspberry PI, Arduino, AC-DC Converter(전압 변경), Wifi Module(통신), Arduino Relay Module, Arduino Current module(전류 측정)
    - SW
        - C, C++
- 스마트 온습도 조절기
    - HW
        - 아두이노 UNO, ESP8266, 서미스터, 습도 센서(DHT22), DC 모터
    - SW
        - C, C++
- 스마트 무드등
    - HW
        - 아두이노 UNO(atmega328, 단일 칩 마이크로 컨트롤러), 시리얼 와이파이 모듈, 릴레이 모듈, 네오픽셀, 어답터, dc잭
    - SW
        - C, C++, HTML

## 👫 팀 구성

![Untitled3](https://user-images.githubusercontent.com/67767912/204736383-43f6302d-6d57-4704-86ee-03cf5441a6a6.png)

## 💻 개발 내용

1. 시스템 블록 다이어그램(System Block Diagram)
    
    ![Untitled4](https://user-images.githubusercontent.com/67767912/204736421-8a8e0e6d-88cb-4f0f-b434-19ed84f4eadb.png)

2. 스마트 멀티탭
    
    ![Untitled5](https://user-images.githubusercontent.com/67767912/204736447-2b56ef32-1c1f-4698-92cd-edbdeca9ee5d.png)

    ![Untitled6](https://user-images.githubusercontent.com/67767912/204736474-42c22e56-e82e-4ef5-837c-d7c02b36354d.png)

    
    
3. 스마트 온습도 조절기
    
    ![Untitled7](https://user-images.githubusercontent.com/67767912/204736514-c1950771-9853-40f7-9383-b42ff0660878.png)
![Untitled8](https://user-images.githubusercontent.com/67767912/204736525-46b4e535-ae9a-40b3-ba32-3f6510d44b83.png)
![Untitled9](https://user-images.githubusercontent.com/67767912/204736528-900f369e-97fb-4407-8c8e-85a7193e1eef.png)

    
4. 스마트 무드등
    
    ![Untitled10](https://user-images.githubusercontent.com/67767912/204736571-b3536cd8-2dfa-4f24-9366-e4feaba52c9e.png)
    ![Untitled11](https://user-images.githubusercontent.com/67767912/204736607-083d3c0e-a2cc-4362-a210-f4b126c832b5.png)
    ![Untitled12](https://user-images.githubusercontent.com/67767912/204736639-154850a2-28b3-4881-aa4a-182945ae760e.png)

    
    - 스마트 무드등 시작을 하면 제품 전원을 다룰 수 있게 됩니다.
        - 제품 전원은 웹이나 앱으로 다루게 되는데 웹과 앱이 어떻게 제품을 다루게 되는지는 잠시 후에 다른 플로우 차트를 보면서 설명하도록 하겠습니다.
    - 제품 전원을 다룰 때 전원을 켜면 전력이 공급되고 전원을 켜지 않으면 다시 시작으로 돌아가게 됩니다.
    - 전원을 켰을 시에 전력이 공급되면 현재 구동이 되고 있었는지 확인하게 됩니다.
    - 전원을 컨트롤 할 수 있는 상황이라면 전원 on을 선택하면 전등이 켜지게 되며 전원 off를 선택하면 플로우 차트가 종료되게 됩니다.
    
    ![Untitled13](https://user-images.githubusercontent.com/67767912/204736627-10715cb2-cb77-455d-8866-5125677a5c67.png)
    ![Untitled14](https://user-images.githubusercontent.com/67767912/204736641-a4956ba1-e87b-4494-893a-1e8ffe38b5e4.png)

    
    - 무드등 시스템, 스마트폰, 조명 플로우 차트와 다이어그램을 같이 보면 처음엔 제품과 유무선 공유기를 연결합니다.
    - 이동 통신 단말기인 스마트폰을 시작하고 유무선 통신망에 접속합니다.
    - 제품 전원을 제어하게 되는데 제품을 끄는 것을 선택하면 스마트폰의 시작 화면으로 돌아가게 되고 제품을 켜는 것을 선택하면 조명에 전력이 공급되고 조명의 구동 상태를 확인한 후전등을 제어할 수 있는 화면으로 넘어가게 됩니다.
    - 전등을 끄는 것을 선택하면 아무런 설정 없이 초기화된 상태로 조명이 꺼진 후 종료 화면으로 넘어갑니다.
    - 전등을 켜는 것을 선택하면 전등이 켜진 후 밝기 조절, 전등 색상 변경, 알람 설정이 가능한 화면으로 넘어갑니다. 이 화면에서 제어한 모든 값은 모두 유무선 통신망으로 공유되고 스마트폰과 조명의 플로우 차트와 끝나게 되며 이 모든 값은 데이터 베이스에 저장됩니다.
    
    ![Untitled15](https://user-images.githubusercontent.com/67767912/204736761-29fb4ec4-b585-4701-887f-659af56f170c.png)
![Untitled16](https://user-images.githubusercontent.com/67767912/204736772-901e4aae-a3e1-46ef-b2e2-db17a759647c.png)

    
5. 어플리케이션 구성
    <img width="801" alt="스크린샷 2022-11-30 오후 4 31 55" src="https://user-images.githubusercontent.com/67767912/204736814-00b023d2-0750-469a-ac06-cdaf424a7646.png">

        
    <img width="796" alt="스크린샷 2022-11-30 오후 4 32 57" src="https://user-images.githubusercontent.com/67767912/204736921-37c4511f-a9fb-4d3d-a727-76561671e914.png">

    
- 선배님들의 작품을 역설계하여 작품에 선배님들의 이름이 적혀있습니다.

## 💻 내가 담당한 파트

[스마트 무드등](https://www.notion.so/bd2b65834f4f410c8457b65d1d75e8cb) 
<img width="801" alt="스크린샷 2022-11-30 오후 4 33 27" src="https://user-images.githubusercontent.com/67767912/204736955-6a3c031e-1502-4bcc-86b2-051e5498d319.png">



## ✏️후기 및 에세이

역설계와 본설계를 진행하며 라즈베리파이를 사용하여 IoT 기기를 만드는 방법과 아두이노에 대해 이해하고 연동하는 방법을 알 수 있었다.
