## Input

Input component. You can use the `v-model` directive to create two-way data bindings and use a clear button to clear the content.

### Example

- Basic usage

You can use the `v-model` directive to create two-way data bindings

```html
<cube-input v-model="value" ></cube-input>
```

```javascript
export default {
  data() {
    return {
      value: ''
    }
  }
}
```

- Multiple configurations

Support most of the attributes of the input element. In addition you can use the `useClear` attribute to toggle the clear button.

```html
<cube-input
  v-model="value"
  :placeholder="placeholder"
  :type="type"
  :maxlength="maxlength"
  :readonly="readonly"
  :disabled="disabled"
  :autofocus="autofocus"
  :autocomplete="autocomplete"
  :useClear="useClear"
></cube-input>
```

```javascript
export default {
  data() {
    return {
      value: '',
      placeholder: '请输入内容',
      type: 'password',
      readonly: true,
      maxlength: 100,
      disabled: true,
      autofocus: true,
      autocomplete: true,
      useClear: false
    }
  }
}
```

### Props configuration

| Attribute | Description | Type | Accepted Values | Default |
| - | - | - | - | - |
| type | type of input | String | text/number/password/date | text |
| v-model | bound value | String | - | empty |
| disabled | disabled status | Boolean | true/false | false |
| readonly | readonly status | Boolean | true/false | false |
| maxlength | maxlength of input | Number | - | 60 |
| placeholder | placeholder of input | String | - | empty |
| autofocus | autofocus status | Boolean | true/false | false |
| autocomplete | autocomplete status | Boolean | true/false | false |
| useClear | whether to show clear button | Boolean | true/false | true |

### Event

| Event Name | Description | Parameters |
| - | - | - |
| focus | This event is triggered after the input box is focused. If input is disabled, it will not be triggered | e - event |
| blur | This event is triggered after the input box blur | e - event |