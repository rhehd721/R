# R

## 변수의 선언
```R
a = 3
a <- 3
```

## 벡터 (선언시 문자와 숫자를 섞어 사용하면 모두 문자로 취급 및 생성)
```R
v <- c(1, 2, 3)
w <- c(TRUE, FALSE, FALSE)
```

## 객체확인
- ls()
- objects()


## 연산기호
- / == % (C Lan)
- %% == / (C Lan)
- ^ : 제곱
- log() : 로그함수
- sqrt() : 제곱근
- max(), min() : 최대, 최소
- abs() : 절대값
- factorial() : 펙토리얼 
- sin(), cos(), tan() : 삼각함수

## 변수
- NA : 결측값
- NaN : 정의가 불가능한 값
- lnf, -lnf : +- 무한대

## x:y
연속된 숫자 x ~ y

## Seq
```R
seq(1, 10, 2) == 1, 3, 5, 7, 9
```

## Rep
rep(n, times = m)
```R
rep(3, times = 5) == (3, 3, 3, 3, ,3)
```

## names()
```R
score <- (1, 2, 3)
print( score ) # (1, 2, 3)
names( score ) # NULL
names( score ) <- ("a", "b", "c")
print( score ) # a 1 , b 2, c 3  < python dic 과 유사 >
```

# 벡터 연산
```R
sum()
length()
mean()
sort(paramiter, decreasing = FALSE, TRUE)
var() # 분산
sd() # 표준편차
```

## List
c() 와 달리 다른 자료형을 가진 데이터들을 보관할 수 있다.
```R
my.info <- list(name = "TOM", age = 60, status = TRUE)
```

## 펙터
문자형 데이터를 저장하는 벡터의 일종
```R
bt.new <- factor(c('A', 'B', 'C'))
```

## matrix (C Lan arr[][]와 비슷)
2차원 테이블 형태의 자료구조 ( 모든 셀에 저장되는 값은 동일한 자료형 이어야 한다)
```R
matrix(1:20, nrow = 4, ncol = 5) # 4(세로) * 5(가로)의 데이터 생성
```

## bind()
여러개의 벡터를 이용해서 매트릭스를 만들 수 있다.
```R
x = 1:4
y = 5:8
m1 = cbind(x, y)  # 열 방향 즉, 세로 방향으로 매트릭스 생성
m2 = rbind(x, y)  # 행 방향 즉, 가로 방향으로 매트릭스 생성
```

## matrix 의 이름 지정
- rownames()
- colnames()

## data.frame()
서로 다른 형태의 데이터를 2차원 데이터 테이블로 생성
```R
city <- c("Seoul", "Tokyo")
rank <- c(1, 2)
city.info <- data.frame(city, rank)
```

## data.frame status
- im() : 행과 열의 갯수 출력
- nrow() : 행의 갯수 출력
- colname() : 열의 이름 출력, names()와 동일한 결과 값
- head() : data set의 앞부분 출력
- tail() : data set의 뒷부분 출력
- str() : data set의 요약정보
- unique() : 중복제거
- colSums(), colMeans(), rowSums(), rowMeans()

## subset(x=diamonds, subset=, select= )
설정하는 조건에 맞는 벡터, 매트릭스 혹은 데이터 프레임을 반환

## class()
data set의 자료구조를 확인
```R
class(a)  # "data.frame"
```

## is.
```R
is.matrix(a) # True, False
is.data.frame(b) # True, False
```

## CSV File Read and Write
```R
setwd("./source")	# Dir 지정
air <- read.csv("airquality.csv", header = T)  # File지정
write.csv(my.irism "my_iris,csv", row.name = F)
```

## 조건문
```R
type <- "A"
if(type == "B"){
	print("B")
}
else{
	print("A")
}
```

## 반복문
```R
for( i in 1:5){
    print(i)
}
```

## apply(data_set, 1(row) or 2(col), 적용함수)
2차원 데이터는 for, while 문보다 apply의 연산속도가 빠르다
```R
apply(iris[,1:4], 1, mean)
```

## function
```R
myfunc <- function(){
	print("Hello World!")
}
myfunc()
```