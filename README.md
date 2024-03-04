# Unity-Game-BeatStreat
Project


https://github.com/Kjhyun-2/Unity-Game-BeatStreat/assets/65886338/3e811a31-b056-46c7-af68-3fedf51d5925

# 구현한 기능
게임 시작, 연습 모드, 게임 로고 구현
메인화면 (메뉴)창 구현 
각 단계, 난이도 선택창 구현
단계별 난이도 구현 (플레이어 속도, 장애물 개수, 장애물 에셋 변경)
게임 시작 배경음, 각 난이도 별, 연습모드 배경음 구현
키보드 방향키와 스페이스바를 사용하여 장애물 피하기
플레이어 점프, 슬라이딩, 피격 시 애니메이션 구현
장애물을 피하지 못했을 경우 체력 소비
게임 종료(나가기) 버튼 구현

# 계획 대비 변경사항
일시정지 버튼 -> 뒤로가기 버튼으로 변경
클리어 조건 변경
 -골인지점 도착 -> 3분 동안 장애물 피하면 클리어
재시작 버튼 구현 x -> 플레이어가 죽으면 자동 재시작으로 변경

![image](https://github.com/Kjhyun-2/Unity-Game-BeatStreat/assets/65886338/a8423cca-55ad-49d8-8727-48055451d373)
캐릭터 체력은 5목숨으로 장애물에 맞을 때마다 1목숨씩 차감
지형(다리)에서 떨어지게 되면 바로 사망 처리하여 
게임을 처음부터 다시 플레이하도록 재시작 처리

![image](https://github.com/Kjhyun-2/Unity-Game-BeatStreat/assets/65886338/aecc3754-23ce-49a2-9e64-f65caff50d22)
플레이어가 3D 환경에서 움직일 때 카메라가 일정한 거리를 유지하면서 플레이어를 중심으로 회전하거나, 플레이어가 점프할 때도 일정한 높이를 유지하도록 한다.

![image](https://github.com/Kjhyun-2/Unity-Game-BeatStreat/assets/65886338/ed7ebea0-adc3-42b5-89e2-0a09dc726864)
![image](https://github.com/Kjhyun-2/Unity-Game-BeatStreat/assets/65886338/a75a198a-37f4-4561-a34e-750d42839004)
![image](https://github.com/Kjhyun-2/Unity-Game-BeatStreat/assets/65886338/2f5b527b-2af9-4520-81d5-53cc734ed70a)
캐릭터의 y위치가 0보다 작을 경우,
 x위치가 -24보다 작거나, 30보다 클 경우 즉, 플레이어가 지형에서 벗어나게 되면 Die()메서드를 호출한다.

이와 동시에 캐릭터가 사망하면 장애물에 맞은 횟수를 초기화한다.
![image](https://github.com/Kjhyun-2/Unity-Game-BeatStreat/assets/65886338/38875c20-5db9-444d-a11d-8a5c2d80a538)

게임이 시작되면 화면에 클리어 UI를 비활성화 하고 플레이 시간을 기록한다.
3분이 경과되면 게임은 클리어하게 되고 클리어 UI와 함께 일정 시간이 지난 후 게임을 자동으로 종료시킨다.




