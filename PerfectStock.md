# PyCoP PerfectStock Project

[1기 프로젝트 목차]

1.프로젝트 환경설정
1-1 아나콘다 최신설치, Pycharm(또는 익숙한 IDE)설치, Jupyter Notebook 설치
       (책 08항목)
1-2 Github 계정만들기

2. 파이썬과 COM
2-1 COM과 파이썬
2-2 파이썬으로 엑셀다루기 (Pandas 엑셀 읽기쓰기 Code공유 : 정세훈)

3. 키움증권API
3-1 개발환경구축
3-2 PyQT기초
3-3 기초API익히기
3-4 Pandas를 이용한 데이터기초분석
3-5 Pandas, zipline을 이용한 백테스트
3-6 matplotlib를 이용한 데이터 시각화
3-7 PyQt를 이용한 GUI 프로그래밍

4. 실전개발 1일
5. 실전개발 2일
6. 실전개발 3일
7. 실전개발 4일
8. 실전개발 5일



### 파이썬과 COM
COM이란 마이크로소프트에서 개발한 기술로, Component Object Model이라는 용어이다.
여러 컴포넌트 객체를 이용해 프로그램을 개발하는 모델을 의미한다.
COM을 이용하면 C++ 같은 프로그래밍 언어로 개발된 객체도 파이썬에서 사용할 수 있다.


import win32com.client  

explore = win32com.client.Dispatch("InternetExplorer.Application")  
explore.Visible = True  


### Pandas로 엑셀 읽어오기
Pandas는 엑셀읽기, 편하게 할 수있다.
기존에 어려운 모듈들이 많음

읽어오기 모듈
import pandas as pd
import numpy as np

data = pd.read_excel('stat_104102.xls')
data.head(5)

쓰기모듈
data.to_csv('test.csv')  # csv 쓰기

### totoiseGit
1.git for windows를 설치한다
2.totoiseGit을 설치한다
http://kwangho9-develope.blogspot.com/2016/11/git-clienttortoisegit.html

