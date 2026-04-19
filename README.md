🔐 스마트 디지털 도어락 시스템 (Smart Digital Doorlock System)
한국어 | English

Logisim을 활용하여 설계한 하드웨어 레벨의 디지털 논리 회로 프로젝트입니다. 보안 기능(비밀번호, OTP)뿐만 아니라 화재 감지, 배터리 관리, 택배 도난 감지 등 실생활에 필요한 안전 기능을 통합적으로 구현했습니다.

🛠 기술 스택 (Tech Stack)
Design Tool: Logisim

Logic Components: 3-bit Counters, ROM, 7-Segment Display, DIP Switches, Logic Gates (AND, OR, MUX, Flip-Flops)

✨ 주요 기능 (Key Features)
비밀번호 관리: 비밀번호 설정, 입력 및 일치 여부 확인, 오류 횟수 카운팅.

배터리 관리: 3비트 카운터를 이용한 잔량 표시 및 배터리 교체 알림(부저).

화재 감지 시스템: 실시간 온도 모니터링 및 화재 발생 시 자동 개폐(Fast Escape).

택배 도난 방지: 박스 센서와 타이머를 연동한 실시간 도난 감지 및 경보.

OTP 보안: 가변 시드 기반 일회용 비밀번호 생성 및 검증.

📖 동작 설명 (Operations)
1. 도어락 (Doorlock)
작동: * 버튼으로 활성화 후 비밀번호 입력.

변경: # 버튼을 눌러 변경 모드 진입 → 숫자 버튼(B0~B9) 4자리 입력 → * 버튼으로 저장.

인증: 저장된 비밀번호와 일치하면 문이 열리며, 불일치 시 오류 횟수가 1회 증가합니다.

2. 배터리 (Battery)
초기화: Reset 버튼 클릭 시 배터리 잔량을 7로 설정.

작동: 문이 열릴 때마다 3비트 카운터가 1씩 감소하며 LED Bar에 시각화됩니다.

알림: 배터리가 0이 되면 부저가 울려 교체 시기를 알립니다.

3. 화재 감지 (Fire Detection)
모니터링: Fire 값이 1이 되면 1초마다 온도가 상승하며 LED Bar에 표시됩니다.

자동 개폐: 온도가 4 이상에 도달하면 신속한 탈출을 위해 도어락이 자동으로 열립니다.

4. 택배 도난 감지 (Theft Detection)
감지: 박스 센서가 1에서 0으로 바뀌었음에도 1분 이내에 문이 열리지 않으면 도난 상황으로 간주합니다.

경보: 도난 판단 시 사용자에게 알리는 경고 시스템이 작동합니다.

5. OTP 설정 (OTP System)
생성: DIP 스위치로 시드 설정 → OTP_Mode 진입 → Next_OTP 버튼으로 생성.

사용: 생성된 OTP는 7세그먼트에서 확인 가능하며, 일회용으로만 사용 가능합니다.

A hardware-level digital logic circuit project designed using Logisim. This system integrates not only security features (Password, OTP) but also essential safety functions such as fire detection, battery management, and parcel theft prevention.

📖 Detailed Operations
1. Doorlock Mechanism
Activation: Press * to activate the system for input.

Password Change: Press # to enter setup mode → Input 4 digits (B0-B9) → Press * to save.

Authentication: Door opens upon matching the stored password; otherwise, the error count increments.

2. Battery Management
Initialization: Reset button sets the battery level to 7.

Tracking: A 3-bit counter decreases by 1 each time the door opens, visualized via an LED Bar.

Alert: When the level reaches 0, a buzzer notifies the user to replace the battery.

3. Fire Detection & Emergency Escape
Monitoring: When the Fire input is 1, a counter simulates temperature rise every second, displayed on the LED Bar.

Auto-Open: If the temperature reaches 4 or higher, the door unlocks automatically for a quick exit.

4. Anti-Theft System
Trigger: If the box sensor changes from 1 to 0 but the door remains closed for over 1 minute, it is flagged as theft.

Alarm: A warning signal is triggered to alert the surroundings.

5. OTP (One-Time Password)
Generation: Set initial seed via DIP switches → Enter OTP_Mode → Press Next_OTP to generate.

Security: The generated OTP is displayed on a 7-segment display and becomes invalid once used.
