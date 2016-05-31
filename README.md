# vue-swiper
Swiper component. Easy to use.
## [DEMO](http://weilao.github.io/vue-swiper/demo)
## Install
```
npm i vue-swiper -S
```

## Usage

```js
import Swiper from 'vue-swiper'
new Vue({
    el: 'body',
    components: {Swiper},
    methods: {
        onSlideChangeStart (currentPage) {
            console.log('onSlideChangeStart', currentPage);
        },
        onSlideChangeEnd (currentPage) {
            console.log('onSlideChangeEnd', currentPage);
        }
    }
});
```

```html
<swiper v-ref:swiper
        :performance-mode="true"
        @slide-change-start="onSlideChangeStart"
        @slide-change-end="onSlideChangeEnd">
    <div>Page 1</div>
    <div>Page 2</div>
</swiper>
```

## Api
### Properties

#### performace-mode `Boolean`

Disable advance effect for better performance, defaults to `false`.

### Methods
#### next()
Go next page.

#### prev()
Go previous page.

#### setPage(`Number`)
Set current page number.

### Events
#### slide-change-start
Fire in the beginning of animation to other slide (next or previous).
 
#### slide-change-end
Will be fired after animation to other slide (next or previous).
