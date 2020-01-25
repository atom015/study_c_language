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
#### 이러면 "1000개의 공간에 있는리스트 안에 값을 넣을수 있다는 뜻"입니다

### 배열안을 다 5로채우기
```
#include <iostream>
#include <algorithm>
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
