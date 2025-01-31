# tmap_travel_time

Tmap Travel Time for Home Assistant

Home Assistant에서 TMAP API를 이용하여 자동차 운행 기준 도착 예상 시간을 표시하는 센서입니다.

1. TMAP API 사용 준비

TMAP API 사이트에서 회원가입을 진행합니다.

"앱 만들기"를 통해 앱을 생성하고 앱 키(App Key)를 확인합니다. (이후 설정에 필요하므로 메모해 두세요.)

초기 화면에서 교통/위치 -> TMAP API를 클릭합니다.

좌측 메뉴에서 API 사용 요금 -> 무료체험(Free) 사용하기를 신청합니다.

2. Home Assistant에 Tmap Travel Time 설치

HACS 또는 Manual 설치

HACS를 이용하거나 수동으로 Tmap Travel Time을 설치합니다.

설치 후 Home Assistant를 재부팅합니다.

통합 구성 요소 추가

설정 -> 기기 및 서비스 -> 통합구성요소 추가하기에서 Tmap Travel Time을 추가합니다.

설정 항목을 입력합니다.

Sensor Name: 원하는 센서 이름을 입력합니다.

Start Entity ID: 출발 지점의 entity_id를 입력합니다.

End Entity ID: 도착 지점의 entity_id를 입력합니다.

Tmap API Key: 앞서 발급받은 앱 키(App Key)를 입력합니다.

Update Interval: 센서의 업데이트 주기를 설정합니다.

참고: 무료 체험 기준 하루 1,000회 호출이 가능하며, 사용량이 80%를 초과하면 휴대폰으로 알림 문자가 전송됩니다. 여러 개의 센서를 만들 경우 호출 횟수를 고려하여 업데이트 주기를 조정하세요.

3. Start Entity ID와 End Entity ID 설정

zone 또는 device_tracker로 설정 가능합니다. (zone과 device_tracker는 위도 및 경도 속성을 포함해야 합니다.)

Google Maps 컴포넌트와 함께 사용하여 device_tracker로 현재 위치를 설정하고, zone을 집이나 직장으로 등록하면 현 위치에서의 운행 예상 시간을 자동으로 계산할 수 있습니다.
