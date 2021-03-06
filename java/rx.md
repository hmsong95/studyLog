RxJava
-----------

### `Observable`

#### `just`, `from`
  간단하게 값 하나나 컬렉션에 대해서 `Observable` 생성하는 유틸매서드

#### `map`
  map

#### `scan`
  reduce 와 비슷한 역할

#### `subscribeOn`
  `Observable` 하는 대상들이 `onNext` 되는 쓰레드 설정

#### `observeOn`
  `subscribe`를 하는 쓰레드 설정

#### `subscribe`
  스트림에서 받아온 아이템에 대해서 작업할것

#### `merge`
  `Observable` 합치기(그냥 스트림에서 나오는것 그대로 리턴)

#### `zip`
  `Observable` 합치기(모든 스트림에서 모두 onNext()가 호출된 후 리턴. 즉 모두 올때까지 기다린다.)

#### `combineLatest`
  `zip` 이랑 비슷하지만, 대신 각 `Observable`에서 나온 값들을 캐싱하고 있다. 

#### `publishSubject`
  `Observable` 만들 때 사용할 수 있음
  ex)
  ```java
  PublishSubject ps<View> = PublishSubject.create();
  view.setOnClickListener(v->ps.onNext(v));
  
  Observable<View> observable = ps.asObservable();
  ```

#### `retryWhen`
  onError 일때 다시 시도할지 말지를 결정한다.
  
  > if a source Observable emits an error, pass that error to another Observable to determine whether to resubscribe to the source [참고](https://github.com/ReactiveX/RxJava/wiki/Error-Handling-Operators)


