
# Hanwha System/ICT 기술교육 (2019.01.28~2019.02.01)
- 매일 아침 전날 배운 내용 2문제 정도 시험
- 마지막 시험: 객관식 10개 주관식 5개

<a href="#python">01_Python</a><br>
<a href="#numpy">02_Numpy</a><br>
<a href="#pandas">03_Pandas</a><br>

## 환경설정
* jupyter notebook 설정 파일 다운로드: http://tagme.to/moon9342/config/
* 다운로드 받은파일은 사용자폴더로 이동 $home/.jupyter (jupyter notebook 1회 실행 후 폴더 자동 생성)

1. Anaconda3설치
2. python -m pip install --upgrade pip (pip 업데이트)
3. conda create -n tensorflow_env python=3.5 (python 3.5 버전으로 tensorflow 가상환경 설정)
4. activate tensorflow_env (가상환경 실행)
5. conda install nb_conda (nb_conda 다운로드)
6. Working directory 지정 (임의 폴더 생성후 이동)
7. jupyter notebook (jupyter notebook 실행)

## Jupyter Notebook 단축키
- ctrl + enter : 셀 실행
- shift + enter : 아래에 셀 추가
- (셀 선택) dd : 셀 삭제
- (셀 선택) a : 위에 셀 추가

-----------------------------------------------------------------------

## 2019.01.28(월)
### 개발 환경 설정
* Data, Data Analysis, Data Mining
* Big Data(3V)
* Big Data 분석 방법
> 1. EDA (탐색적 데이터 분석)
> 2. Machine Learning
> 3. Deep Learning

### <a id="python">01_Python</a>
- Python Data Type
> 1. 숫자 (정수, 실수, 지수, 복소수)
> 2. 문자열
> 3. Boolean
>	* True
>	* False
>	* False로 간주되는 것
>		* ""(빈문자열)
>		* [](빈 List)
>		* ()(빈 Tuple)
>		* {}(빈 Dict)
>		* 0(숫자 0)
> 4. List, Tuple, Dictionary, Set ...

- 문자열 Indexing
> 1. 변수[n]
> 2. 변수[-n] (뒤에서부터)

- 문자열 Slicing
> 1. 변수[n:n]
> 2. 변수[n:] (끝까지)
> 3. 변수[:n] (처음부터)

- 문자열 Formatting
> 1. %d (정수)
> 2. %s (문자열)
> <br>예시) a = "나는 사과를 %d개 가지고 있어요!" %count
> <br>예시) a = "사과를 {0}개, 바나나를 {1}개".format(3, 4)

- 문자열 함수
> 1. len(String)
> 2. String.count(String2) : 문자열 변수 내에서 문자열2의 개수
> 3. String.find(String2) : 문자열2가 처음 나온 위치, 없으면 -1
> 4. String.index(String2) : 문자열2가 처음 나온 위치, 없으면 Error
> 5. String.upper()
> 6. String.lower()
> 7. String.strip() : 양옆 공백 제거
> 8. String.replace(원본문자열, 바꿀문자열)
> 9. String.split(구분자)

- Python의 List
> 1. list()
> 2. [    ]
> <br>Tip! 데이터 타입 확인시 type(변수)
> <br>Tip! 데이터 타입에 관계없이 하나의 리스트에 삽입 가능 (리스트 안의 리스트도 OK)

- List의 연산
> 1. Indexing
> 2. Slicing
> 3. ＋ (덧셈) 
> 4. ＊ (곱셈)
> 5. 부분리스트의 대체, 삭제 연산 : Slicing 개념 이용
> 6. del 리스트[n] : n번째 요소 삭제
> 7. "".join(List) : 리스트의 항목들을 병합
> <br>Tip! Python에서는 숫자 + 문자열 연산 불가능, 그러므로 숫자를 문자열로 변경 후 처리 => str() 함수 사용

- List의 함수
> 1. List.append(요소) : 마지막에 요소 추가
> 2. List.sort() : return 값 없음 (리스트 자체를 변경시킴)
> 3. List.reverse() : 리스트 요소 순서 뒤집기
> 4. List.insert(n, m) : n번째 앞에 m 추가
> 5. List.remove(m), 처음 발견한 m 삭제
> 6. List.pop()
> 7. List.extend(부분리스트)
> <br>Tip! List.sort().reverse() 불가능, 왜냐하면 sort()함수의 return이 none이기 때문!

- List의 복사
> 1. 복사할 때는 copy 모듈 사용 (import copy from copy as cp)
> <br>Tip! 객체의 비교시 "a is b" 형태로 사용 가능, ( == 은 내용을 비교, is는 참조 객체를 비교)
> <br>Tip! 리스트를 Slicing해서 다른 변수에 대입하는 경우 다른 리스트로 인식!

- Python의 Tuple
> 1. tuple()
> 2. (      ) : 소괄호 생략 가능
> <br>Tip! List와의 차이점: 튜플은 수정이 불가능함! (삭제, 변경, 추가 불가능)
> <br>Tip! Indexing, Slicing,   +   (덧셈) ,   *   (곱셈)은  List와 똑같이 가능함!
> <br>Tip! 요소가 하나인 튜플을 선언할 때는 (요소값,) 처럼 뒤에 , 붙이기!
> <br>Tip! 튜플 안에 리스트가 있는 경우 리스트 변경 가능

- Python의 Dictionary (연관 배열로 구성 일반적으로 Hash, Map라고도 함)
> 1. {    }
> 2. Json 방식으로 데이터 표현 (순서 관계 X) : Dict = {"key1" : "value1", "key2" : "value2", ...}
> 3. Dict["key"]
> 4. 값의 삽입, 변경 가능
> 5. del Dict["key"] : 키값으로 데이터 삭제
> <br>Tip! key 값은 primary 하다. 

- Dictionary의 함수
> 1. Dict.keys() : 키만 추출 (그러나 List는 아님)
> 2. Dict.values()
> 3. Dict.items() : 각 항목의 키와 값을 튜플로 보여줌
> 4. 반복문 사용 가능 : for key in Dict.keys() : print (Dict[key])
> 5. Dict[key] : 방법 1
> 6. Dict.get(key, default) : 방법 2 - 키값이 없으면 default 값 사용 가능 
> 7. key in Dict : Dict 안에 key가 있는지 확인
> 8. Dict.clear() : 모든 내용 삭제

- Python의 집합(Set) - 순서가 없고 중복이 없는 자료구조
> 1. {      }
> 2. set([n, m, l ...]) : 일반적인 set의 생성법
> 3. Set1 & Set2 : Set1과 Set2의 교집합
> 4. Set1 | Set2 : Set1과 Set2의 합집합
> 5. Set1 - Set2 : Set과 Set2의 차집합
> 6. Set1 ^ Set2 : 합집합에서 교집합을 뺀 결과
> 7. Set.add(n)
> 8. Set.update([n, m, l ...]) : 리스트 항목들을 Set에 추가
> 9. Set.remove(n) : Set에서 삭제

- if문 구조
> if 조건문:
> <br>elif 조건문2:
> <br>else:
> <br>&nbsp;&nbsp;&nbsp;&nbsp;pass(생략)

- for문 구조
> for n in range:
> <br>&nbsp;&nbsp;&nbsp;&nbsp;반복할 문장
> <br>[for문과 List의 응용]
> <br>score1 = [tmp * 2 for tmp in list]
> <br>score2 = [tmp * 2 for tmp in list if tmp > 5]

- 함수의 선언
> def 함수이름(인자, 인자2):
> <br>elif 조건문2:
> <br>&nbsp;&nbsp;&nbsp;&nbsp;실행 문장
> <br>&nbsp;&nbsp;&nbsp;&nbsp;return 결과

- Exercise01. 두 수의 합과 차

- Module이란?
> 함수, 변수, class들을 모아놓은 파일
> <br>모듈 생성 : module1.py
> <br>모듈 호출 : import module1
> <br>from 모듈 import 함수 as 가져올 이름 (from과 as는 생략 가능)
> <br>다른 폴더의 모듈을 불러 올 때는 import sys , sys.path.append("절대경로")
> <br>환경변수 PYTHONPATH를 생성한 후 모듈을 저장한 폴더를 설정하는 것도 가능
> <br>모듈은 폴더형태로 계층구조로 관리하는 것이 좋다!

-----------------------------------------------------------------------

## 2019.01.29(화)
### 절차지향과 객체지향
* 절차적 언어
- 대표적 언어 C
- 절차적 언어의 특징
> 은행업무
> * 외환 업무
> * 예금 업무
> 	* 입금업무
>	* 출금업무
>	* 마이너스 통장개설
> * 대출업무
> * 보험업무
><br>장점: 문제를 분석하기 쉽고, 구현이 용이
><br>단점: 유지보수가 어려움 - 코드 관리가 힘듦
><br>1990년대 인터넷의 보급으로 정보량이 증가 -> 프로그램에 대한 유지보수 요구사항 증가

* 객체지향 언어
- 문제를 구성하는 요소들을 파악
- 요소들 간의 데이터 흐름을 프로그램적으로 표현 (객체 모델링)
> * 은행: 고객, 계좌, 지점, ...
> * 계좌: 상태(계좌주 이름, 현재 잔액) , 행동 (입금, 출금, ...)
> * 객체 모델링: 추상화(Abstraction)과정을 통해서 프로그램적으로 표현
> * Class: 객체모델링을하는 수단

### 01_Python
- Class
> 1. class 클래스명:
> * 내부에 속성, 생성자, 메소드 생성 가능

### <a id="numpy">02_Numpy</a>
- numpy
> * ndarray: n-dimension array
> * Python의 List와 대동소이, 대신 ndarray는 같은 데이터 타입만 사용 가능
> * List보다 메모리도 적게 사용하며 속도도 빠름
> 1. Arr = np.array(List) : 파이썬 리스트로 넘파이 배열 생성
> 2. Arr.ndim : 몇 차원의 배열인지 확인 가능
> 3. Arr.shape : 차원의 개수와 원소의 개수
> 4. Arr.shape = n, m : n행 m열로 배열 형태 변환
> 5. Arr.dtype = Datatype : 명시적 자료형 선언 - arr = np.array([1, 2, 3, 4, 5], dtype=np.float64)
> 6. Arr = Arr.astype(np.datatype) : 자료형 변경 가능 (실수 -> 정수 변환시 소수점 이하 버림)
> 7. Arr = np.zeros((n, m)) : 0으로 채워진 n행 m열 매트릭스 생성
> 8. Arr = np.arange(n, m, l) : 생성함수 시작, 끝, 간격
> 9. Arr = np.linspace(n, m, l) : 주어진 범위를 지정한 샘플의 개수로 나누어 정해지는 간격으로 연속적인 배열 생성
> 10. Arr2 = Arr1.reshape(n, m) : Arr1을 n행 m열로 변환하여 Arr2에 저장 (원본 보존 View의 개념)
> 11. Arr1.base is Arr2 : 두 배열의 원본이 같은지 확인 가능
> 12. Arr2 = Arr1.resahpe(n, m).copy() : 복사하기
> 13. Arr.ravel() : 모든 내용을 1차원 배열로 만듦
> 14. Arr1 = np.vstack((Arr2, Arr3)) : 열 붙이기
> 15. Arr1 = np.hstack((Arr2, Arr3)) : 행 붙이기
> 16. for idx, date in enumerate(Arr) : 인덱스와 데이터 반복해서 가져오기
> <br> Tip! 가상환경에 numpy 라이브러리 설치하기 - (tensorflow_env) pip install numpy
> <br> Tip! reshape() 함수 안에 -1을 넣으면 자동 설정 (ex> -1, 2인 경우 열은 2로 고정, 행은 나머지 자동)
> <br> Tip! Numpy의 Slicing은 View이다! (원본 변경시 함께 변경됨)

- numpy  배열의 연산
> 1. ＋ : 두 매트릭스의 같은 위치 요소들을 합침
> 2. ＊ : 각 요소에 숫자를 곱함

- Movie Rating 분석 실습
> 1. csv 파일의 맨 윗줄은 # 주석처리
> 2. 파일 오픈 : data = np.loadtxt("data/movie/ratings.csv", delimiter=",", dtype=np.float64)
> 3. 평균 구하기 : data[:, 2].mean()
> 4. 회원 수 구하기: np.unique(data[:, 0]

### <a id="pandas">03_Pandasy</a>
> * Python data 분석의 핵심 Library
- Series
> 1. pd.Series(List or Dictionary ..) : 시리즈 생성
> 2. Series.name = 문자열 : 시리즈에 이름 부여
> 3. Series.index.name = 문자열 : 시리즈의 인덱스에 이름 부여
> <br> Pandas에서 정의한 고유의 자료구조: Series(1차원 nparray), DataFrame(2차원 nparray)
> <br> Tip! 가상환경에 pandas 라이브러리 설치하기 - (tensorflow_env) pip install pandas
> <br> Tip! 생성시 바로 인덱스 부여 : pd.Series([-1, 3, 6, 8, 9], index=["a", "b", "c", "d", "e"])

- DataFrame
> 1. List와 Dictionary를 사용한 생성 가능

-----------------------------------------------------------------------

### 강사님 연락처 & 블로그
* moon9342@gmail.com
* http://moon9342.github.io
* 파일공유 링크: http://192.168.0.109/