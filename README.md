# IdleGame_Unity

● 게임 스크린샷 / 플레이 영상<br>

<img width="1920" alt="111" src="https://github.com/sangwook1210/IdleGame_Unity/assets/112921582/88c4be44-31f5-402c-955d-aaa37f55d671">

https://youtu.be/Z2fps6O5eLw <br>

● 게임 소개<br>
적을 죽여 돈을 벌고 이를 이용하여 캐릭터를 강화하여 더 강한 적을 죽이는 방치형 게임

● 게임 기획
- StartScene
  - 캐릭터의 Idle Animation을 사용
  - Play 버튼을 누를 시 LoadingScene으로 이동
- LoadingScene
  - UI의 Slider를 사용하여 로딩 바를 연출
  - UI의 Text를 사용하여 현재 로딩 상황을 유저에게 알려줌
  - 코루틴을 사용하여 비동기 로딩을 작업
  - 로딩이 완료될 경우, enter 버튼을 통하여 GameScene으로 이동
- GameScene
  - UI
    - 좌측 상단에 플레이어 캐릭터가 현재 보유한 골드를 표시
    - 우측 상단에 다음 레벨업 시 증가할 체력과 공격력을 표시
    - 각 캐릭터의 하단에 각 캐릭터의 체력과 공격력을 표시
    - 우측에 체력과 공격력 증가 버튼 배치
    - 각 캐릭터가 데미지를 입었을 경우, 각 캐릭터의 상단에 데미지 텍스트가 각 텍스트 풀에 생성됨
    - 플레이어 캐릭터가 골드를 얻었을 경우, GoldTextPool에서 생성된 텍스트가 얻은 골드를 플레이어 캐릭터의 좌측 상단에 표시
    - 잔액이 부족할 경우, NEGTextPool에서 생성된 텍스트가 메시지를 화면의 중앙 하단에 표시
  - Script
    - 플레이어 캐릭터와 적 캐릭터가 생성됨
    - 플레이어 캐릭터는 200의 체력, 10의 공격력, 1.0의 공격속도를 가지고 생성됨
    - 적의 체력, 공격력, 공격 속도는 랜덤하게 생성됨
    - 적이 죽으면 죽을수록 강력한 적이 생성되고, 주는 골드량도 늘어남
    - 생성되는 적의 스펙은 적의 체력이 100, 3000, 10000을 넘어가는 것을 기점으로 점점 증가폭이 커짐
    - 체력 증가 버튼을 눌렀을 경우, 플레이어 캐릭터의 최대 체력이 늘어나고, 현재 체력이 회복됨
    - 공격력 증가 버튼을 눌렀을 경우, 플레이어 캐릭터의 공격력이 늘어남
    - 플레이어 캐릭터는 3가지 공격 애니메이션 중 하나를 랜덤으로 사용하고 플레이어 캐릭터의 공격력이 1000을 넘어갔을 경우, 4번 공격 애니메이션의 확률이 크게 증가
    - 적은 두가지 공격 애니메이션 중 하나를 랜덤으로 사용
- GameOverScene
  - 플레이어 캐릭터가 패배하였기 때문에 플레이어 캐릭터의 패배 애니메이션과 적 캐릭터의 승리 애니메이션을 재생
  - 플레이어 캐릭터를 2초간 확대
  - Retry 버튼을 누를 경우 StartScene으로 이동
