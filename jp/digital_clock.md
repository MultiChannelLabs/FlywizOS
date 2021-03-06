# 디지탈 시계
 디지탈 시계는 시간을 표시하는 전용 컨트롤로, 많은 시나리오에서 사용자는 시간을 표시해야하며 시스템 시간에 따라 자동으로 표시됩니다.
## 사용법
1. 프로젝트 창에서 버튼을 추가하고자 하는 액티비티의 UI 파일을 더블 클릭합니다.

2. 우측의 컨트롤 박스에서 `Digital Clock` 컨트롤을 선택합니다.

3. `Digital Clock`컨트롤을 마우스 왼쪽 클릭 후 드래그하여 버튼을 만들 위치에 놓으면, 자동으로 컨트롤이 만들어집니다.

4. 만들어진 디지털 시계를 마우스 왼쪽 클릭하면 속성 창에서 해당 버튼과 관련된 속성들을 확인하고, 변경할 수 있습니다.

	![](assets/clock/clock1.png)
	
  * Format
	이 속성은 시간을 표시하는 형식을 정한다. 24시간 또는 12시간 시스템, 그리고 초에 대한 표시 유무를 선택할 수 있습니다. 
  * Blinking
	이 속성은 `:`이 항상 표시되는지, 점멸되는지를 설정합니다.
  * Color
	디지털 시계의 글자 색을 설정합니다.
  * Font size
	디지털 시계의 글자 크기를 설정합니다.
  * Picture Character Set  
	숫자나 글자를 지정된 이미지로 표시할 수 있도록 설정합니다. (Text 컨트롤의 [이미지 캐릭터 설정](textview.md) 참고하십시오)
5. 저장, 다운로드 후 효과를 확인합니다.
6. 만약 시간을 수정하기 원한다면 [시스템 시간](system_time.md)을 참고하십시오.


# サンプルコード

![](assets/clock/example.png) 

[Sample code](demo_download.md＃demo_download)のDigitalClockDemoプロジェクト参照してください。