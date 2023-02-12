# PAPLE-public

2년이 넘는 시간 동안 우리 사회는 코로나19 바이러스로 많은 어려움을 겪었습니다. 그 어려움 중에서 고독과 외로움에 주목하여, 외부 활동을 통해 사람들을 만나지 않고 사회적 활동의 결핍을 해소할 수 있는 방법을 고민했습니다. 그리고 그에 대한 솔루션으로, 종이비행기에 글을 적어서 이웃에게 날려 소통하면 재밌겠다는 생각을 앱으로 구현했습니다. 가까운 유저에게 쪽지를 날리고, 쪽지 교환이 만족스러웠을 때 대화를 시작하는 방식으로 건전한 소통 환경을 목표로 개발했습니다.

## Project Structure

```

📦PAPLE-public  
 ┣ 📂adapter  
 ┃ ┣ 📜ChatLogAdapter.kt  
 ┃ ┣ 📜FirstPaperPlaneAdapter.kt  
 ┃ ┣ 📜LatestMessageAdapter.kt  
 ┃ ┣ 📜MainViewPagerAdapter.kt  
 ┃ ┣ 📜RepliedPaperPlaneAdapter.kt  
 ┃ ┗ 📜SentPaperPlaneAdapter.kt  
 ┣ 📂fragment  
 ┃ ┣ 📜AlertDialogChildFragment.kt  
 ┃ ┣ 📜AlertDialogFragment.kt  
 ┃ ┣ 📜ChatFragment.kt  
 ┃ ┣ 📜FirstDialogFragment.kt  
 ┃ ┣ 📜HomeFragment.kt  
 ┃ ┣ 📜MyPageFragment.kt  
 ┃ ┣ 📜PermissionAlertDialogFragment.kt  
 ┃ ┣ 📜RepliedDialogFragment.kt  
 ┃ ┣ 📜ReportChatDialogFragment.kt  
 ┃ ┣ 📜ReportPlaneDialogFragment.kt  
 ┃ ┣ 📜SentDialogFragment.kt  
 ┃ ┣ 📜SettingAlertDialogFragment.kt  
 ┃ ┗ 📜SuspendAlertDialogFragment.kt  
 ┣ 📂interfaces  
 ┃ ┗ 📜FirstPlaneListener.kt  
 ┣ 📂models  
 ┃ ┣ 📜ChatMessage.kt  
 ┃ ┣ 📜LatestChatMessage.kt  
 ┃ ┣ 📜PaperplaneMessage.kt  
 ┃ ┣ 📜ReportedChat.kt  
 ┃ ┣ 📜ReportMessage.kt  
 ┃ ┣ 📜Users.kt  
 ┃ ┗ 📜VoiceOfUser.kt  
 ┣ 📂room  
 ┃ ┣ 📜PaperPlaneDao.kt  
 ┃ ┣ 📜PaperPlaneDatabase.kt  
 ┃ ┣ 📜PaperPlaneRepository.kt  
 ┃ ┗ 📜PaperPlanes.kt  
 ┣ 📂service  
 ┃ ┗ 📜MyFirebaseMessagingService.kt  
 ┣ 📂ui  
 ┃ ┣ 📜ChatBottomSheet.kt  
 ┃ ┣ 📜ChatLogMultiView.kt  
 ┃ ┣ 📜FragmentChatViewModel.kt  
 ┃ ┣ 📜FragmentChatViewModelFactory.kt  
 ┃ ┣ 📜LoadingDialog.kt  
 ┃ ┣ 📜PlaneBottomSheet.kt  
 ┃ ┣ 📜SendLoadingDialog.kt  
 ┃ ┣ 📜SoftKeyboard.java  
 ┃ ┗ 📜SuccessBottomSheet.kt  
 ┣ 📜App.kt  
 ┣ 📜ChatLogActivity.kt  
 ┣ 📜GuideActivity.kt  
 ┣ 📜InitialSetupActivity.kt  
 ┣ 📜MainActivity.kt  
 ┣ 📜MySharedPreferences.kt  
 ┣ 📜NestedScrollableHost.kt  
 ┣ 📜NetworkConnection.kt  
 ┣ 📜OtpActivity.kt  
 ┣ 📜README.md  
 ┣ 📜SettingActivity.kt  
 ┣ 📜SignInActivity.kt  
 ┣ 📜SignOutActivity.kt  
 ┣ 📜SplashActivity.kt  
 ┗ 📜SplashCongratsActivity.kt

```

```
