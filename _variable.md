###### variable
  
```java
int[] num = new int[length];
List<T> list = new ArrayList<T>();
Map<K,V> map = new Map<K,V>();
```

###### range
| Kind      | Type   | Byte/Bit | Range   |
| :---:     | :---:  | :---:    | :---   |
| `논리형`  | boolean | 1 / 8   | true 또는 false    |
| `문자형`  | char    | 2 / 16  | '\u0000' ~ 'uFFFF' |
| `정수형`  | byte    | 1 / 8   | -128 ~ 127         |
| `정수형`  | short   | 2 / 16  | -32768 ~ 32767     |
| `정수형`  | int     | 4 / 32  | -2147483648 ~ 2147483647 |
| `정수형`  | long    | 8 / 64  | -9223372036854775808 ~ 9223372036854775807 |
| `실수형`  | float   | 4 / 32  | 1.4E-45 ~ 3.4028235E38   |
| `실수형 ` | double  | 8 / 64  | 4.9E-324 ~ 1.7976931348623157E308 |

###### javascript to java string of boolean value
```js
const toggle = "true";
```

```java
Boolean toggle = request.getParameter("toggle");
log.info(toggle);
```
- js 에서 boolean 값을 스트링 타입으로 보내도 "true" or "false"
- java 에서 boolean 타입으 변수에 대입할 경우 java에서는 boolean 타입이 된다
  
###### Integer to int  
```java
Integer sample = null;
sample = 123456789;
int intValue = sample.intValue();
```
  
###### LocalDate / LocalTime / LocalDateTime
```java
LocalDate localDate = null;
LocalTime localTime = null;
LocalDateTime localDateTime = null;
```
  
###### Period / Duration
```java
Period period = null;
Duration duration = null;
```
###### default value
```java
String str; // default value is null
```
