# snackbar_nobuilder
플러터 Builder 위젯 없이 Snack bar 만들기

## 실행 화면
![image](https://user-images.githubusercontent.com/77111523/147486706-ef753396-804d-4b07-b930-dbbc22ff504f.png)

## 설명
Builder 위젯이 필요했던 이유
- body에서 Builder 위젯을 불러와서 새로운 context를 할당하는 방법으로 SnackBar를 구현하기 위해서 였음.

Builder 위젯 없이 Snack Bar 만드는 방법 Idea
- 핵심적인 문제는 잘못된 context로 인해서 `Scaffold.of()`함수가 위젯 트리에서 Scaffold의 위치를 찾을 수 없는 것임.
- 따라서, 아예 MySnackBar라는 커스텀 위젯을 Scaffold 밑에 새롭게 생성해서 `Scaffold.of()`함수가 MySnackBar의 context를 가지고 위젯 트리 상에서 그럼처럼 Scaffold를 찾아서 올라오게 하면 됨!
- MySnackBar라는 새로운 커스텀 위젯을 만들어서 그 안에서 Snack Bar를 구현해줌.
- Snack Bar도 색상, 글씨 색, 메세지 전달 시간 등을 커스텀할 수 있음.
