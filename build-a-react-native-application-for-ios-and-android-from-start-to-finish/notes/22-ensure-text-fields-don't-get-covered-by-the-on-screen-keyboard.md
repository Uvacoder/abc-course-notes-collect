# Ensure Text Fields Don't Get Covered by the On Screen Keyboard

**[๐น Video](https://egghead.io/lessons/react-native-ensure-text-fields-don't-get-covered-by-the-on-screen-keyboard)**

## Multiline inputs

The `<TextInput />` component can be turned into a multiline input - similar to HMTL `<textarea />` - by adding the `multiline={true}` and `numberOfLines={5}` props. The `numberOfLines` can be any number.

```jsx
<TextInput
  // other props
  multiline={true}
  numberOfLines={2}
/>
```

## Onscreen keyboard

When focusing an input the onscreen keyboard is automatically displayed. If this does not open in the simulator, it can be toggled from the developer menu - `cmd + d` or `cmd + m` on macOS and `ctrl + m` on Windows.

๐The onscreen keyboard can cover the page content. To fix this we can install the `<KeyboardAwareScrollView />` component from NPM.

```bash
npm i react-native-keyboard-aware-scrollview
```

๐This can be used to wrap each screen to ensure the keyboard does not hide page content.

```jsx
render() {
  return (
    <KeyboardAwareScrollView>
      <TextInput />
      // other components
    </KeyboardAwareScrollView>
  )
}
```

---

๐น [Go to Previous Lesson](https://egghead.io/lessons/react-native-add-a-modal-screen-that-pops-up-from-the-bottom-with-react-navigation)
๐น [Go to Next Lesson](https://egghead.io/lessons/react-native-show-a-spinner-while-submitting-a-form-in-react-native-with-activityindicator)
