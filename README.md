# *Ehcache Example*

 출처는 **기억보단 기록을**(https://jojoldu.tistory.com/57). 자세한 설명은 출처 링크를 참고.



### 🍊 실습

1. 아래의 url로 접근하면 콘솔창에서 name을 호출하는 데 걸린 시간을 확인할 수 있다. 캐시가 적용되지 않아서 연속적으로 호출했을 때 거의 비슷한 시간이 걸리는 것을 확인할 수 있다.

````
localhost:8080/member/nocache/{name}
````



2. 반면 아래의 url로 접근하면 name을 호출하는 데 걸린 시간이 차이를 보인다. 첫 호출은 캐시를 적용하지 않은 경우와 비슷한 시간이 걸리지만 이후로는 캐시로 관리하기 때문에 빠른 속도로 호출됨을 확인할 수 있다.

````
localhost:8080/member/cache/{name}
````



3. 아래의 url로 접근하면 캐시 데이터가 삭제된다.

````
localhost:8080/member/refresh/{name}
````

