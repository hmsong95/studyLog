## 자바 스크립트 성능

[http://prezi.com/ehj7w5coi4gp/javascript/](http://prezi.com/ehj7w5coi4gp/javascript/)


### 요청 횟수를 줄이고 캐싱을 활용!
게으른 로딩(lazy loading) + 브라우져 캐싱


#### js파일 압축(이라기 보단 합치기!)
`cat *.js > app.js`
또는 아에 압축! -> GZip

cat 명령의 결과를 app.js에 박는다. 이런건 보통 빌드툴로 하게된다.
jQuery 의 경우 그런트? 노드로 관리?

[Grunt](http://gruntjs.com/)를 이용해서 js 압축하기~




#### 1. javascript 파일은 `</body>` 태그 바로 위에!


#### 2. 스코프 관리 - 지역변수 접근이 빠르기 때문에 자주쓰는건 지역변수로 선언후 사용(캐싱)
ex)
```javascript
function(){
  var doc = document;
  doc.~~~
}
```

#### 3. 객체/배열은 리터럴 사용
```javascript
new Object() -> {}
new Array() -> []
```


#### 4. [CDN(content delivery network)](http://goo.gl/U4bdT) 활용!


#### 5. [JSPref](http://jsperf.com/jquery-css-vs-native-dom/16)
해당 os, browser 별 성능 표 제공.ㅎㅎ


#### 6. [PageSpeed Insights (Chrome extention - google)](http://goo.gl/hoJzt)
page load 최적화 관련해서 성능을 올릴 수 있는 팁? 제공해줌.ㅎㅎ


#### 7. HTTP 를 이해!
request
- method
- uri
- data

response
- header
 - status
```
200 ok / 
4xx client error / 
5xx server error
```
- header - content-type=text/html | zip?
- body



## 재밌는 HTML5 + JS


#### [TML5 로 만든것들 모아둔 사이트인듯](ttp://hakim.se/)
 [Game - Coil](http://hakim.se/experiments/html5/coil/)
 [Sketch toy](http://sketchtoy.com/)
 
 
 
#### [10 Best JS Drawing Libs](http://javascript.open-libraries.com/utilities/drawing/10-best-javascript-drawing-and-canvas-libraries/)
