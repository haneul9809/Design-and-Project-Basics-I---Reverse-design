# Design-and-Project-Basics-I---Reverse-design
똑똑한 우리집(Smart Home)
## 발표 영상 링크
https://youtu.be/TYO0KbbRAI8

## 🗓️ 개발 기간

2020/3/2 ~ 2020/4/19

## 📜서비스 내용

- 문제 제기
    - 사물인터넷(IoT : Internet of Things)는 사물간 통신을 통해 수집되는 방대한 데이터를 기반으로 새로운 형태의 서비스를 창출할 수 있다.
        - 국내외의 IoT 시장 추세는 점점 더 증가하고 있고 가정, 교통, 의료 등 다양한 분야에 활용되고 있다.
        - 스마트홈(Smart Home)은 집과 IoT를 융합하여 사용자가 집안의 다양한 장치를 제어할 수 있는 서비스이다.
        - IoT 기술을 이용하여 사용자 중심의 스마트홈 플랫폼을 구축하고자 이 작품을 설계하였다
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9a45fc2b-aa53-4caa-a86f-c54d72487822/Untitled.png)
        
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d14c6561-7ee8-4700-b4bd-22a0a6507412/Untitled.png)
    
    - 혈압의 결정 요인은 심장의 수축과 확장 기능에 의해 뿜어져 나오는 혈액량과 혈관의 직경에 따른 문제가 있다. 혈압은 위의 표와 같이 정상 혈압과 고혈압으로 구분할 수 있다.
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

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f52f7b3c-92d1-42e0-b9f1-d15ce00072cb/Untitled.png)

## 💻 개발 내용

1. 시스템 블록 다이어그램(System Block Diagram)
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/74572f68-ec27-44eb-a26e-a50b81e486f9/Untitled.png)
    
2. 스마트 멀티탭
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/565ecd76-3db8-4d5e-b65d-6c2eae0355f7/Untitled.png)
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/81a06945-ebd0-4d50-b538-7856eb2b9112/Untitled.png)
    
3. 스마트 온습도 조절기
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b7d028cd-5a26-45ed-ab66-7e89da2e9751/Untitled.png)
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6cbe64db-ce9f-42f7-94f3-6047f9ad1b37/Untitled.png)
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6271a392-732b-48f1-9a11-bae18564f9bc/Untitled.png)
    
4. 스마트 무드등
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7cc692d4-cd20-49cf-8667-92c9fe4a804a/Untitled.png)
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/06403900-275c-4979-a413-e5932101e534/Untitled.png)
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b5097bef-deca-4326-8bf9-9e7bcbc997d0/Untitled.png)
    
    - 스마트 무드등 시작을 하면 제품 전원을 다룰 수 있게 됩니다.
        - 제품 전원은 웹이나 앱으로 다루게 되는데 웹과 앱이 어떻게 제품을 다루게 되는지는 잠시 후에 다른 플로우 차트를 보면서 설명하도록 하겠습니다.
    - 제품 전원을 다룰 때 전원을 켜면 전력이 공급되고 전원을 켜지 않으면 다시 시작으로 돌아가게 됩니다.
    - 전원을 켰을 시에 전력이 공급되면 현재 구동이 되고 있었는지 확인하게 됩니다.
    - 전원을 컨트롤 할 수 있는 상황이라면 전원 on을 선택하면 전등이 켜지게 되며 전원 off를 선택하면 플로우 차트가 종료되게 됩니다.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/17c8266b-bbc8-40a8-8e64-a03ada4653fd/Untitled.png)
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/90f5f2a2-fac5-4cf1-bc92-f70bb0f41850/Untitled.png)
    
    - 무드등 시스템, 스마트폰, 조명 플로우 차트와 다이어그램을 같이 보면 처음엔 제품과 유무선 공유기를 연결합니다.
    - 이동 통신 단말기인 스마트폰을 시작하고 유무선 통신망에 접속합니다.
    - 제품 전원을 제어하게 되는데 제품을 끄는 것을 선택하면 스마트폰의 시작 화면으로 돌아가게 되고 제품을 켜는 것을 선택하면 조명에 전력이 공급되고 조명의 구동 상태를 확인한 후전등을 제어할 수 있는 화면으로 넘어가게 됩니다.
    - 전등을 끄는 것을 선택하면 아무런 설정 없이 초기화된 상태로 조명이 꺼진 후 종료 화면으로 넘어갑니다.
    - 전등을 켜는 것을 선택하면 전등이 켜진 후 밝기 조절, 전등 색상 변경, 알람 설정이 가능한 화면으로 넘어갑니다. 이 화면에서 제어한 모든 값은 모두 유무선 통신망으로 공유되고 스마트폰과 조명의 플로우 차트와 끝나게 되며 이 모든 값은 데이터 베이스에 저장됩니다.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ddb8a3e0-ea17-48f1-a9f8-b04182d8a3ac/Untitled.png)
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5d4c9f85-0d72-482f-a312-77c546de4ed8/Untitled.png)
    
5. 어플리케이션 구성
    
    ![스크린샷 2022-11-30 오후 4.31.55.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/010b7f10-354b-4a16-89f1-ac9051009e0e/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2022-11-30_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_4.31.55.png)
    
    ![스크린샷 2022-11-30 오후 4.32.57.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ef1fc097-1d22-4319-bd1a-4a100e3bdf1e/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2022-11-30_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_4.32.57.png)
    
- 선배님들의 작품을 역설계하여 작품에 선배님들의 이름이 적혀있습니다.

## 💻 내가 담당한 파트

[스마트 무드등](https://www.notion.so/bd2b65834f4f410c8457b65d1d75e8cb) 

![스크린샷 2022-11-30 오후 4.33.27.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/86ece6fe-07f5-46ab-a73f-0426b5e82a97/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2022-11-30_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_4.33.27.png)

## ✏️후기 및 에세이

역설계와 본설계를 진행하며 라즈베리파이를 사용하여 IoT 기기를 만드는 방법과 아두이노에 대해 이해하고 연동하는 방법을 알 수 있었다.
