





## 2. 집

* Android 접속

1. 인체감지센서: 집 안 거실에 설치. 거실에서 사람을 감지했을 때 LED 조명이 켜진다.
   * 주인이 집 안에 들어갈 때 RFID 태그를 리더기에 접근하고, 출입 승인을 받아 인체감지센서를 해제시킨 후 들어간다.
   * 주인이 나갈 때 다시 한 번  RFID 태그를 리더기에 찍어 인체감지센서를 동작시킨 후 나간다.

2. 조도센서: 거실과 부엌에 설치.  조도센서 값에 따라 LED 밝기 제어 

* 자동모드: 조도 센서가 주변 밝기를 감지하여
  * 주변이 어두우면 LED밝기를 올려주고
  * 주변이 밝으면 LED밝기를 낮추어준다.
* 수동모드: 안드로이드의 프로그레스 바에 의해 LED 밝기를 0-9 사이까지 조절해준다.
  * 프로그레스 바가 0이면 LED가 완전히 꺼진 상태이고
  * 프로그레스 바가 9이면 LED가 완전히 켜진 상태이다.

3. 온습도 센서: 거실과 부엌 사이에 설치.

   * 온도와 습도값을 TCP/IP 서버를 통해  핸드폰에 보내주어 실시간 모니터링

   * 희망온도를 안드로이드에서 설정하여 측정된 온도가 희망온도보다 높으면 DC모터 선풍기가 작동되어서 희망온도까지 낮추어준다.

4. 가스 센서: 부엌에 설치. 부탄가스나 에탄올을 감지하기에 에탄올로 테스트

   * 가스 센서가 에탄올을 감지하면: 가스벨브 잠금잠치(서보모터)가 움직여 벨브가 잠기고 핸드폰에 가스누출 알람 메시지가 울린다.

   - 가스누출 알람 메시지는 Android Immortal Service(안드로이드 죽지않는 서비스)를 적용하여 앱이 닫혀도 백그라운드에서 작동이 된다. 

5. 불꽃 감지 센서: 부엌에 설치. 불꽃이나 섬광같은 밝은 불빛도 감지하기에 밝은 플래시 불빛으로 테스트
   * 불꽃 감지 센서가 플래시 불빛을 감지하면: 붉은색 LED가 깜빡거리고 핸드폰에 불꽃 감지 알람 메시지가 울린다.
   * 불꽃 감지 알람 메시지는 Android Immortal Service(안드로이드 죽지않는 서비스)를 적용하여 앱이 닫혀도 백그라운드에서 작동이 된다.

6. 집안 감시용 CCTV
   * 라즈베리파이 보드를 이용해 CCTV 카메라 동작시키고 CCTV가 동작되고 있다는 알림 메시지 핸드폰에 전송
   * Node.js 실시간 스트리밍 서버를 통해 안드로이드와 웹 사이트로 전송해 실시간 모니터링
   * 집안 전체를 감시하기 위해 출입문과 대각선에 있는 천장 구석 높은곳에 설치
   
   * CCTV 동작 알림 메시지는 Android Immortal Service(안드로이드 죽지않는 서비스)를 적용하여 앱이 닫혀도 백그라운드에서 작동이 된다. 