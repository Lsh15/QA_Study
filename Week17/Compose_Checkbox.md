# Checkbox
## Checkbox의 구성요소
Compose Checkbox의 구성요소는 6가지가 있다.
``` kotlin 
@Composable
fun Checkbox(
    checked: Boolean,
    onCheckedChange: ((Boolean) -> Unit)?,
    modifier: Modifier = Modifier,
    enabled: Boolean = true,
    interactionSource: MutableInteractionSource = remember { MutableInteractionSource() },
    colors: CheckboxColors = CheckboxDefaults.colors()
)
```
* checked - Checkbox를 선택하거나 선택하지 않도록하는 정의
* onCheckedChange - Checkbox의 상태가 변경되었을때의 정의
* modifier - Checkbox의 Modifier 정의
* enabled - Checkbox 버튼이 눌릴 수 있는지 정의
* interactionSource - 컴포넌트가 눌렸거나 드래그 됬을 때 필요한 정의
* colors - Checkbox의 색깔 정의

### 참고
https://developer.android.com/jetpack/compose/accessibility?hl=ko    
https://medium.com/nerd-for-tech/jetpack-compose-ep-10-checkbox-c79142e87268       
https://www.youtube.com/watch?v=EgPkv_Jb7G4&list=PLgOlaPUIbynpFHXeEORmvIOoiNVgSsWeq&index=10


