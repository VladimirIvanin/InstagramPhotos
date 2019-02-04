# Instagram

[Сгенерировать токен](http://instagram.pixelunion.net/)

В настройках аккаунта обязательно нужно убрать галку с "Disable implicit OAuth:"

Как пользоваться плагином:

```js
var myInstagram = new InstagramPhotos({
  user_id: 1111112,
  access_token: '111112.1677ed0.9844c23093e34ff290cd09d941e22535',
  countPhoto: 20,
  filterImages: null, // отфильтровать фото по какому-нибудь признаку, например тегу function (image){ return image.tags.indexOf('beauty') > -1 }
  done: function (photos) {
    // тут рисуем вывод фотографий
  },
  fail: function (error) {
    if (error.meta) {
      console.warn(error.meta.error_message);
    }
  }
});
```

[Популярная библиотека для вывода фотографий как альтернатива InstagramPhotos](http://instafeedjs.com/)
