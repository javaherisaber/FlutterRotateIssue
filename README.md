# Flutter web issues

A sample project to reproduce following issues (all in iPhone 6 device)

## Wrong canvas height when rotating device

1. Create a new project with Web support
2. `flutter build web --web-renderer canvaskit --release`
3. Deploy on hosting server
4. Open website on iOS safari
5. Tap on Add to Home Screen
6. Open the app from the added shortcut in the home screen
7. At this point canvas height is Okay.
8. Rotate device to landscape and then portrait again
9. canvas height is half the previous size and it never returns to the correct state again, even restarting the app does not change the height.

https://user-images.githubusercontent.com/29440700/148176804-b4f335af-4df7-40dc-abdf-52c13d774365.mp4

## TextField not allowing to tap on other widgets in Safari

1. Create a new project with Web support
2. Add a TextField and a Button to your main screen
3. `flutter build web --web-renderer canvaskit --release`
4. Deploy on hosting server
5. Open website on iOS safari
6. Open TextField to type in and at the same time that focus is on TextField, tap on the other button.
7. Button is not being pressed while the focus is on TextField

https://user-images.githubusercontent.com/29440700/148673490-777d0fb6-e517-4b5b-9fa6-331bbe87f0be.mp4
