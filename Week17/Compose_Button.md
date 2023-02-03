# Compose_Button
## Button의 구성요소
Compose Button 구성요소는 10가지가 있다.
``` kotlin
@Composable
fun Button(
    onClick: () -> Unit,
    modifier: Modifier = Modifier,
    enabled: Boolean = true,
    interactionSource: MutableInteractionSource = remember { MutableInteractionSource() },
    elevation: ButtonElevation? = ButtonDefaults.elevation(),
    shape: Shape = MaterialTheme.shapes.small,
    border: BorderStroke? = null,
    colors: ButtonColors = ButtonDefaults.buttonColors(),
    contentPadding: PaddingValues = ButtonDefaults.ContentPadding,
    content: @Composable RowScope.() -> Unit
) 
```
10가지의 요소는 Surface영역과 Row영역으로 나눌 수 있다.

Surface영역은 버튼의 배결색과 스타일, 유저와의 Interaction(Click 등)을 담당하며, Row영역은 Button 내부에 보여줄 컴포저블(Text 등)에 대한 설정을 담당한다.

## Surface 영역
* onClick - 버튼이 눌렸을때 효과 정의
* modifier - Surface의 Modifier 정의
* enabled - 버튼이 눌릴 수 있는지 정의
* interactionSource - 컴포넌트가 눌렸거나 드래그 됬을 때 필요한 
* elevation - 버튼의 올라온 효과 정의
* shape - 모양 정의 
* border - 테두리 정의
* colors - 버튼의 색깔 정의

## Row영역
* content - 버튼 내부의 Content 정의
* contentPadding - 버튼 내부의 Content의 여유공간 정의

### 참고
https://kotlinworld.com/240     
https://www.jetpackcompose.net/buttons-in-jetpack-compose    
https://www.youtube.com/watch?v=aihuR5zdBUc&list=PLgOlaPUIbynpFHXeEORmvIOoiNVgSsWeq&index=9    
