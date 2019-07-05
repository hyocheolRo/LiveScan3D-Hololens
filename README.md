# LiveScan3D-Hololens
This application allows for streaming point clouds to a HoloLens and rendering them. Together with our other application, LiveScan3D, it can be used for viewing 3D data captured in real time (for example for telepresence) or pre-recorded data.

이 어플리케이션은 홀로렌즈로 포인트 클라우드를 스트리밍하고 랜더링할 수 있게 해줍니다. 우리의 다른 어플리케이션인 LiveScan3D 와 함께 실시간으로 캡처된 3d 데이터를 보거나 미리 기록된 데이터를 볼 수 있습니다.

You will find a short presentation of the application in the video below (click to go to YouTube):
[![YouTube link](http://img.youtube.com/vi/Wc5z9OWFTTU/0.jpg)](http://www.youtube.com/watch?v=Wc5z9OWFTTU)

## How to get it running with LiveScan3D ##
First of all you need to download LiveScan and get that running. Once this is done, open LiveScan, connect a client and open the live view window (it is the contents of that window that are streamed to Hololens). Next start the Unity application on the same machine as the server, if everything is fine it should be working. If it is not working, let me know and I will try to fix it.

우선 LiveScan을 다운받고 running 합니다. 그리고 나서 LiveScan을 열고 clinet 와 연결하여 live view 윈도우를 열어봅니다 (이것이 홀로렌즈로 스트림되는 윈도우의 콘텐츠입니다). 다음으로 같은 장치에서 서버로써 Unity 어플리케이션을 시작합니다, 만약 모든게 잘 되었다면 제대로 동작할 것입니다. 만약에 제대로 동작 안하면 알려주세요 고쳐볼게요.

If you got this far, getting it to work on Hololens should be easy, just make sure you deploy the app using XAML UWP build type instead of D3D (this is required by the touch keyboard). Once you deploy and start the app on Hololens all you need to do is input the IP number of the server and you should see the point cloud. If there are issues try rebuilding NetworkCommunication in the Release mode, the resulting dll files should be automatically copied to /Assets/Plugins/x86/

여기까지 완료되었다면, 홀로렌즈에서 동작하는 것은 쉽습니다. 그냥 D3D 대신에 XAML UWP 빌드 타입을 사용해서 어플리케이션을 deploy 하도록 설정해 놓았는지 확인해봅시다. 그렇게 채택하고 홀로렌즈에서 앱을 실행하면 서버의 IP number를 입력해야 합니다, 그리고 포인트 클라우드를 볼 수 있을겁니다. 만약에 Release 모드에서 NetworkCommunication 리빌딩할때 이슈가 발생하면 최종 dll 파일은 /Assets/Plugins/x86/ 자동으로 복사되어야 합니다.

## How to control the scene ##
The scene can be moved, scaled and rotated around the Y axis, the modes are chosen using the following voice commands:
 * Move - the scene can be moved using the tap and hold gesture.
 * Rotate - the scene can be rotated by using the tap and hold gesture and moving the hand horizontally.
 * Zoom - the scene can be scaled using the tap and hold gesture and moving the hand horizontally.
 * Reset - resets the scene to its original position, rotation and scale.

## Citations ##
If you use this software in your research, then please use the following citation:

Kowalski, M.; Naruniec, J.; Daniluk, M.: "LiveScan3D: A Fast and Inexpensive 3D Data Acquisition System for Multiple Kinect v2 Sensors". in 3D Vision (3DV), 2015 International Conference on, Lyon, France, 2015

## Authors ##
  * Marek Kowalski <m.kowalski@ire.pw.edu.pl>, homepage: http://home.elka.pw.edu.pl/~mkowals6/
  * Jacek Naruniec <j.naruniec@ire.pw.edu.pl>, homepage: http://home.elka.pw.edu.pl/~jnarunie/
