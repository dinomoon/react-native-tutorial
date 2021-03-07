# React Native Tutorial

## ✔ Views, Text & Styles

- `View` is a container that supports layout with flexbox, style, some touch handling, and accessibility controls. (div라고 생각하면 될 것 같다.)
- `Text` is a react component for displaying text.

<br/>

## ✔ Using State

- react처럼 useState사용가능
- Button component가 존재하는데, self closing component임. title속성의 값으로 text를 전달

```js
<Button
  onPress={onPressLearnMore}
  title="Learn More"
  color="#841584"
  accessibilityLabel="Learn more about this purple button"
/>
```

<br/>

## ✔ Text Inputs

```js
  <Text>Enter name:</Text>
  <TextInput
    multiline
    style={styles.input}
    placeholder="e.g. John Doe"
    onChangeText={(val) => setName(val)}
  />
  <Text>Enter age:</Text>
  <TextInput
    keyboardType="numeric"
    style={styles.input}
    placeholder="e.g. 99"
    onChangeText={(val) => setAge(val)}
  />
  <Text>
    name: {name}, age: {age}
  </Text>
```

<br/>

## ✔ Lists & ScrollView

- Scroll이 가능하게 하기 위해서는 ScrollView로 감싸줘야한다.

<br/>
