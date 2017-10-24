## Feedback building an app

<img src="/assets/images/pauling.png" style="height: 200px">

[TailorDev/pauling](https://github.com/TailorDev/pauling)


### Complexity

If you don't know mobile app development, you don't know mobile app dev: browser
!== device.


### iOS first, Android second

React Native started as an iOS project and Android has been added later. iOS
support is therefore better.


### It is still alpha

It works and you can use in production, but:

- navigation is not solved
- you may find bugs
- some libraries are immature


### Target both platforms from Day 1

1. It works on iOS \o/
2. It works on Android \o/
3. iOS app is broken now... 😅


### Keep components similar...

``` js
import StyleSheet from 'app/PaulingStyleSheet';

export default StyleSheet.create({
  Header: {
    paddingTop: 0,
    android: {
      height: 56,
    },
    ios: {
      height: 44,
    },
  },
  // ...
});
```


### ...but split when it makes sense

``` js
import PosterViewer from 'app/PosterViewer';

<PosterViewer
  fileType={poster.file_type}
  path={poster.cached_file}
/>
```

<br>
``` plain
src/PosterViewer
├── index.android.js
├── index.android.test.js
├── index.ios.js
└── index.ios.test.js
```


### Developer Experience

- Debugger in Chrome
- Fast feedback loop
- Live/Hot reload is ❤️❤️❤️


![](/assets/images/hot-reload.gif)
