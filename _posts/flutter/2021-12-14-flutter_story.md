---
title: Flutter 2.8 버전 업데이트
categories: flutter
tags: 
  - flutter
  - programming

date: 2021-12-14
late_modified_at: 2021-12-14
---

Flutter 2.8 버전 업데이트

StartUp  
이번 릴리즈는 시작 대기시간에 대한 개선 사항이 포함되어있다.
구글 페이의 시작 지연 시간이 Android 저가형 기기에서 50%, 고가형 기기에서 10% 개선됨을 확인하였다.
Flutter가 Dart VM의 가비지 수집 정책(GC)에 영향을 미치는 것을 기선하여, 
애플리케이션 시작 시, 부적절한 GC 주기를 방지할 수 있다.
기본 글꼴 관리자의 시작을 지연하여, 병목현상을 제거하여 시작 대기시간이 개선되었다.


Memory  
메모리가 최대 40MB까지 절약 가능하다.


Profiling  
앱시작 시 활성화 하여, Android Systrace Recorder에 추적 이벤트를 전송할 수 있다.
릴리즈 모드로 빌드된 경우에도 전송 가능하다.  
래스터 캐시의 동작에 대한 선능 추적에서 더 많은 정보를 확인 할 수 있다.  
Flutter는 로드시 부하가 많인 걸리는(expansive), 재사용 이미지들을 각 프레임마다 다시 그리는 대신 blit를 허용한다.  
blit의 정의는 "데이터 배열을 비트맵 배열 목적지에 복사하는 것"이다.  
일반적인 데이터 복사보다 더 복잡하지만, 다양한 기능이 사용 가능하다.  




원본 : <https://medium.com/flutter/whats-new-in-flutter-2-8-d085b763d181>