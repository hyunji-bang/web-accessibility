# form
### 개념
- `<form>`태그는 사용자 입력을 위한 다양한 형식의 control(입력필드, 버튼 등 폼을 구성하는 입력 요소들)로 구성되는 영역
- `<fieldset>`은 form양식에서 연관된 것을 묶어줌
- `<legend>`는 fieldset 요소에 관한 제목
---

> 아래 부분도 하나의 fieldset이 될 수 있다.
```javascript
<label for="join">옥션 약관과 개인정보 수집 및 이용을 확인하였으며 이에 동의하십니까?</label>

<input id="join" type="submit" value="동의하고 회원가입" />
<input id="join_cancel" type="reset" value="취소" />
```


>`select`를 사용할 때에는, 이렇게 `title`을 붙여서 설명해준다.
```javascript
<select name="user_email" id="user_email" title="이메일 서비스 회사를 선택">
    <option value="0">선택</option>
    <option value="hanmail.net">hanmail.net</option>
    <option value="gmail.com">gmail.com</option>
    <option value="naver.com">naver.com</option>
</select>
```

> 휴대폰 입력부분 3개의 영역에선, 각 input에 `title`을 붙여주어 연결시켜주고, `각기 다른 name` 속성을 주어야한다.
```javascript
<select name="user_phone1" id="user_phone">
    <option value="1">휴대폰 번호를 선택하세요.</option>
    <option value="010">010</option>
    <option value="019">019</option>
</select>
<input type="text" name="user_phone2" id="user_phone2" title="휴대폰 가운데 번호 3~4자리 입력" />
<input type="text" name="user_phone3" title="휴대폰 끝 번호 4자리 입력" />
```


> 이렇게 `value`값을, `진짜 값`으로 넣는 방법-> *좋은방법!!*
```javascript
<dl>
    <dt><label for="user_email">이메일 주소를 입력하세요</label></dt>
    <dd>
        <input type="text" title="이메일 입력" />
        @
        <select name="user_email" id="user_email">
            <option value="0">선택</option>
            <option value="hanmail.net">hanmail.net</option>
            <option value="gmail.com">gmail.com</option>
            <option value="naver.com">naver.com</option>
        </select>
    </dd>
</dl>
```
---
### 참고 )

- 한 페이지에 여러개의 `<form>`이 들어갈 수 있다.
- 하나의 `<form>`에 여러 개의 `<fieldset>`이 들어갈 수 있다.
- `submit`과 `reset`은 꼭 `<form>` 안에 들어가있어야 한다.
- `<form>`태그 안에 `heading 태그` 를 쓰면 절대 안된다.
- `heading태그`와 `<legend>`가 중복 될 때는, 둘 중 하나를 날려야 한다.
- `required`와 `placeholder`는 `html5`속성이기 때문에, html4, xhtml에서는 쓸 수 없다.
- `name`값이 모두 달라야 하는것은 `radio button`밖에 없다
- `name`은 *서버측으로 값이 날라갈때* 를 위해서 쓰인다.

