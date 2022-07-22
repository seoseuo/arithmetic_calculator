# 📱arithmetic_calculator 0.1📱 
<img src="https://img.shields.io/badge/androidstudio-3DDC84?style=flat&logo=androidstudio&logoColor=white"/>
* 안드로이드 스튜디오를 이용한 사칙연산 계산기
* 최초로 안드로이드 스튜디오를 통한 APP 구현.
  
# 
> 두 개의 EditView를 이용하여 두개의 숫자를 사칙연산 하는 계산기를 만들었다. 
> 지금은 기본적으로 두가지 숫자를 이용한 게산만 가능하지만, 중위표현식을 작성하여 연산자 우선순위에 맞게 Data Structure - linked Stack 메소드를 응용하여 더욱 더 복잡한 계산 기능을 구현토록 할 예정이다.  

### ADV 
* PIXEL API 30
  
  
### 구현 사진


<img src="https://user-images.githubusercontent.com/90320005/180497191-17e26722-8ac2-4a31-9f4e-0c13275d7a58.png" width="300" height="550">  <img src="https://user-images.githubusercontent.com/90320005/180497242-c3f7265c-6317-4ddb-97bb-97753326638c.png" width="300" height="550"> 


<img src="https://user-images.githubusercontent.com/90320005/180497283-033a39fd-d988-4a53-a80a-3f863d332b66.png" width="300" height="550">  <img src="https://user-images.githubusercontent.com/90320005/180497311-2cd32283-045f-4719-adee-2bbb8b47b615.png" width="300" height="550">  

---

### 주요 기능

```java

public void Click(View v) // 더하기 메소드
    {   
        import android.view.View;
        import android.widget.EditText;
        import android.widget.TextView;
        
        
        EditText number1 = (EditText)findViewById(R.id.number1);
        EditText number2 = (EditText)findViewById(R.id.number2);
        TextView result = (TextView)findViewById(R.id.result);

        int n1 = Integer.parseInt(number1.getText().toString());
        int n2 = Integer.parseInt(number2.getText().toString());

        result.setText("결과는 "+Integer.toString((n1+n2)));
    }
    
    
    //XML CODE 나눗셈 버튼
    
        <Button
        android:id="@+id/div"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="나누기"
        android:onClick="divClick"/>
```


 


### 개선 방향
* 첫번째 숫자, 두번째 숫자 EditView를 식을 입력하는 형식으로 변경한 뒤, 스택을 이용하여 __' {{( '__ 우선순위를 구분한 뒤 연산을 시행한다.  
  
  

### 어려웠던 점, 깨달은 점 ᕙ(⇀‸↼‵‵)ᕗ
> 처음으로 사용해보는 안드로이드 스튜디오이기 때문에 XML과 LAYOUT 란을 찾지 못하는 것 부터. 기본적인 세팅을 하는데 시간이 많이 걸렸다.
> TextView 와 EditView 를 사용하기 위해선 import를 해야한다는 것. 가장 기본적인 개념을 간과한 상태부터 시작하니 막막하였다. 또한 XML 디자인은 코드를 통해 구현할 수 있고. 굉장히 직관적이었다. 
> 또한 그동안 쓰던 자바툴인 이클립스와는 사용하는 라이브러리와 API가 많이 달라 적응하는데 시간이 많이 걸렸다.
> 그동안 만들어놓은 메소드들을 적용시켜보고싶다.
