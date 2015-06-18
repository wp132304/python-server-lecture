초보자도 할수있는 서버개발 #2
==================

## JSON
아까 딕셔너리를 배우면서 Key-Value 형식의 데이터를 보았을 것이다.

> "철수의 전화번호" = "010-1234-5678"  
> "준성이의 이름" = "김준성"  
> "준성이의 여자친구" = "영희"

JavaScript에서는 저런 데이터 뿐만이 아니라 모든 객체 (Object)를 위와 같은 Key-Value 형식의 딕셔너리로 표현하는데, 다음과 같은 방식으로 나타낸다.  

```json
{
    "Key1": "Value1",
    "Key2": "Value2"
}
```
나타내는 방식이 파이썬과 비슷하지 않은가? 맞다. JavaScript에서 이렇게 Key-Value Dictionary를 표현하는 것을 **JSON (Javascript Object Notation)**이라고 부르며, 위와 같은 키-밸류 형식의 데이터 교환을 위해 만든 언어이다.

기본적인 문법은 C/C++등 기존 친숙한 언어의 영향을 받았으며, 파이썬 등의 다른 언어들은 JSON의 영향을 받아서 비슷한 표현법을 만든 것이다.

#### 왜 JSON을 쓰는가?
- 매우 간편하다.
- 거의 모든 언어에서 Dictionary(Hash) 타입을 표현할 때 통용되는 문법이다.

#### 왜 서버 만드는데 JSON을 배우나?
JSON은 위의 이유들로 인해서, 상당히 많은 서버들에서 데이터 표현 방법으로 JSON을 사용한다.



#### JSON 문법
JSON에는 `string`, `number`, `array`, `object` 크게 4개의 자료형이 있다.

- `string`: 문자열. 문자 하나도 문자열로 친다. 큰따옴표 ("") 안에 들어간다.
- `number`: 정수형, 실수형을 포함한 모든 숫자.
- `array` : 배열. 대괄호 (`[]`) 안에 자료형 상관없이 값들을 나열한다.
- `object`: 값으로 또다른 JSON 객체를 넣을 수 있다.

Key는 무조건 string이 되어야 하고, 값들에는 위 4가지 자료형이 올 수 있다.

한번 김준성을 JSON으로 표현해보자.

```json
{
    "name": "김준성",
    "age": 18,
    "friends": ["들쥐", "박쥐", "개미", "사마귀"]
}
```

++ 준성이의 친구들을 object를 활용해서 이름뿐만이 아닌 또다른 JSON 객체로 나타내보자!

### Python Dictionary -> JSON

```python
>>> import json
>>> json.dumps(dictionary)
"딕셔너리가 JSON으로 인코딩된 결과 출력됨"
```