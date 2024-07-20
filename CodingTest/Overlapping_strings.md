<h1>문자열 겹쳐쓰기</h1>

<h2>문제 설명</h2>
문자열 my_string, overwrite_string과 정수 s가 주어집니다. <br>문자열 my_string의 인덱스 s부터 overwrite_string의 길이만큼을 문자열 overwrite_string으로 <br>바꾼 문자열을 return 하는 solution 함수를 작성해 주세요.<br>

<h3>제한사항</h3>
my_string와 overwrite_string은 숫자와 알파벳으로 이루어져 있습니다.<br>
1 ≤ overwrite_string의 길이 ≤ my_string의 길이 ≤ 1,000<br>
0 ≤ s ≤ my_string의 길이 - overwrite_string의 길이<br>
<hr>

<h3>입출력 예</h3>

| my string        | overwrite string | s | result           |
|------------------|------------------|---|------------------|
| "He11oWor1d"     | "lloWorl"        | 2 | "HelloWorld"     |
| "Program29b8UYP" | "merS123"        | 7 | "ProgrammerS123" |

입출력 예 설명

<h4>입출력 예 #1</h4>
예제 1번의 my_string에서 인덱스 2부터 overwrite_string의 길이만큼에 해당하는 부분은 "11oWor1"이고 이를 "lloWorl"로 바꾼 "HelloWorld"를 return 합니다.

<h4>입출력 예 #2</h4>
예제 2번의 my_string에서 인덱스 7부터 overwrite_string의 길이만큼에 해당하는 부분은 "29b8UYP"이고 이를 "merS123"로 바꾼 "ProgrammerS123"를 return 합니다.

<hr>
<h2>코드💻</h2>
<pre><code>
  
``` cpp
#include <stdio.h>
#include <stdbool.h>
#include <stdlib.h>
#include <string.h>

// 파라미터로 주어지는 문자열은 const로 주어집니다. 변경하려면 문자열을 복사해서 사용하세요.
char* solution(const char* my_string, const char* overwrite_string, int s) {
    // return 값은 malloc 등 동적 할당을 사용해주세요. 할당 길이는 상황에 맞게 변경해주세요.
    int my_string_len = strlen(my_string);
    int overwrite_string_len = strlen(overwrite_string);
    int i;

    // my_string의 길이만큼 동적 메모리 할당
    char* answer = (char*)malloc(my_string_len + 1);

    // my_string을 answer에 복사
    strcpy(answer, my_string);

    // overwrite_string을 answer의 s 위치부터 덮어쓰기
    for (i = 0; i < overwrite_string_len; i++) {
        answer[s + i] = overwrite_string[i];
    }

    // 문자열 끝에 NULL 문자 추가
    answer[my_string_len] = '\0';

    return answer;
```    
}
</pre></code>
