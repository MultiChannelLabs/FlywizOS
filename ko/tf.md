# TF card
TF카드를 삽입하면 시스템이 자동으로 `/mnt/extsd`디렉토리로 마운트합니다.

### 파일 경로 
TF카드의 루트 디렉토리에 `test.txt`파일이 있는 경우 보드에서 이 파일의 절대 경로는 `/mnt/extsd/test.txt`입니다.

## TF카드 쓰기에서 주의 사항
TF카드에 파일을 쓰려면 다음 순서를 따르시기 바랍니다. 그렇지 않으면 제대로 쓰여지지 않는 상황이 발생할 수 있습니다.
`카드 삽입`->`전원 켜기`->`파일 열기`->`파일 읽기 및 쓰기`->`fflush()`->`파일 닫기`->`sync()`->`카드 분리`
즉, TF카드를 쓸 필요가 있는 경우 보드를 켜기 전에 TF 카드가 삽입되었는지 확인하십시오.
그리고 파일 쓴 후에는 동기화 문제에 주의하십시오.

## TF카드 장착 여부 확인
```c++
#include "os/MountMonitor.h"
```
```c++
if (MOUNTMONITOR->isMount()) {
  //TF card has been mounted
} else {
  //TF card is not mounted
}
```
> [!Note]
> `/mnt/extsd`디렉토리는 TF카드 삽입 여부에 관계없이 항상 존재합니다.
> TF카드가 삽입되지 않은 경우 해당 디렉토리를 읽고 쓰면 내용이 메모리에 저장되지만 전원이 꺼진 후에는 사라집니다.