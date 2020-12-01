## Компонент загрузки пользовательских файлов на страницу
<br />

Реализован drag & drop, вывод ошибки при попытке:
 - повторной загрузки файла
 - загрузить неразрешенный формат
 - превышения лимита количества загруженных файлов.

props | description
--- | ---
text | заголовок инпута
onChange | функция-коллбэк
allowedTypes | массив с типами файлов
typesForError | строка с расширениями для текста ошибки
hint | текст-подсказка
<br />
По дефолту принимает файлы форматов png, jpeg

<br />
```javascript
<Download
    text="Загрузите или перетащите файл"
    hint='Вы можете прикрепить до 5 файлов'
    onChange={this.onChange}
    allowedTypes={ ["image/png","image/jpeg"] }
    typesForError='png, jpeg'
/>
```