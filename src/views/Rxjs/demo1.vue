
<template>
  <div>

  </div>
</template>

<script lang="ts">
import { Observable } from 'rxjs/Observable';

// const oneObservable = Observable.create(subscriber => {
//   subscriber.next('🍎')
//   subscriber.next('🍊')
//   subscriber.complete()
// })

// const oneObserver = {
//   next: data => console.log(data),
//   complete: () => console.log('done!')
// }

// oneObservable.subscribe(oneObserver)

var myObservable = Observable.create(observer => {
  observer.next('foo');
  setTimeout(() => observer.next('bar'), 1000);
});
myObservable.subscribe(value => console.log(value));

</script>
