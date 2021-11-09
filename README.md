# gift_macro

글로 설명하면 길어짐. https://youtu.be/bjQaods52NY (단톡방 멤버들의 개인정보 보호를 위해 480p로 화질을 낮춤)

scrcpy가 필요함. https://github.com/Genymobile/scrcpy

메커니즘은 다음과 같음:
1. scrcpy를 통해 폰의 화면을 컴에 미러링하고, 
2. openCV로 컴의 화면 중 일부분을 캡쳐하고, 
3. 그 캡쳐 이미지 중 특정 부분의 픽셀값을 디텍트 해 '선착순'인지 확인하고, 
4. '선착순'일 경우 pyautogui로 클릭하고, 
5. '선착순'을 성공적으로 받았는지 확인한 뒤, 
6. 받았으면 adb를 통해 감사 메세지를 입력하고, 
7. 원래 상태로 복귀하는 

'선착순'이 화면에 나타난 지 400 ms내에 클릭할 수 있음.

특정 픽셀을 디텍트하고 클릭해야 하기 때문에 폰, 모니터, 카톡 UI 등이 달라질 경우 픽셀 위치와 픽셀 디텍팅의 기대값을 수정해야 함.
