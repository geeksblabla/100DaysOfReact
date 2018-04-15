Consider running this snippet on iOS Platform, Does the text get Justified or not?

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
      <Text style={{alignText:"justify"}}>
       {this.state.myText}
      </Text>
    </View>
   );
 }
}
```
