# study_c_language

### C++언어 인접리스트 만드는법
```
#include<iostream>
#include<stdio.h>
#include<vector>
using namespace std;

int main(){
	vector<int> arr[1001];
	
	return 0;
}
```
#### 이러면 "1000개의 공간에 있는리스트 안에 값을 넣을수 있다는 뜻"입니다.

### 배열안을 다 5로채우기
```
#include<iostream>
#include<stdio.h> 
using namespace std;

int main(){
    int arr[5] = {1,2,3,4,5};
    for (int i = 0; i < 5; i++){
    	printf("%d ",arr[i]);
    }
    printf("\n");
    fill(arr,arr+5,5); // 첫번째위치부터 마지막위치까지 5로 채워준다. 
    for (int i = 0; i < 5; i++){
       printf("%d ",arr[i]);
    }
    return 0;
}
```
#### fill(첫위치,마지막위치,채울값);

### c++ 백준 실수하지 말아야 할것.

#### 안좋은예
```

#include<iostream>
#include<stdio.h> 
using namespace std;

int main(){
    bool v[500];
    if (v[0] == false){
        printf("1");
    }else{
        printf("0");
    }
    return 0;
}

```
#### 좋은예
```
#include<iostream>
#include<stdio.h> 
using namespace std;

int main(){
    bool v[500] = {false,};
    if (v[0] == false){
        printf("1");
    }else{
        printf("0");
    }
    return 0;
}
```

### 백준 c++ 유의할점,기억할점.
#### 1.이차원 배열 매개변수 받는법
```
#include<iostream>
#include<stdio.h> 
using namespace std;

int func(int arr[][5]){ // 일차원 배열받는 방식에서 이차원의가로길이를 추가해준다.
    return arr[0][0];
}

int main(){
    int arr[5][5];
    func(arr)
}
```
#### 2. 백준 테스트케이스를 실행시켰는데 답이 음수가 아닌데 음수가나오면 오버플로우다.
#### 3. C++ 배열크기를 나름(?) 넉넉하게 잡아야한다.
