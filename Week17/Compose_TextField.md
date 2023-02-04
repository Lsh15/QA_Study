# Compose_TextField
TextField에는 Filled text field 와 Outlined text field 두 종류가 있다.
동일한 구성요소, 기능을 제공하므로 선호하는 스타일에 맞춰 선택하면된다.
 
## TextField 구성요소
Compose TextField의 구성요소는 18가지가 있다.

``` kotlin
@Composable
fun TextField(
    value: TextFieldValue,
    onValueChange: (TextFieldValue) -> Unit,
    modifier: Modifier = Modifier,
    enabled: Boolean = true,
    readOnly: Boolean = false,
    textStyle: TextStyle = LocalTextStyle.current,
    label: @Composable (() -> Unit)? = null,
    placeholder: @Composable (() -> Unit)? = null,
    leadingIcon: @Composable (() -> Unit)? = null,
    trailingIcon: @Composable (() -> Unit)? = null,
    isError: Boolean = false,
    visualTransformation: VisualTransformation = VisualTransformation.None,
    keyboardOptions: KeyboardOptions = KeyboardOptions.Default,
    keyboardActions: KeyboardActions = KeyboardActions(),
    singleLine: Boolean = false,
    maxLines: Int = Int.MAX_VALUE,
    interactionSource: MutableInteractionSource = remember { MutableInteractionSource() },
    shape: Shape =
        MaterialTheme.shapes.small.copy(bottomEnd = ZeroCornerSize, bottomStart = ZeroCornerSize),
    colors: TextFieldColors = TextFieldDefaults.textFieldColors()
) 
```
* value - TextField의 표시되는 Text 내용
* onValueChange - Text가 업데이트할때 트리거되는 콜백
* modifier - TextField의 Modifier 정의
* enabled - TextField의 활성화 여부 
* readOnly - true일시 읽기 전용 모드(수정 불가) 
* textStyle - TextField의 입력 Text의 스타일
* label - 컨테이너 내부 또는 상단에 포커스 상태일때 표시되는 레이블
* placeholder - TextField가 비어있을때 보여지는 Text
* leadingIcon - TextField의 시작부분에 표시되는 아이콘
* trailingIcon - TextField의 끝부분에 표시되는 아이콘
* isError - true일시 label과 TextField색 변경  
* visualTransformation - 입력값의 시각적인 표현을 변경하는 옵션
* keyboardOptions - TextField 입력시 나오는 키보드 옵션
* keyboardActions - TextField 입력시 발생하는 키보드 액션
* singleLine - TextField의 singleLine 여부
* maxLines - TextField의 최대 라인의 수 
* interactionSource - 컴포넌트가 눌렸거나 드래그 됬을 때 필요한 정의
* shape - TextField의 색깔 정의
* colors - TextField의 색깔 정의

### 참고
https://developer.android.com/jetpack/compose/text?hl=ko#enter-modify-text   
https://m3.material.io/components/text-fields/specs    
https://mypark.tistory.com/entry/JETPACK-COMPOSE-OutlinedTextField-FilledTextField%EC%97%90-%EB%8C%80%ED%95%B4-%EC%95%8C%EC%95%84%EB%B3%B4%EC%9E%90        

