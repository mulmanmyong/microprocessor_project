# microprocessor_project

S32K144 보드 기반 마이크로프로세서설계실험 텀 프로젝트입니다.

LCD1602A, 4자리 7-segment, keypad, LED, buzzer, motor, ADC, external interrupt를 통합해 4종 미니게임을 실행하는 **Counting Game 콘솔**을 구현했습니다.

## Games

- Memory: 7-segment에 표시된 숫자 순서를 기억해 keypad로 입력
- 9x9: 랜덤 구구단 문제를 풀고 keypad로 정답 입력
- WAM: 랜덤으로 켜진 LED 번호를 맞히는 Whack-a-Mole 게임
- Prime: 표시된 숫자가 소수인지 판별

## Main Hardware Features

- GPIO 기반 LED, buzzer, keypad, 7-segment 제어
- LCD1602A 4-bit 모드 출력
- ADC channel 값을 이용한 게임 선택
- PORTB external interrupt를 이용한 메뉴 이동 및 게임 시작
- FTM PWM을 이용한 motor 제어
- LPIT 기반 delay

## Entry Point

메인 로직은 `final_term_project_team_8.c`에 있으며, 보드 초기화 후 LCD 메뉴를 출력하고 ADC 입력값에 따라 게임을 선택합니다.
