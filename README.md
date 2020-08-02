## :two_men_holding_hands: ​부캠나우(나우누리) (20200731 - v1.0.0)

### :pushpin: 나우누리 소개

- 나우누리는 1994년 서비스를 개시했으며 **2013년 1월 31일 서비스**가 종료되었다. 천리안과 하이텔에 이은 대형 BBS로 인터넷이 지금과 같이 발전하지 못했던 시절, 몇 안되는 정보 **교류의 장** 역할을 수행함으로써 한 때 수백만에 이르는 많은 회원을 거느렸으며 **다양한 게시판 및 동호회가 운영**되었다.

  ![나우누리2](https://user-images.githubusercontent.com/33643752/89039259-b1c36700-d37c-11ea-927e-0b650ebf6969.gif)

- 당시는 예절이 지켜지는 아름다운 시절로 요즘처럼 초딩들이 날뛰는 모습은 볼 수 없었다. **나우지기**들이 열심히 모니터링을 하였기 때문이다. 또한 여러 대학들과 제휴하여 <u>사이버캠퍼스</u>를 운영하여서 **대학생**들도 많이 이용하였다.

- 웹으로 넘어와서 나우누리의 가장 강력한 세일즈 포인트는 **동호회 자료실**이었다. 당시 나우누리의 자료실 소스는 어느 인터넷 서비스도 쫓아올 수 없는 서비스량을 자랑하고 있었고, 내심 유료 서비스로도 사용자들의 충성도를 유지할 수 있으리라 생각했나 보지만 결과는 시궁창이었다.

  

  ![나우누리](https://user-images.githubusercontent.com/33643752/89039227-a40de180-d37c-11ea-889d-6ab1dab66a1b.jpg)

  
<br/>

### :closed_book: 만들 서비스 소개

- 기존의 클린 했던 나우누리의 상황을 재현 하기 위한 **A: 욕설 필터링 기능**과 현재 존재하는 다른 커뮤니티와의 차이를 만들기 위해서 **B: 둘 중 하나, C: 유저 추천** 기능을 추가하였다.

- 여기서 **둘 중 하나** 기능은 유저의 유치를 위한 재미 요소로 추가하였다.

<br/>

### :man: 서비스 대상

- 부스트 캠퍼와 스태프, 마스터님

<br/>

### :book: 일반 서비스 제공 요구사항 명세

| 구분  | 요구사항                                                     | 산출물                                                     |
| ----- | ------------------------------------------------------------ | ---------------------------------------------------------- |
| 2주차 | 댓글 기능이 구현된 게시판(코딩, 아재개그, 운동, 음악, 역사, 맛집, 음주 등)<br />관심사(코딩, 운동, 음악, 역사, 맛집탐방, 음주 등) | 게시판 페이지                                              |
| 3주차 | 회원가입 - 받을 데이터(아이디, 패스워드, 닉네임, 관심사)<br />로그인 - 예시) Session, Cookie<br />프로필수정 | 회원가입 페이지<br />로그인 페이지<br />프로필 수정 페이지 |
| 4주차 | 메인화면 구현(전체적인 디자인 수정), 게시글의 좋아요(하트) 기능 | 메인화면 페이지                                            |

<br/>

### :book: 인공지능 서비스 제공 기능 명세

| 구분   | 기능명      | 설명                                                         |
| :------: | :-----------: | ------------------------------------------------------------ |
| 기능 A<br/>(주) | 욕설 필터링 | **욕설, 비방을 걸러주는 기능** [[참조](https://github.com/hjh010501/appropriate-filetering)]<br />게시판과 댓글에 올라오는 스팸이나 욕설/비방을 필터링 해주는 것입니다.<br />욕설에 해당하는 문자는 *로 표기합니다. |
| 기능 A<br/>(서브) | 읽음이      | **CSS 서비스를 통해 글 읽어주는 서비스** [[참조](https://www.ncloud.com/product/aiService/css)]<br />다중 작업을 하는 동안 글을 귀로 들을 수 있다. |
| 기능 B<br/>(주) | 둘 중 하나  | **teachable machine을 통한 1:1 비교** [[참조](https://teachablemachine.withgoogle.com/train)]<br />자신의 이미지나 웹캠을 통한 얼굴을 업로드하고 그에 대한 결과값을 출력해주는 <br /> 것입니다. teachable machine을 통해 여러 장의 이미지를 학습합니다.<br />예제) 사자와 토끼를 학습시키고 사용자가 얼굴을 등록하면 웹 페이지에 <br /> "당신은 사자와 더 닮았습니다(73%)" 이런식으로 출력해줍니다. <br/>(사자, 토끼), (아이유, 아이린) 등 누구와 내가 더 닮았는지 다양한 <br/> 경우를 제공합니다. |
| 기능 B<br/>(서브) | 감정 이모지 | **얼굴인식을 통한 이모지 만들기** [[참조](https://www.ncloud.com/product/aiService/cfr)]<br />셀카를 올리면 얼굴을 가려지기 원하는 사람은 얼굴이 이모지로 대체가 된다.<br />쉽게 프로필 사진이라고 생각하면 됩니다.<br />제공해드린 링크를 보시면 표정에 대한 결과값이 제공되고 그에 맞는 <br /> 이모지를 프로필로설정해주시면 됩니다. |
| 기능 C<br/>(주) | 유저 추천   | **활동이나 관심사기반으로 그룹이나 유저를 추천해주는 기능**<br />Recommendation 기본 알고리즘에 대해서 검색<br />유저를 추천해주는 것에서 친구 추가나 쪽지에 대해서는 고려하지 않는다. <br/> 어려울 수도 있는 주제인 만큼 데이터셋과 방법에 대해서 [공유](https://github.com/boostcamp-2020/relay_03#bell-%EC%B6%94%EA%B0%80-%EC%84%A4%EB%AA%85)하려고 합니다. <br/>  |
| 기능 C<br/>(서브) | 게시글 추천 | **예상 조회수나 추천수를 예측하는 기능**<br />게시글의 길이, 첨부된 이미지 개수 등의 메타데이터들을 활용해 <br/> 게시글이 받게 될 조회수와 추천수를 예측한다. <br/>
실제 커뮤니티 웹사이트의 자료를 크롤링하여 training set의 <br/> 자료로 활용한다. |

:star: **각 주차별 팀은 주 기능이 힘들 시 서브 기능을 구현할 수 있다.**

<br/>

### :hammer: UI 설계
- [UI 설계도](https://docs.google.com/presentation/d/10_LDhi5gE6HRMyb9G11cD4XZKgyufq62Za5Njs0RkBU/edit#slide=id.g86ac92521f_0_10)

<br/>

### :bell: 추가 설명
- 코사인 유사도 [[참조](https://euriion.com/?p=548)]
  - 선택한 카테고리에 따라서 친구 추천을 해주는 알고리즘은 <u>데이터의 유사도</u>를 측정하면 구현 할 수 있을거 같네요. 추천 시스템은 이미 쌓아놓은 데이터가 필요하기에 선택한 카테고리를 테이블 데이터로 만들고 ([1,1,0,0],[1,0,1,0]) 유사도를 측정하면 쉽게 얼마나 가까운지 알 수 있어요. 유사도를 측정하는 이론에서 **코사인 유사도**가 가장 여기에 활용하기 쉬워보이네요. **다차원 벡터의 유사도를 계산**하는 이론이에요.
- BIG 5 성격 캐글 데이터셋 [[참조](https://www.kaggle.com/tunguz/big-five-personality-test/kernels)]
  - Big5 성격 특성이 심리학적으로 지지를 받고 문항수도 많은만큼 <u>나와 더 비슷한 사람을 추천</u>해줄 수 있을 것 같아요. 임의의 데이터가 아니라 **1,015,342**개의 실제 데이터도 있으니 더욱 좋네요. 다만 신규 가입자에게 추천을 위해 **100문항**을 물어봐야한다는 점이 서비스면에서 조금 걱정이 될 것같아요! 회원가입할 때 말고 <u>사용자가 원할때</u> 마이페이지에서 응답을 할 수 있도록 하면 어떨까요? 응답 결과가 없으면 추천 기능을 사용할 수 없는 것으로 하는거죠. 사용자가 마이페이지에서 원할때 재검사를 할 수 있도록 해도 좋을 거 같아요.
- 16 Personalities 무료 성격유형검사 [[참조](https://www.16personalities.com/ko/%EB%AC%B4%EB%A3%8C-%EC%84%B1%EA%B2%A9-%EC%9C%A0%ED%98%95-%EA%B2%80%EC%82%AC)]
  - MBTI는 학계에서 유행이 지났을뿐 학술적으로 타당하게 연구한 내용이며 대중들한테는 여전히 가장 큰 인기가 있습니다. 코사인 유사도와 함께 벡터를 만들어 유사도를 측정한다면 MBTI의 네 요소들을 벡터화해서 (외향적/내향적, 이상적/현실적, 이성적/감성적, 결과중시/과정중시) 처럼 나눈 뒤 5점척도(혹은 3점척도)등으로 각 유저의 벡터를 완성시켜 활용할 수 있을 것 같습니다. 참조된 사이트를 보시면 10~20개의 응답을 받는 기능을 구현하여 받은 응답을 유형별로 점수화하여 유사도를 구하는 공식에 적용하는 방법을 쓰는 것도 좋을 것 같습니다. 예를들어, 외향성이 양수고 내향성이 음수라 가정할 때, 맨 오른쪽 답은 +3점을 맨 왼쪽 답은 -3점을 부여하는 거죠. 사이트의 질문 set을 발췌하여 분류한 뒤 사용하는 것도 좋을 것 같습니다.

<br/>

### :triangular_flag_on_post: 프로젝트 참여자
- 1주차
  | [**J025 김대선**](https://github.com/kimdaeseon) | [**J026 김덕현**](https://github.com/Kim-deokhyeon)  |   [**J027 김도균**](https://github.com/kdogyun)   | [**J028 김도균**](https://github.com/thesulks) |
  | :----------------------------------------------: | :--------------------------------------------------: | :-----------------------------------------------: | :--------------------------------------------: |
  | [**J029 김도연**](https://github.com/do02reen24) |     [**J030 김도호**](https://github.com/Do-ho)      | [**J031 김동인**](https://github.com/dannydongin) | [**J032 김동현**](https://github.com/dooking)  |
  |  [**J034 김민섭**](https://github.com/msmk530)   | [**J035 김민성**](https://github.com/Front-line-dev) |   [**J036 김민식**](https://github.com/zmrdltl)   |                                                |

