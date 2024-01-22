
# 문제
> 팰린드롬

# 코드
```java
import java.util.*;

public class Test {
    public static void main(String[] args) {

        String str = "A Santa at NASA";
        solution(str);
    }

    public static boolean solution(String str) {

        int start = 0;
        int end = str.length() - 1;

        while (start < end) {
            if(!Character.isLetterOrDigit(str.charAt(start))) {
                start++;
            } else if(!Character.isLetterOrDigit(str.charAt(end))) {
                end--;
            } else {
                if(Character.toLowerCase(str.charAt(start)) != Character.toLowerCase(str.charAt(end))) {
                    return false;
                }
            }

            start++;
            end--;
        }
        
        return true;

    }
}

```