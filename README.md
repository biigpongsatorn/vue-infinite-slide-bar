<p>
<a href="https://npmjs.com/package/vue-infinite-slide-bar"><img src="https://img.shields.io/npm/v/vue-infinite-slide-bar.svg?style=flat" alt="NPM version"></a>
<a href="https://npmjs.com/package/vue-infinite-slide-bar"><img src="https://img.shields.io/npm/dm/vue-infinite-slide-bar.svg?style=flat" alt="NPM downloads"></a>
<a href="https://www.npmjs.com/package/vue-infinite-slide-bar"><img src="https://img.shields.io/npm/l/vue-infinite-slide-bar.svg?style=flat" alt="License"></a>
<a href="https://biigpongsatorn.github.io/#/vue-infinite-slide-bar"><img src="https://travis-ci.org/biigpongsatorn/biigpongsatorn.github.io.svg?branch=dev" alt="Demo Build Status"></a>
</p>

# ∞ Vue Infinite Slide Bar

🎚 Infinite slide bar component. (Lightweight 2KB)

# 👀 Document & Demo Page

Coming soon...

# 💻 Install

```sh
npm install vue-infinite-slide-bar --save
```
or
```sh
yarn add vue-infinite-slide-bar
```

# 🕹 Usage
```javascript
// main.js
import Vue from 'vue'
import InfiniteSlideBar from 'vue-infinite-slide-bar'

Vue.component('InfiniteSlideBar', InfiniteSlideBar)
```
or
```javascript
// xxx.vue
import InfiniteSlideBar from 'vue-infinite-slide-bar'

export default {
  components: {
    InfiniteSlideBar
  }
}
```

# 🔎 Example

```html
<infinite-slide-bar :style="{ color: '#fff', background: '#42b883', 'font-weight': 'bold' }">
  Helo World, I love Vue.js
</infinite-slide-bar>
```

# ⚙️ Props
| Props       | Type          | Default  | Description  |
| ----------- |:--------------| ---------|--------------|
| style       | Object        | { padding: '5px 0' }     | Customize style of slide bar |
| duration      | String        | 12s     | Speed of animation |
| direction      | String        | normal     | Direction of animation (`normal`, `reverse`) |
| delay      | String        | 0s     | Delay time before animation start |

# 🤝 Contributing
1. Fork this repository.
2. Create new branch with feature name.
3. Run `npm install` and `npm run dev`.
4. Create your feature.
5. Commit and set commit message with feature name.
6. Push your code to your fork repository.
7. Create pull request. 🙂

# ⭐️ Support

```
If you like this project, You can support me with starring ⭐ this repository.
```

# 📄 License

[MIT](LICENSE)

Developed with ❤️ and ☕️ 
