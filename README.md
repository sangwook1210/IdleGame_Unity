# IdleGame_Unity

● 게임 스크린샷 / 플레이 영상<br>


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
    - 좌측 상단에 캐릭터가 현재 보유한 골드를 표시
    - 우측 상단에 다음 레벨업 시 증가할 체력과 공격력을 표시
    - 각 캐릭터의 하단에 각 캐릭터의 체력과 공격력을 표시
    - 우측에 체력과 공격력 증가 버튼 배
    - 각 캐릭터가 데미지를 입었을 경우, 각 캐릭터의 상단에 데미지 텍스트가 각 텍스트 풀에 생성됨
    - 캐릭터가 골드를 얻었을 경우, GoldTextPool에서 생성된 텍스트가 얻은 골드를 캐릭터의 좌측 상단에 표시
  - 
- GameOverScene
  - ff
  - Retry 버튼을 누를 경우 StartScene으로 이
