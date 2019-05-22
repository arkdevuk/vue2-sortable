# vue2-sortable

> Easily add drag-and-drop sorting to your Vue.js applications using the v-sortable2 directive, a thin wrapper for the minimalist [RubaXa/SortableJS](https://github.com/RubaXa/Sortable) library. 
Based on [sagalbot/vue-sortable](https://github.com/sagalbot/vue-sortable)


Installation
--

#### NPM

```bash
npm install vue2-sortable
```

Setup

```javascript
import Vue from 'vue'
import Sortable2 from 'vue2-sortable'

Vue.use(Sortable2)
```

Common Use Cases
--

#### Update Source Data Order

```javascript
new Vue({
  el: 'body',
  data: {
    list: ['Foo', 'Bar', 'Baz']
  },
  methods: {
    onUpdate: function (event) {
      this.list.splice(event.newIndex, 0, this.list.splice(event.oldIndex, 1)[0])
    }
  }
});
```

```html
<ul v-sortable2="{ onUpdate: onUpdate }">
    <li v-for="item in list">{{ item }}</li>
 </ul>
```

Contributing
--

Feel free to fork or PR :)

