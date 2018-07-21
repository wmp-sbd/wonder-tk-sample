# 스크립트 작성 및 삽입 방법
- 결제 완료 페이지의 맨 아래에 아래 스크립트를 넣어주세요.
- WonderTK.checkOut 메소드에서 전달하는 값을 *쇼핑몰에 맞게* 설정해주셔야 합니다
  * ffuid : 쇼핑몰별로 지정된 고유키
  * conversionAmount: 사용자가 결제한 총 금액 

```html
<!-- [시작] 원더쇼핑 CPC 전환 기록 스크립트 -->
<script>  
  window.__wonderTKAsyncTasks = function() {
    WonderTK.checkOut({
      ffuid: '이곳에 FFUID를 넣어주세요.', 
      conversionAmount:'이곳에 고객이 결제한 금액 총액을 입력해주세요.'
    });
  };

  (function(d, s, id){
    var js, wjs = d.getElementsByTagName(s)[0];
    if (d.getElementById(id)) {return;}
    js = d.createElement(s); js.id = id;
    js.src = "https://tk.wonder-shopping.com/sdk/base.js";
    wjs.parentNode.insertBefore(js, wjs);
  }(document, 'script', 'wonder-tk-js'));
  <!-- [끝] 원더쇼핑 CPC 전환 기록 스크립트 -->
</script>
```

# 샘플
- 결제 총 금액은 쇼핑몰 솔루션 별로 제공되는 템플릿 코드를 사용하시면 편하게 입력하실 수 있습니다
- 각 쇼핑몰 솔루션별 샘플 파일을 참고해주세요
  - gabia_firstmall.html : 가비아 퍼스트몰
  - makeshop.html : 메이크샵


# 문의처
- 스크립트 삽입에 어려움이 있을 경우 아래 연락처로 연락 부탁드립니다
  - 기술문의 : dsadsa@wemakeprice.com
  - ffuid 발급 문의 : dsadsadsa@wemakeprice.com
