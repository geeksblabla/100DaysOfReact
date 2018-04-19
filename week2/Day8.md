What is the result of the snippet below ?! Does is run smoothly on iOS and/or Android ?
```
import React, { Component } from 'react';
import {
 Text,
 View
} from 'react-native';
export default class MyContainerComponent extends Component {
 constructor() {
   super()
   this.state = {
    myText: 'Hello DevC Casa!'
   }
 }
 render() {
   return (
    <View>
      <Text>
       {this.state.myText}
      </Text>
    </View>
   );
 }
}
```