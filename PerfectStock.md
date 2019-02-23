# PyCoP PerfectStock Project


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

