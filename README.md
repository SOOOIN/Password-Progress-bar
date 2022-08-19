
## Password Progress bar

![화면-기록-2022-08-19-오후-10 52 27](https://user-images.githubusercontent.com/56300369/185635018-e8c64bbb-b208-4cf9-ba12-ff1f5a36e926.gif)


### `라이브러리`

[zxcvbn 라이브러리](https://www.npmjs.com/package/zxcvbn)

<콘솔창에서 확인 할 부분>
result.score
  0-4의 정수(강도 막대를 구현하는 데 유용) 
 
  0 #  너무 추측 가능: 위험한 암호.
 
  1 #  매우 추측 가능: 제한된 온라인 공격으로부터 보호.
 
  2 #  다소 추측 가능: 제한되지 않은 온라인 공격으로부터 보호.
 
  3 #  안전하게 추측할 수 없음: 오프라인 슬로우 해시 시나리오로부터 적당한 보호. 
 
  4 #  매우 추측할 수 없음: 오프라인 슬로우 해시 시나리오로부터 강력한 보호.  

---------------------------------------

### `구현 방법`

1. 암호화 라이브러리를 사용하여, 콘솔로 비밀번호 score를 확인.
2. score(0~4) 수를 0~100으로 변환한다.
3. score 점수에 따라, Progress-bar의 길이와 색상이 바뀐다.

---------------------------------------

### `보완할 점`

[] 비밀번호 미입력시, 하단에 아무런 텍스트도 나타나지 않아야함.

   [발생한 문제] input 창이 비어도, default: 값이 나타나지않음.
              case 0 값만 나타남.
    -> case 0:
          return '사용할 수 없습니다.';
       default:
          return'';
.
