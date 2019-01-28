# Hanwha System/ICT 기술교육 (2019.01.28~2019.02.01)
- 매일 아침 전날 배운 내용 2문제 정도 시험
- 마지막 시험: 객관식 10개 주관식 5개

## 환경설정
* jupyter notebook 설정 파일 다운로드: http://tagme.to/moon9342/config/
* 다운로드 받은파일은 사용자폴더로 이동 $home/.jupyter (jupyter notebook 1회 실행 후 폴더 자동 생성)

1. Anaconda3설치
2. python -m pip install --upgrade pip (pip 업데이트)
3. conda create -n tensorflow_env python=3.5 (python 3.5 버전으로 tensorflow 가상환경 설정)
4. activate tensorflow_env (가상환경 실행)
5. conda install nb_conda (nb_conda 다운로드)
6. Work place 지정 (임의 폴더 생성후 이동)
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

### 01_Python
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
-----------------------------------------------------------------------

### 강사님 연락처 & 블로그
* moon9342@gmail.com
* http://moon9342.github.io