---
title: The build Failed likely due to AndroidX incompatibilities in a plugin

categories: flutter

tags:
 - flutter
 - troubleshooting
---

* 에러
Execution failed for task ':app:packageMarketDebug'. > A failure occurred while executing com.android.build.gradle.internal.tasks.Workers$ActionFacade > Entry name 'META-INF/android.support.design_material.version' collided

* 발생원인
안드로이드 시스템은 개발 성능을 향상시키기 위해 방대한 캐시를 생성하며 삭제하지 않는다. 이러한 캐쉬가 종종 문제를 일으킨다.

* 해결방법
1. 안드로이드 애뮬레이터 및 안드로이드 스튜디오 및 비쥬얼 스튜디오 코드 완전 종료 (완전 종료를 위해 재부팅도 좋은 방법)
2. Android Stuiod -> File -> Invailate Cashes / Restart


* 에러
The build failed likely due to AndroidX incompatibilities in a plugin. The tool is about to try using Jetifier to solve the incompatibility. 

* 해결방법
android/gradle.properties에 추가
  android.useAndroidX=true
  android.enableJetifier=true

해결이 안될 경우
특정 라이브러리에서 androidX를 지원하지 않을 수 있으므로 해당 라이브러리의 버전을 업데이트
