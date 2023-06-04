# 함수 리턴의 문제점

### 1. 어떤 부분에 로그를 남기는 것을 깜빡할 수 있습니다.

캡슐화하면서 중요한 인자가 숨겨져버릴 수 있습니다.



그래서 인자 역할을 하는 함수의 명에 의도를 정확하게 담아야함

```javascript
function withLogging(saveUserData(user)) {
    try {
        saveUserData(user);
    } catch (error) {
        logToSnapErrors(error);
    }
}
```

withLogging = > saveUserDataWithLogging

saveUserData(user) => saveUserDataNoLogging(user)



### 2. 모든 코드에 수동으로 withLogging() 함수를 적용해야 합니다.

슈퍼 파워를 자동으로 주면서 자연스럽게 설계로 처리할 수 있습니다.

<figure><img src="../../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>
