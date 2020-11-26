This library is still in the state of developing and testing. Use at your own risk!

# React Native Custom Modal Alert

A customizable pop-up alert using [react-native-modal](https://github.com/react-native-modal/react-native-modal) to display and [react-native-vector-icons](https://github.com/oblador/react-native-vector-icons) for buttons

## Installation

Install it with

```bash
npm i react-native-custom-modal-alert
```
OR
```bash
yarn add react-native-custom-modal-alert
```

## Usage

1. Import react-native-custom-modal-alert
```js
import useCustomAlert from 'react-native-custom-modal-alert';
```

2. Create ```useCustomAlert``` object
```js
const { showCustomAlert, renderCustomAlert } = useCustomAlert();
```

3. Nest ```renderCustomAlert```component into the page's element
```js
return (
  <>
    { renderCustomAlert() }
    <SafeAreaView>
        ...
    </SafeAreaView>
  </>
);
```

4. Show alert by calling ```showCustomAlert``` API
```js
renderInstructions = () =>{
    return(
        <View style={{width:'90%', alignSelf: 'center'}}>
            <Text style={{margin: 10}}>{"Body goes here"}</Text>
        </View>
    );
}

showCustomAlert({
    title:"Title goes here",
    body:renderInstructions(),
    hasCancelButton:true,
    borderColor: 'black'
})
```

## Props

| Name                 | Type             | Default      | Description                                   |
| -------------------- | ---------------- | ------------ | --------------------------------------------- |
| title                | string           | undefined    | Title for the alert                           |
| body                 | element          | undefined    | Body component for the alert                  |
| hasCancelButton      | boolean          | false        | Controls the visibility of the cancel button  |
| borderColor          | string           | undefined    | Border color for the alert                    |

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://github.com/eddie-lim/react-native-custom-modal-alert/blob/master/LICENSE)