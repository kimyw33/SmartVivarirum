# ESP32 LED Test Code Explanation

### 목적
ESP32가 정상적으로 작동하는지 **내장된 LED**를 이용해 테스트합니다. LED가 1초 간격으로 켜지고 꺼지는 과정을 통해 보드가 정상적으로 동작하는지 확인할 수 있습니다.

## 코드

```cpp
#define BUILT_IN_LED 2  // 내장된 LED의 핀 번호를 정의합니다. ESP32의 내장 LED는 2번 핀에 연결되어 있습니다.

void setup() {
  pinMode(BUILT_IN_LED, OUTPUT);  // LED가 출력 장치이므로, 해당 핀을 출력 모드로 설정합니다.
}

void loop() {
  digitalWrite(BUILT_IN_LED, HIGH);  // LED를 켭니다 (전압을 HIGH로 설정).
  delay(1000);  // 1초 동안 대기합니다 (1000밀리초).
  
  digitalWrite(BUILT_IN_LED, LOW);  // LED를 끕니다 (전압을 LOW로 설정).
  delay(1000);  // 다시 1초 동안 대기합니다.
}