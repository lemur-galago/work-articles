<style>
mark{
    color: red
}
</style>
<mark>Тест внешних стилей в GitHub</mark>


# Дополнительные стили

Специально для написания внутренней документации была добавлена таблица стилей для оформления некоторых специфических элементов:

```css
tip, info, warning {
  --tip-header-content: "✐ TIP";
  --tip-background-color: #e6f6e6;
  --tip-foreground-color: #003100;
  --tip-border-color: #009400;

  --info-header-content: "Ⓘ INFO";
  --info-background-color: #eef9fd;
  --info-foreground-color: #003100;
  --info-border-color: #4cb3d4;

  --warning-header-content: "❗ WARNING";
  --warning-background-color: #ffebec;
  --warning-foreground-color: #003100;
  --warning-border-color: #e13238;

  --header-font-weight: bold;
  --header-font-size: large;
  --header-font-family: system-ui,-apple-system,Segoe UI,Roboto,Ubuntu,Cantarell,Noto Sans,sans-serif,BlinkMacSystemFont,"Segoe UI",Helvetica,Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji","Segoe UI Symbol";
  --header-margin: 0 0 10px 0;

  --shadow: 0 1px 2px 0 rgba(0, 0, 0, .1);
  --border-left-width: 5px;
  --border-radius: .4rem;
  --padding-vertical: 1rem;
  --padding-horisontal: 1rem;

  display: block;
  width: 100%;
  border: 0 solid var(--tip-border-color);
  border-left-width: var(--border-left-width);
  border-radius: var(--border-radius);
  box-shadow: var(--shadow);
  padding: var(--padding-vertical) var(--padding-horisontal);
}

tip::before, info::before, warning::before {
  display: block;
  font-weight: bold;
  font: var(--header-font-weight) var(--header-font-size) var(--header-font-family);
  margin: var(--header-margin);
}

/* Совет */
tip {
  background-color: var(--tip-background-color);
  color: var(--tip-foreground-color);
  border-color: var(--tip-border-color);
}
tip::before {
  content: var(--tip-header-content);
}

/* Информация */
info {
  background-color: var(--info-background-color);
  color: var(--info-foreground-color);
  border-color: var(--info-border-color);
}
info::before {
  content: var(--info-header-content);
}

/* Внимание */
warning {
  background-color: var(--warning-background-color);
  color: var(--warning-foreground-color);
  border-color: var(--warning-border-color);
}
warning::before {
  content: var(--warning-header-content);
}
```

Для использования специальных элементов оформления должен быть подключен приложенный css-стиль.

## Примеры информационных блоков

### Совет
```html
<tip>
Это пример оформления совета
</tip>
```

<tip>
Это пример оформления совета
</tip>

### Информация
```html
<info>
Это пример оформления информации
</info>
```

<info>
Это пример оформления информации
</info>

### Предупреждение
```html
<warning>
Это пример оформления предупреждения
</warning>
```

<warning>
Это пример оформления предупреждения
</warning>

