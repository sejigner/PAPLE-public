# PAPLE-public

2년이 넘는 시간 동안 우리 사회는 코로나19 바이러스로 많은 어려움을 겪었습니다. 그 어려움 중에서 고독과 외로움에 주목하여, 외부 활동을 통해 사람들을 만나지 않고 사회적 활동의 결핍을 해소할 수 있는 방법을 고민했습니다. 그리고 그에 대한 솔루션으로, 종이비행기에 글을 적어서 이웃에게 날려 소통하면 재밌겠다는 생각을 앱으로 구현했습니다. 가까운 유저에게 쪽지를 날리고, 쪽지 교환이 만족스러웠을 때 대화를 시작하는 방식으로 건전한 소통 환경을 목표로 개발했습니다.

## Project Structure

```

📦PAPLE-public  
 ┣ 📂adapter  
 ┃ ┣ 📜ChatLogAdapter.kt  # 채팅방 내부 리사이클러뷰 어댑터
 ┃ ┣ 📜FirstPaperPlaneAdapter.kt  # 상대로부터 처음으로 받은 메시지를 담는 리사이클러뷰를 담당하는 어댑터
 ┃ ┣ 📜LatestMessageAdapter.kt  # 채팅방 리스트에 나오는 최신 메시지를 담는 리사이클러뷰를 담당하는 어댑터
 ┃ ┣ 📜MainViewPagerAdapter.kt  # 홈 화면 3 탭 구조를 만드는 뷰페이저2의 어댑터
 ┃ ┣ 📜RepliedPaperPlaneAdapter.kt #  상대가 답장한 메시지를 담는 리사이클러뷰를 담당하는 어댑터
 ┃ ┗ 📜SentPaperPlaneAdapter.kt  # 보낸 메시지를 담는 리사이클러뷰를 담당하는 어댑터
 ┣ 📂fragment  
 ┃ ┣ 📜AlertDialogChildFragment.kt  # 경고 메시지 자식 프래그먼트 (메시지에 대한 응답)
 ┃ ┣ 📜AlertDialogFragment.kt  # 경고 메시지 프래그먼트
 ┃ ┣ 📜ChatFragment.kt  # 채팅 탭 프래그먼트(메시지 및 채팅방 리스트)
 ┃ ┣ 📜FirstDialogFragment.kt  # 최초 메시지의 다이얼로그 프래그먼트
 ┃ ┣ 📜HomeFragment.kt  # 홈 탭 프래그먼트(사용 안내, 쪽지 날리기, 위치 정보 수집)
 ┃ ┣ 📜MyPageFragment.kt  # 마이페이지 탭 프래그먼트
 ┃ ┣ 📜PermissionAlertDialogFragment.kt  # 권한 허용 커스텀 다이얼로그 프래그먼트
 ┃ ┣ 📜RepliedDialogFragment.kt  # 답장 메시지의 다이얼로그 프래그먼트
 ┃ ┣ 📜ReportChatDialogFragment.kt  # 채팅 신고 기능 다이얼로그 프래그먼트
 ┃ ┣ 📜ReportPlaneDialogFragment.kt  # 메시지 신고 기능 다이얼로그 프래그먼트
 ┃ ┣ 📜SentDialogFragment.kt  # 보낸 쪽지 확인 다이얼로그 프래그먼트
 ┃ ┣ 📜SettingAlertDialogFragment.kt  # 설정 확인 창 프래그먼트
 ┃ ┗ 📜SuspendAlertDialogFragment.kt  # 사용 정지 안내 프래그먼트
 ┣ 📂models  데이터 클래스 디렉토리
 ┃ ┣ 📜ChatMessage.kt  # 채팅방 메시지 데이터 클래스
 ┃ ┣ 📜LatestChatMessage.kt  # 채팅방 미리보기용 최신 메시지 데이터 클래스
 ┃ ┣ 📜PaperplaneMessage.kt  # 메시지 데이터 클래스
 ┃ ┣ 📜ReportedChat.kt  # 신고 당한 채팅 데이터 클래스
 ┃ ┣ 📜ReportMessage.kt  # 신고 당한 메시지 데이터 클래스
 ┃ ┣ 📜Users.kt  # 사용자 정보 데이터 클래스
 ┃ ┗ 📜VoiceOfUser.kt  # 사용자 피드백 데이터 클래스
 ┣ 📂room  Room Library를 이용한 로컬 데이터베이스 구축
 ┃ ┣ 📜PaperPlaneDao.kt  # 데이터베이스에 저장된 데이터와 상호작용하는 데이터 액세스 객체 (SQLite 계층 추상화 제공)
 ┃ ┣ 📜PaperPlaneDatabase.kt  # 앱의 데이터와 데이터베이스를 연결하는 기본 액세스 포인트 역할
 ┃ ┣ 📜PaperPlaneRepository.kt # 데이터베이스에 데이터를 요청하고 가져오는 모델 클래스
 ┃ ┗ 📜PaperPlanes.kt  # 데이터베이스 테이블 정의
 ┣ 📂service  
 ┃ ┗ 📜MyFirebaseMessagingService.kt  # Firebase Cloud Functions를 활용한 Push 알림 담당 서비스
 ┣ 📂ui  
 ┃ ┣ 📜ChatBottomSheet.kt  # 채팅방 하단 시트 프래그먼트
 ┃ ┣ 📜ChatLogMultiView.kt  # 채팅 메시지 별 정렬을 정의하는 상수
 ┃ ┣ 📜FragmentChatViewModel.kt  # 채팅 탭의 데이터 바인딩을 담당하는 뷰모델
 ┃ ┣ 📜FragmentChatViewModelFactory.kt  # 뷰모델 팩토리 인터페이스 구현 클래스
 ┃ ┣ 📜LoadingDialog.kt  # 메시지 전송 로딩 다이얼로그 프래그먼트
 ┃ ┣ 📜PlaneBottomSheet.kt  # 메시지 하단 시트 프래그먼트
 ┃ ┣ 📜SoftKeyboard.java  # 메시지 전송시 자동으로 키보드를 내리도록 하는 클래스
 ┃ ┗ 📜SuccessBottomSheet.kt  # 메시지 전송 성공 다이얼로그 프래그먼트
 ┣ 📜App.kt  # 전역 애플리케이션 상태를 정의하는 클래스
 ┣ 📜ChatLogActivity.kt  # 채팅 액티비티
 ┣ 📜GuideActivity.kt  # 사용 안내 액티비티
 ┣ 📜InitialSetupActivity.kt  # 초기 프로필 설정 액티비티
 ┣ 📜MainActivity.kt  # 메인 액티비티(뷰페이저2 프래그먼트 관리)
 ┣ 📜MySharedPreferences.kt  # 환경 설정 값 및 닉네임을 저장하는 SharedPreference
 ┣ 📜NestedScrollableHost.kt  # 중첩 스크롤을 관리하는 클래스
 ┣ 📜NetworkConnection.kt  # 네트워크 연결 상태를 확인하는 클래스
 ┣ 📜OtpActivity.kt  # 로그인 인증 액티비티
 ┣ 📜SettingActivity.kt  # 환경 설정 액티비티
 ┣ 📜SignInActivity.kt  # 로그인 액티비티
 ┣ 📜SignOutActivity.kt  # 로그아웃 액티비티
 ┣ 📜SplashActivity.kt  # 스플래시 화면
 ┗ 📜SplashCongratsActivity.kt # 가입 환영 스플래시 

```

