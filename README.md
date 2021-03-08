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

- Scroll이 가능하게 하기 위해서는 `ScrollView`로 감싸줘야한다.

```jsx
<ScrollView>
  {people.map((item) => (
    <View key={item.key}>
      <Text style={styles.item}>{item.name}</Text>
    </View>
  ))}
  ;
</ScrollView>
```

<br/>

## ✔ Flat List Component

- `ScrollView`와 같은 기능을 함
- 차이점: ScrollView는 화면이 나타날 때 모든 아이템을 렌더링하지만, FlatList는 유저가 화면을 스크롤할 때마다 렌더링한다. -> `FlatList`의 성능이 더 좋다. + less code
- `View`에 key를 넘겨주는 것처럼 `keyExtractor`를 사용해 key를 넘겨주어야한다. (객체의 key이름을 key라고 하면 안써줘도 된다.)
- `numColums`속성을 사용해 column의 수를 정할 수 있다.

```jsx
<FlatList
  numColumns={2}
  keyExtractor={(item) => item.id}
  data={people}
  renderItem={({ item }) => <Text style={styles.item}>{item.name}</Text>}
/>
```

<br/>
